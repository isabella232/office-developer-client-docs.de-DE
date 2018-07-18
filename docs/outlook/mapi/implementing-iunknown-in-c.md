---
title: Implementieren von IUnknown in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d12201d8476d15021e896a44797ae5fc21178802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792569"
---
# <a name="implementing-iunknown-in-c"></a>Implementieren von IUnknown in C

**Betrifft**: Outlook 
  
Implementierungen von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) -Methode in C# sind C++ Implementierungen sehr ähnlich. Es gibt zwei grundlegende Schritte an der Implementierung: 
  
1. Überprüfen die Parameter.
    
2. Überprüfen den Bezeichner des mit der Liste der Schnittstellen, die durch das Objekt unterstützt die angeforderte Schnittstelle und Zurückgeben der E_NO_INTERFACE-Wert oder einen Zeiger gültige Schnittstelle. Wenn ein Schnittstellenzeiger zurückgegeben wird, sollte die Implementierung die [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode, um den Referenzzähler erhöhen auch aufrufen. 
    
Der Hauptunterschied zwischen einer Implementierung von **QueryInterface** in C# und C++ ist der erste zusätzliche Parameter in der C-Version. Da der Parameterliste der Objektzeiger hinzugefügt wird, benötigen eine C#-Implementierung von **QueryInterface** Weitere Parameter Überprüfung als eine C++-Implementierung. Die Logik für die Überprüfung der Identifier, erhöht den Referenzzähler und Zurückgeben eines Objektzeigers muss in beiden Sprachen identisch sein. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie **QueryInterface** in C für ein Statusobjekt implementieren. 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

Während die Implementierung der **AddRef** -Methode in C# eine C++-Implementierung ähnlich ist, kann eine C#-Implementierung der [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufwendigeres als eine C++-Version abrufen. Dies ist, da der Großteil der Funktionalität Zusammenhang mit der Freigabe eines Objekts in C++ Konstruktor und Destruktor integriert werden kann und C hat kein entsprechender Mechanismus. Alle diese Funktionalität muss in der **Version** -Methode enthalten sein. Darüber hinaus ist aufgrund der zusätzliche Parameter und dessen explizite Vtable, weitere Validierung erforderlich. 
  
Der folgende Aufruf von **AddRef** -Methode veranschaulicht eine typische C-Implementierung für ein Statusobjekt. 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

Das folgende Codebeispiel zeigt für ein Objekt der C-Status eine normale Implementierung der **Version** . Wenn Sie der Referenzzähler 0 ist, nachdem er verringert wird, sollte eine C Status objektimplementierung die folgenden Aufgaben ausführen: 
  
- Lassen Sie alle angehaltenen Zeiger auf Objekte. 
    
- Die Vtable auf NULL festgelegt wurde, im Fall, in dem ein Objekt Benutzer mit dem Namen **Version** noch fortgesetzt versuchen, verwenden Sie das Objekt, Debuggen erleichtern. 
    
- Rufen Sie **MAPIFreeBuffer** , um das Objekt frei. 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)
- [Implementieren der IUnknown-Schnittstelle](implementing-the-iunknown-interface.md)


---
title: Implementieren von IUnknown in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346774"
---
# <a name="implementing-iunknown-in-c"></a>Implementieren von IUnknown in C

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementierungen der [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode in C ähneln C++-Implementierungen. Die Implementierung umfasst zwei grundlegende Schritte: 
  
1. Validieren von Parametern.
    
2. Überprüfen des Bezeichners der angeforderten Schnittstelle anhand der Liste der vom Objekt unterstützten Schnittstellen und Zurückgeben des E_NO_INTERFACE-Werts oder eines gültigen Schnittstellenzeigers. Wenn ein Schnittstellenzeiger zurückgegeben wird, sollte die Implementierung auch die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode aufrufen, um den Verweiszähler zu erhöhen. 
    
Der Hauptunterschied zwischen einer Implementierung von **QueryInterface** in c und C++ ist der zusätzliche erste Parameter in der c-Version. Da der Objektzeiger der Parameterliste hinzugefügt wird, muss eine C-Implementierung von **QueryInterface** mehr Parametervalidierung als eine C++-Implementierung aufweisen. Die Logik zum Überprüfen des Schnittstellen Bezeichners, erhöhen der Verweisanzahl und Zurückgeben eines Objektzeigers sollte in beiden Sprachen identisch sein. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie **QueryInterface** in C für ein Status-Objekt implementiert wird. 
  
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

Während die Implementierung der **AddRef** -Methode in c der c++-Implementierung ähnelt, kann eine C-Implementierung der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufwändiger als eine c++-Version sein. Der Grund dafür ist, dass ein Großteil der Funktionalität, die mit der Freigabe eines Objekts verbunden ist, in den C++-Konstruktor und Destruktor integriert werden kann und C keinen solchen Mechanismus besitzt. Alle diese Funktionen müssen in der **Release** -Methode enthalten sein. Außerdem ist aufgrund des zusätzlichen Parameters und der expliziten Vtable eine weitere Validierung erforderlich. 
  
Der folgende **AddRef** -Methodenaufruf veranschaulicht eine typische C-Implementierung für ein Status-Objekt. 
  
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

Das folgende Codebeispiel zeigt eine typische Implementierung von **Release** für ein C Status-Objekt. Wenn der Verweiszähler nach dem Dekrementieren 0 ist, sollte die Implementierung eines C-Status Objekts die folgenden Aufgaben ausführen: 
  
- Geben Sie alle gehaltenen Zeiger auf Objekte frei. 
    
- Legen Sie die Vtable auf NULL fest, um das Debuggen zu erleichtern, wenn der Benutzer des Objekts " **Release** " noch weiterhin versucht, das Objekt zu verwenden. 
    
- Rufen Sie **mapifreebufferfreigegeben** auf, um das Objekt freizugeben. 
    
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


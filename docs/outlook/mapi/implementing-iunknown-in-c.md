---
title: Implementieren von IUnknown in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 11c52770251528f58edd09b66fdf855c6669fdf4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620744"
---
# <a name="implementing-iunknown-in-c"></a>Implementieren von IUnknown in C

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementierungen der [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) in C sind C++-Implementierungen sehr ähnlich. Es gibt zwei grundlegende Schritte für die Implementierung: 
  
1. Überprüfen von Parametern.
    
2. Überprüfen des Bezeichners der angeforderten Schnittstelle anhand der Liste der Schnittstellen, die vom Objekt unterstützt werden, und Zurückgeben des werts E_NO_INTERFACE oder eines gültigen Schnittstellenzeigers. Wenn ein Schnittstellenzeiger zurückgegeben wird, sollte die Implementierung auch die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl zu erhöhen. 
    
Der Hauptunterschied zwischen einer Implementierung von **QueryInterface** in C und C++ ist der zusätzliche erste Parameter in der C-Version. Da der Objektzeiger der Parameterliste hinzugefügt wird, muss eine **C-Implementierung von QueryInterface** mehr Parameterüberprüfungen aufweisen als eine C++-Implementierung. Die Logik zum Überprüfen des Schnittstellenbezeichners, zum Erhöhen der Referenzanzahl und zum Zurückgeben eines Objektzeigers sollte in beiden Sprachen identisch sein. 
  
Das folgende Codebeispiel zeigt, wie **QueryInterface** in C für ein Statusobjekt implementiert wird. 
  
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

Während die Implementierung der **AddRef-Methode** in C einer C++-Implementierung ähnelt, kann eine C-Implementierung der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) ausführlicher sein als eine C++-Version. Dies liegt daran, dass ein Großteil der Funktionalität, die mit der Freigabe eines Objekts verbunden ist, in den C++-Konstruktor und Destruktor integriert werden kann und C über keinen solchen Mechanismus verfügt. Alle diese Funktionen müssen in der **Release-Methode** enthalten sein. Außerdem ist aufgrund des zusätzlichen Parameters und der expliziten vtable eine weitere Überprüfung erforderlich. 
  
Der folgende **Aufruf der AddRef-Methode** veranschaulicht eine typische C-Implementierung für ein Statusobjekt. 
  
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

Das folgende Codebeispiel zeigt eine typische Implementierung von **Release** für ein C-Statusobjekt. Wenn die Referenzanzahl 0 ist, nachdem sie verringert wurde, sollte eine C-Statusobjektimplementierung die folgenden Aufgaben ausführen: 
  
- Geben Sie alle gehaltenen Zeiger auf Objekte frei. 
    
- Legen Sie die vtable auf NULL fest, wodurch das Debuggen für den Fall erleichtert wird, dass der Benutzer des Objekts **"Release"** aufgerufen hat, aber weiterhin versucht hat, das Objekt zu verwenden. 
    
- Rufen Sie **MAPIFreeBuffer** auf, um das Objekt frei zu geben. 
    
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


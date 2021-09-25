---
title: Zugreifen auf eine Nachricht in einem IMAP-Speicher, ohne die gesamte Nachricht herunterzuladen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61e81b2b078718bdb7d11d3dc5f99e192077eaa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551450"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Zugreifen auf eine Nachricht in einem IMAP-Speicher, ohne die gesamte Nachricht herunterzuladen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Codebeispiel in C++ gezeigt, das einen Nachrichtenspeicher für die **[IProxyStoreObject-Schnittstelle](iproxystoreobject.md)** abfragt und den zurückgegebenen Zeiger und die **[IProxyStoreObject::UnwrapNoRef-Funktion](iproxystoreobject-unwrapnoref.md)** verwendet, um einen Zeiger auf ein IMAP-Speicherobjekt abzurufen, das entpackt wurde. Die Verwendung dieses nicht gepackten Speichers ermöglicht den Zugriff auf eine Nachricht im aktuellen Zustand, ohne einen Download der gesamten Nachricht zu starten. 
  
Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das unwrappede Speicherobjekt erhöht, müssen Sie nach dem erfolgreichen Aufrufen von **"UnwrapNoRef"** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) aufrufen, um die Referenzanzahl beizubehalten. 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```



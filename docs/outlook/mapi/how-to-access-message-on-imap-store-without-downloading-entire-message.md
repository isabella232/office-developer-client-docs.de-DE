---
title: Zugriff auf eine Nachricht auf ein IMAP-Speicher ohne die gesamte Nachricht herunterladen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a5a327ff74a4058d8eb15928912ca075e55ea95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564388"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Zugriff auf eine Nachricht auf ein IMAP-Speicher ohne die gesamte Nachricht herunterladen

**Betrifft**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Codebeispiel in C++, die Abfragen eines Nachrichtenspeichers für die **[IProxyStoreObject](iproxystoreobject.md)** -Schnittstelle und verwendet die zurückgegebene Zeiger und die **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** -Funktion, um einen Zeiger auf ein IMAP-Speicher-Objekt abzurufen, die wurde allein stehenden. Mit diesem allein stehenden Informationsspeicher ermöglicht den Zugriff auf eine Nachricht im aktuellen Zustand ohne einen Download der gesamten Nachricht aufzurufen. 
  
Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, müssen Sie [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen. 
  
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



---
title: Zugriff auf eine Nachricht auf ein IMAP-Speicher ohne die gesamte Nachricht herunterladen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa7a61da47169ca7c6a1521ad5b3e84685a9b9a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791861"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a><span data-ttu-id="788ee-103">Zugriff auf eine Nachricht auf ein IMAP-Speicher ohne die gesamte Nachricht herunterladen</span><span class="sxs-lookup"><span data-stu-id="788ee-103">Access a message on an IMAP store without downloading the entire message</span></span>

<span data-ttu-id="788ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="788ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="788ee-105">In diesem Thema wird ein Codebeispiel in C++, die Abfragen eines Nachrichtenspeichers für die **[IProxyStoreObject](iproxystoreobject.md)** -Schnittstelle und verwendet die zurückgegebene Zeiger und die **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** -Funktion, um einen Zeiger auf ein IMAP-Speicher-Objekt abzurufen, die wurde allein stehenden.</span><span class="sxs-lookup"><span data-stu-id="788ee-105">This topic shows a code sample in C++ that queries a message store for the **[IProxyStoreObject](iproxystoreobject.md)** interface, and uses the returned pointer and the **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** function to obtain a pointer to an IMAP store object that has been unwrapped.</span></span> <span data-ttu-id="788ee-106">Mit diesem allein stehenden Informationsspeicher ermöglicht den Zugriff auf eine Nachricht im aktuellen Zustand ohne einen Download der gesamten Nachricht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="788ee-106">Using this unwrapped store allows access to a message in its current state without invoking a download of the entire message.</span></span> 
  
<span data-ttu-id="788ee-107">Da **UnwrapNoRef** nicht den Referenzzähler für diese neuen Zeiger auf das allein stehenden Store-Objekt, nach dem erfolgreichen Aufruf von **UnwrapNoRef**erhöht, müssen Sie [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) zum Verwalten von des Referenzzähler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="788ee-107">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you must call [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) to maintain the reference count.</span></span> 
  
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



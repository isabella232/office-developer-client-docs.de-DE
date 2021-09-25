---
title: Algorithmus zum Codieren von Eintrags-IDs und Anlagen-IDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb8ace42381002d96a4a89e2a9b7eb36898d7927
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556931"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algorithmus zum Codieren von Eintrags-IDs und Anlagen-IDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Speicheranbieter kann als Teil eines MAPI Uniform Resource Locator (URL) eine Eintrags-ID und eine Anlagen-ID an den MAPI-Protokollhandler senden, um ein Objekt zu identifizieren, das für die Indizierung bereit ist. Der Store-Anbieter codiert die Eintrags-ID und anlagen-ID als Unicode-Zeichenfolgen. In diesem Thema wird ein Algorithmus gezeigt, der eine kompakte Darstellung der Eintrags-ID oder Anlagen-ID generiert.
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a>Siehe auch



[Informationen zur Notification-Based Store Indizierung](about-notification-based-store-indexing.md)
  
[Informationen zu MAPI-URLs für Notification-Based-Indizierung](about-mapi-urls-for-notification-based-indexing.md)


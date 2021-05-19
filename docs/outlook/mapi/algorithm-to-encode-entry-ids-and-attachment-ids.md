---
title: Algorithmus zum Codieren von Eintrags-IDs und Anlagen-IDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420136"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algorithmus zum Codieren von Eintrags-IDs und Anlagen-IDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Speicheranbieter kann im Rahmen eines MAPI Uniform Resource Locator (URL) eine Eintrags-ID und eine Anlagen-ID an den MAPI-Protokollhandler senden, um ein Objekt zu identifizieren, das für die Indizierung bereit ist. Der Speicheranbieter codiert die Eintrags-ID und die Anlagen-ID als Unicode-Zeichenfolgen. In diesem Thema wird ein Algorithmus gezeigt, der eine kompakte Darstellung der Eintrags- oder Anlagen-ID generiert.
  
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



[Informationen Notification-Based Store Indizierung](about-notification-based-store-indexing.md)
  
[Informationen zu MAPI-URLs für Notification-Based Indizierung](about-mapi-urls-for-notification-based-indexing.md)


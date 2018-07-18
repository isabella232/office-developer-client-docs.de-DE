---
title: Algorithmus zum Codieren von Eintrags-IDs und Anlage-IDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791300"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algorithmus zum Codieren von Eintrags-IDs und Anlage-IDs

  
  
**Betrifft**: Outlook 
  
Ein Anbieter anmelden kann im Rahmen einer MAPI-Uniform Resource Locator (URL) senden eine Eintrags-ID und eine Anlage-ID an der MAPI-Protokollhandler, um ein Objekt zu identifizieren, die für die Indizierung bereit ist. Speicheranbieter codiert die Eintrags-ID und Anlagen-ID als Unicode-Zeichenfolgen. In diesem Thema wird einen Algorithmus, der eine kompakte Darstellung des Eintrags-ID oder der Anlage-ID generiert.
  
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



[Informationen zum benachrichtigungsbasierten Indizieren von Stores](about-notification-based-store-indexing.md)
  
[Informationen zu MAPI-URLs für das benachrichtigungsbasierte Indizieren](about-mapi-urls-for-notification-based-indexing.md)


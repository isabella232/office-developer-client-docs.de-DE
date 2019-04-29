---
title: Algorithmus zum Codieren von Eintrags-IDs und Anlage-IDs
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
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="d9600-103">Algorithmus zum Codieren von Eintrags-IDs und Anlage-IDs</span><span class="sxs-lookup"><span data-stu-id="d9600-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="d9600-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9600-105">Ein Informationsspeicher Anbieter kann als Teil einer MAPI-URL (Uniform Resource Locator) eine Eintrags-ID und eine Anlagen-ID an den MAPI-Protokoll Handler senden, um ein Objekt zu identifizieren, das für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="d9600-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="d9600-106">Der Informationsspeicher Anbieter codiert die Eintrags-ID und die Anlagen-ID als Unicode-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9600-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="d9600-107">In diesem Thema wird ein Algorithmus gezeigt, der eine kompakte Darstellung der Eintrags-ID oder der Anlagen-ID generiert.</span><span class="sxs-lookup"><span data-stu-id="d9600-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d9600-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9600-108">See also</span></span>



[<span data-ttu-id="d9600-109">Informationen zu Benachrichtigungs basierter Speicher Indizierung</span><span class="sxs-lookup"><span data-stu-id="d9600-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="d9600-110">Informationen zu MAPI-URLs für die Benachrichtigungs basierte Indizierung</span><span class="sxs-lookup"><span data-stu-id="d9600-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)


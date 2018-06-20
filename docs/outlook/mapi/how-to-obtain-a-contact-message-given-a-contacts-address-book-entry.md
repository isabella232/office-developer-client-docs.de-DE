---
title: Erhalten Sie eine Kontakte Nachricht erhält eine Kontakte Buch Adresseintrag
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Zuletzt geändert: 13 August 2013'
ms.openlocfilehash: 346e6bc471f5257aacb34c2e7d02a0aade1bb46e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791864"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="6ced3-103">Erhalten Sie eine Kontakte Nachricht erhält eine Kontakte Buch Adresseintrag</span><span class="sxs-lookup"><span data-stu-id="6ced3-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="6ced3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ced3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ced3-105">Dieses Thema enthält ein Beispiel in C++ `HrOpenContact`, die zeigt, wie die [CONTAB_ENTRYID](contab_entryid.md) -Struktur, die einen Eintrag in einem Adressbuch Kontakte die zugehörige MAPI Kontakt Meldung erhalten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ced3-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="6ced3-106">`HrOpenContact`hat die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="6ced3-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="6ced3-107">*LpSession* ist ein Eingabeparameter, die die aktuelle Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ced3-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="6ced3-108">**LPMAPISESSION** in der MAPI-Header-Datei mapix.h definiert ist, als Zeiger auf [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6ced3-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="6ced3-109">*CbEntryID* ist ein Eingabeparameter, der die Größe des Bezeichners Eintrag *LpEntryID* zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6ced3-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="6ced3-110">*LpEntryID* ist ein Eingabeparameter, einen Zeiger auf die Eintrags-ID eines Eintrags im Adressbuch eines Kontakts darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ced3-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="6ced3-111">*UlFlags* ist ein Eingabeparameter, der eine Bitmaske mit Objekt Access Flags, die der Kontakt MAPI-Nachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ced3-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="6ced3-112">*LpContactMessage* ist ein Output-Parameter, der einen Zeiger auf die Nachricht MAPI-Kontakt an.</span><span class="sxs-lookup"><span data-stu-id="6ced3-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="6ced3-113">Um die zugrunde liegenden MAPI-Kontakt Nachricht öffnen `HrOpenContact` zuerst wandelt *LpEntryID* auf einen Zeiger auf **CONTAB_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="6ced3-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="6ced3-114">Es ruft dann [IMAPISession::OpenEntry](imapisession-openentry.md) zum Abrufen von MAPI-Kontakt-Nachricht, die als Parameter übergeben, die Felder *Cbeid* und *Abeid* des Eintrags im Adressbuch Kontakte, die jeweils die Größe des Eintrags-ID identifizieren und die Kennzeichnung der Kontakt MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6ced3-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```

## <a name="see-also"></a><span data-ttu-id="6ced3-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ced3-115">See also</span></span>

- [<span data-ttu-id="6ced3-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6ced3-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)


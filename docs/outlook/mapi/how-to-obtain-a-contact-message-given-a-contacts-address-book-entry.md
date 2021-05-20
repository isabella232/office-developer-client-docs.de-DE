---
title: Abrufen einer Kontaktnachricht mit einem Kontakt-Adressbucheintrag
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Letzte Änderung: 13. August 2013'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437791"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="6486a-103">Abrufen einer Kontaktnachricht mit einem Kontakt-Adressbucheintrag</span><span class="sxs-lookup"><span data-stu-id="6486a-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="6486a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6486a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6486a-105">Dieses Thema enthält ein Beispiel in C++, , das zeigt, wie Sie die CONTAB_ENTRYID-Struktur verwenden, die einen Eintrag in einem Adressbuch für Kontakte identifiziert, um die zugeordnete `HrOpenContact` [#A0](contab_entryid.md) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6486a-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="6486a-106">`HrOpenContact` hat die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="6486a-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="6486a-107">*lpSession*  ist ein Eingabeparameter, der die aktuelle Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6486a-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="6486a-108">**LPMAPISESSION** ist in der MAPI-Headerdatei mapix.h als Zeiger auf [IMAPISession : IUnknown definiert.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="6486a-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="6486a-109">*cbEntryID* ist ein Eingabeparameter, der die Größe des Eintragsbezeichners darstellt, der *lpEntryID zugeordnet ist.*</span><span class="sxs-lookup"><span data-stu-id="6486a-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="6486a-110">*lpEntryID ist*  ein Eingabeparameter, der einen Zeiger auf die Eintrags-ID eines Eintrags in einem Kontaktadressenbuch darstellt.</span><span class="sxs-lookup"><span data-stu-id="6486a-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="6486a-111">*ulFlags ist*  ein Eingabeparameter, der eine Bitmaske darstellt, die Objektzugriffsflags für die MAPI-Kontaktnachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="6486a-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="6486a-112">*lpContactMessage*  ist ein Ausgabeparameter, der einen Zeiger auf die MAPI-Kontaktnachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="6486a-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="6486a-113">Um die zugrunde liegende MAPI-Kontaktnachricht zu öffnen, wird `HrOpenContact` *zunächst lpEntryID* in einen Zeiger auf **CONTAB_ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="6486a-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="6486a-114">Anschließend ruft sie [IMAPISession::OpenEntry](imapisession-openentry.md) auf, um die #A0 zu erhalten. Dabei werden die  *Felder cbeid*  und  *abeid*  des Eintrags im Adressbuch kontakte übergeben, die die Größe der Eintrags-ID bzw. die Eintrags-ID der #A1 identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6486a-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="6486a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6486a-115">See also</span></span>

- [<span data-ttu-id="6486a-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6486a-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)


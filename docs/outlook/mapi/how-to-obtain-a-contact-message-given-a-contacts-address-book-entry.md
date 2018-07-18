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
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Erhalten Sie eine Kontakte Nachricht erhält eine Kontakte Buch Adresseintrag

**Betrifft**: Outlook 
  
Dieses Thema enthält ein Beispiel in C++ `HrOpenContact`, die zeigt, wie die [CONTAB_ENTRYID](contab_entryid.md) -Struktur, die einen Eintrag in einem Adressbuch Kontakte die zugehörige MAPI Kontakt Meldung erhalten identifiziert. 
  
`HrOpenContact`hat die folgenden Parameter: 
  
-  *LpSession* ist ein Eingabeparameter, die die aktuelle Sitzung darstellt. **LPMAPISESSION** in der MAPI-Header-Datei mapix.h definiert ist, als Zeiger auf [IMAPISession: IUnknown](imapisessioniunknown.md).
    
-  *CbEntryID* ist ein Eingabeparameter, der die Größe des Bezeichners Eintrag *LpEntryID* zugeordnet. 
    
-  *LpEntryID* ist ein Eingabeparameter, einen Zeiger auf die Eintrags-ID eines Eintrags im Adressbuch eines Kontakts darstellt. 
    
-  *UlFlags* ist ein Eingabeparameter, der eine Bitmaske mit Objekt Access Flags, die der Kontakt MAPI-Nachricht darstellt. 
    
-  *LpContactMessage* ist ein Output-Parameter, der einen Zeiger auf die Nachricht MAPI-Kontakt an. 
    
Um die zugrunde liegenden MAPI-Kontakt Nachricht öffnen `HrOpenContact` zuerst wandelt *LpEntryID* auf einen Zeiger auf **CONTAB_ENTRYID**. Es ruft dann [IMAPISession::OpenEntry](imapisession-openentry.md) zum Abrufen von MAPI-Kontakt-Nachricht, die als Parameter übergeben, die Felder *Cbeid* und *Abeid* des Eintrags im Adressbuch Kontakte, die jeweils die Größe des Eintrags-ID identifizieren und die Kennzeichnung der Kontakt MAPI-Nachricht. 
  
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

## <a name="see-also"></a>Siehe auch

- [IMAPISession::OpenEntry](imapisession-openentry.md)


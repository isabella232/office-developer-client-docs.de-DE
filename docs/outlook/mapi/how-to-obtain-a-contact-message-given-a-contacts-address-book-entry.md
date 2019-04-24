---
title: Abrufen einer Kontakt Nachricht bei Adressbucheinträgen für Kontakte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Zuletzt geändert: 13 August, 2013'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345955"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Abrufen einer Kontakt Nachricht bei Adressbucheinträgen für Kontakte

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Beispiel in C++ `HrOpenContact`, das zeigt, wie die [CONTAB_ENTRYID](contab_entryid.md) -Struktur verwendet wird, die einen Eintrag in einem Adressbuch für Kontakte identifiziert, um die zugehörige MAPI-Kontakt Nachricht abzurufen. 
  
`HrOpenContact`hat die folgenden Parameter: 
  
-  *lpSession* ist ein Eingabeparameter, der die aktuelle Sitzung darstellt. **LPMAPISESSION** ist in der MAPI-Headerdatei mapix. h als Zeiger auf [IMAPISession: IUnknown](imapisessioniunknown.md)definiert.
    
-  *cbEntryID* ist ein Eingabeparameter, der die Größe der mit *lpEntryID* verknüpften Eintrags-ID darstellt. 
    
-  *lpEntryID* ist ein Eingabeparameter, der einen Zeiger auf den Eintragsbezeichner eines Eintrags in einem Kontakt Adressbuch darstellt. 
    
-  *ulFlags* ist ein Eingabeparameter, der eine Bitmaske darstellt, die Objektzugriffs Kennzeichen für die MAPI-Kontakt Nachricht enthält. 
    
-  *lpContactMessage* ist ein Ausgabeparameter, der einen Zeiger auf die MAPI-Kontakt Nachricht darstellt. 
    
Um die zugrunde liegende MAPI- `HrOpenContact` Kontakt Nachricht zu öffnen, wandelt *lpEntryID* zunächst in einen Zeiger auf **CONTAB_ENTRYID**. Anschließend wird [IMAPISession:: OpenEntry](imapisession-openentry.md) aufgerufen, um die MAPI-Kontakt Nachricht abzurufen und als Parameter die Felder *cbeid* und *Abeid* des Eintrags im Adressbuchkontakte zu übergeben, die die Größe der Eintrags-ID und die Eintragsbezeichner der MAPI-Kontakt Nachricht. 
  
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


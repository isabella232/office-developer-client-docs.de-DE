---
title: Abrufen einer Kontaktnachricht bei einem Kontaktadressbucheintrag
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Last modified: August 13, 2013'
ms.openlocfilehash: d4f56314dc8b2acac859f519ac2e15e219011b27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616971"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Abrufen einer Kontaktnachricht bei einem Kontaktadressbucheintrag

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Beispiel in C++, das zeigt, wie die CONTAB_ENTRYID Struktur verwendet wird, die einen Eintrag in einem Adressbuch kontakte identifiziert, `HrOpenContact` um die zugeordnete MAPI-Kontaktnachricht abzurufen. [](contab_entryid.md) 
  
`HrOpenContact` hat die folgenden Parameter: 
  
-  *lpSession*  ist ein Eingabeparameter, der die aktuelle Sitzung darstellt. **LPMAPISESSION** ist in der MAPI-Headerdatei mapix.h als Zeiger auf [IMAPISession definiert: IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID*  ist ein Eingabeparameter, der die Größe des Eintragsbezeichners darstellt, der  *lpEntryID*  zugeordnet ist. 
    
-  *LpEntryID*  ist ein Eingabeparameter, der einen Zeiger auf den Eintragsbezeichner eines Eintrags in einem Kontaktadressbuch darstellt. 
    
-  *ulFlags*  ist ein Eingabeparameter, der eine Bitmaske mit Objektzugriffsflags für die MAPI-Kontaktnachricht darstellt. 
    
-  *lpContactMessage*  ist ein Ausgabeparameter, der einen Zeiger auf die MAPI-Kontaktnachricht darstellt. 
    
Um die zugrunde liegende MAPI-Kontaktnachricht zu öffnen,  `HrOpenContact` wandelt sie zunächst  *lpEntryID*  in einen Zeiger **in CONTAB_ENTRYID** um. Anschließend wird [IMAPISession::OpenEntry](imapisession-openentry.md) aufgerufen, um die MAPI-Kontaktnachricht abzurufen, wobei die Felder  *"cbeid"*  und  *"abeid"*  des Eintrags im Adressbuch "Kontakte" als Parameter übergeben werden, die jeweils die Größe des Eintragsbezeichners und den Eintragsbezeichner der MAPI-Kontaktnachricht identifizieren. 
  
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


---
title: Erkennen von der Version von Exchange Server in ein Outlook-Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: 3ed3def3fd76ec4f67239958b5d5164d97f81d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791841"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Erkennen von der Version von Exchange Server in ein Outlook-Profil

**Betrifft**: Outlook 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie verwenden die **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** -Eigenschaft und **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** -Eigenschaft, um Informationen zur Version von Microsoft Exchange Server zu erhalten, das aktive Konto ist mit verbunden ist. 
  
Die `GetProfileServiceVersion` -Funktion im Codebeispiel nimmt ein Profil als Eingabeparameter. Je nachdem, ob die **PR_PROFILE_SERVER_VERSION** -Eigenschaft und die **PR_PROFILE_SERVER_FULL_VERSION** -Eigenschaft im angegebenen Profil vorhanden sind die Funktion ruft jede Eigenschaft ab und gibt die entsprechende Versionsinformationen als Ausgabe zurück Parameter. 
  
`GetProfileServiceVersion`Ruft zunächst die Funktion **["MAPIAdminProfiles"](mapiadminprofiles.md)** hinzu, um ein Profil Administration-Objekt zu erstellen. Anschließend wird das Profil Administration-Objekt aufrufen, **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** , um eine Nachricht Service Administration-Objekt zu erhalten. Message Service Administration-Objekts verwenden, es ruft **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** um einen Abschnitt des aktuellen Profils zu erhalten, und anschließend **[HrGetOneProp](hrgetoneprop.md)** überprüft, ob jedes der beiden Eigenschaften in diesem Abschnitt der vorhanden ist, um die das Profil und gegebenenfalls die Versionsinformationen in die entsprechenden Ausgabeparameter festgelegt. 
  
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



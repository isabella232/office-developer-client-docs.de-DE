---
title: Ermitteln, ob Outlook nur die Kopfzeile einer Nachricht heruntergeladen hat
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: acc96bb9-1592-c480-53ee-1325f65297e1
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 04770b2838941239219637a75435fcdd586dca55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551436"
---
# <a name="determine-if-outlook-downloaded-only-the-header-of-a-message"></a>Ermitteln, ob Outlook nur die Kopfzeile einer Nachricht heruntergeladen hat

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Thema wird ein Codebeispiel in Visual C++ gezeigt, das die [kanonische PidLidHeaderItem-Eigenschaft](pidlidheaderitem-canonical-property.md) verwendet, um zu bestimmen, ob Microsoft Outlook 2013 nur die Kopfzeile einer Nachricht oder die Kopfzeile und den Textkörper einer Nachricht heruntergeladen hat. 
  
```cpp
BOOL bIsHeader(LPMESSAGE lpMessage) 
{ 
    HRESULT         hRes = S_OK; 
    BOOL            bRet = false; 
    ULONG    ulVal = 0; 
    LPSPropValue    lpPropVal = NULL; 
    LPSPropTagArray lpNamedPropTag = NULL; 
    MAPINAMEID      NamedID = {0}; 
    LPMAPINAMEID    lpNamedID = NULL; 
 
    NamedID.lpguid = (LPGUID) &PSETID_Common; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidHeaderItem; 
    lpNamedID = &NamedID; 
    hRes = lpMessage->GetIDsFromNames(1, &lpNamedID, NULL, &lpNamedPropTag); 
 
    if (lpNamedPropTag && 1 == lpNamedPropTag->cValues) 
    { 
lpNamedPropTag->aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTag->aulPropTag[0], PT_LONG); 
 
//Get the value of the property. 
hRes = lpMessage->GetProps(lpNamedPropTag, 0, &ulVal, &lpPropVal); 
if (lpPropVal && 1 == ulVal && PT_LONG == PROP_TYPE(lpPropVal->ulPropTag) && lpPropVal->Value.ul) 
{ 
    bRet = true; 
} 
    } 
 
    MAPIFreeBuffer(lpPropVal); 
    MAPIFreeBuffer(lpNamedPropTag); 
    return bRet; 
}

```



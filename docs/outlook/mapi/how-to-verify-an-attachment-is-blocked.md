---
title: Stellen Sie sicher, dass eine Anlage gesperrt ist
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a21383e0ea6920075a57d872e82851462bf0e8d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791883"
---
# <a name="verify-an-attachment-is-blocked"></a>Stellen Sie sicher, dass eine Anlage gesperrt ist

**Betrifft**: Outlook 
  
In diesem Codebeispiel in C++ beschreibt, wie Sie die ["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) Schnittstelle, um herauszufinden, ob eine Anlage von Microsoft Outlook 2010 oder Microsoft Outlook 2013 zum Anzeigen und Indizierung ausgeschlossen wird. 
  
["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) die [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) -Schnittstelle abgeleitet ist. Sie erhalten die ["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) Schnittstelle durch Aufrufen von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) für das MAPI-Sitzungsobjekt **IID_IAttachmentSecurity**anfordern. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) gibt in _PfBlocked_ **true** , wenn die Anlage von Outlook 2010 oder Outlook 2013 unsichere angesehen wird und wird zum Anzeigen und Indizierung in Outlook 2010 oder Outlook 2013 blockiert. 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```



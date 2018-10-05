---
title: Stellen Sie sicher, dass eine Anlage gesperrt ist
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393838"
---
# <a name="verify-an-attachment-is-blocked"></a>Stellen Sie sicher, dass eine Anlage gesperrt ist

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Codebeispiel in C++ beschreibt, wie Sie die ["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) Schnittstelle, um herauszufinden, ob eine Anlage von Microsoft Outlook 2010 oder Microsoft Outlook 2013 zum Anzeigen und Indizierung ausgeschlossen wird. 
  
["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) die [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle abgeleitet ist. Sie erhalten die ["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) Schnittstelle durch Aufrufen von [QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) für das MAPI-Sitzungsobjekt **IID_IAttachmentSecurity**anfordern. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) gibt in _PfBlocked_ **true** , wenn die Anlage von Outlook 2010 oder Outlook 2013 unsichere angesehen wird und wird zum Anzeigen und Indizierung in Outlook 2010 oder Outlook 2013 blockiert. 
  
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



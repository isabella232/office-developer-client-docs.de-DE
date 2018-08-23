---
title: Stellen Sie sicher, dass eine Anlage gesperrt ist
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: bb83b57de3bb484e4fb5f94f76a7d9bfa0fce876
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589798"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="5e135-103">Stellen Sie sicher, dass eine Anlage gesperrt ist</span><span class="sxs-lookup"><span data-stu-id="5e135-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="5e135-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e135-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e135-105">In diesem Codebeispiel in C++ beschreibt, wie Sie die ["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) Schnittstelle, um herauszufinden, ob eine Anlage von Microsoft Outlook 2010 oder Microsoft Outlook 2013 zum Anzeigen und Indizierung ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5e135-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="5e135-106">["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) die [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) -Schnittstelle abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="5e135-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="5e135-107">Sie erhalten die ["IAttachmentSecurity": IUnknown](iattachmentsecurityiunknown.md) Schnittstelle durch Aufrufen von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) für das MAPI-Sitzungsobjekt **IID_IAttachmentSecurity**anfordern.</span><span class="sxs-lookup"><span data-stu-id="5e135-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="5e135-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) gibt in _PfBlocked_ **true** , wenn die Anlage von Outlook 2010 oder Outlook 2013 unsichere angesehen wird und wird zum Anzeigen und Indizierung in Outlook 2010 oder Outlook 2013 blockiert.</span><span class="sxs-lookup"><span data-stu-id="5e135-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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



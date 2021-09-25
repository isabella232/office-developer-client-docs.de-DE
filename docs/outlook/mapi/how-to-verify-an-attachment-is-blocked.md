---
title: Überprüfen, ob eine Anlage blockiert ist
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 57c7c3861073910a1f5331c71e9e5ecc1c0c83a0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576198"
---
# <a name="verify-an-attachment-is-blocked"></a>Überprüfen, ob eine Anlage blockiert ist

**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Codebeispiel in C++ wird gezeigt, wie Die [IAttachmentSecurity : IUnknown-Schnittstelle](iattachmentsecurityiunknown.md) verwendet wird, um herauszufinden, ob eine Anlage durch Microsoft Outlook 2010 oder Microsoft Outlook 2013 zum Anzeigen und Indizieren blockiert wird. 
  
[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) wird von der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) abgeleitet. Sie können die [IAttachmentSecurity : IUnknown-Schnittstelle](iattachmentsecurityiunknown.md) abrufen, indem Sie [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) für das MAPI-Sitzungsobjekt aufrufen und **IID_IAttachmentSecurity** anfordern. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013. 
  
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



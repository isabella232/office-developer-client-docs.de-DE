---
title: Überprüfen, ob eine Anlage blockiert ist
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345885"
---
# <a name="verify-an-attachment-is-blocked"></a>Überprüfen, ob eine Anlage blockiert ist

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Codebeispiel in C++ zeigt, wie Sie die [IAttachmentSecurity : IUnknown-Schnittstelle](iattachmentsecurityiunknown.md) verwenden, um herauszufinden, ob eine Anlage von Microsoft Outlook 2010 oder Microsoft Outlook 2013 zum Anzeigen und Indizierung blockiert wird. 
  
[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) wird von der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) abgeleitet. Sie können die [IAttachmentSecurity : IUnknown-Schnittstelle](iattachmentsecurityiunknown.md) abrufen, indem Sie [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) im MAPI-Sitzungsobjekt aufrufen und **IID_IAttachmentSecurity.** [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) gibt **true** in _pfBlocked_ zurück, wenn die Anlage Outlook 2010 oder Outlook 2013 als unsicher eingestuft wird und für die Anzeige und Indizierung in Outlook 2010 oder Outlook 2013 gesperrt ist. 
  
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



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
  
Dieses Codebeispiel in C++ zeigt, wie Sie die [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) -Schnittstelle verwenden, um herauszufinden, ob eine Anlage von microsoft Outlook 2010 oder microsoft Outlook 2013 zum Anzeigen und indizieren blockiert wird. 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) ist von der [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) -Schnittstelle abgeleitet. Sie können die [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) -Schnittstelle abrufen, indem Sie [IUnknown:: QUERYINTERFACE](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) für das MAPI-sitzungsObjekt aufrufen, das **IID_IAttachmentSecurity**anfordert. [IAttachmentSecurity:: IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) gibt **true** in _pfBlocked_ zurück, wenn die anlage von Outlook 2010 oder Outlook 2013 als unsicher betrachtet wird und zum anzeigen und Indizieren in Outlook 2010 oder Outlook 2013 gesperrt ist. 
  
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



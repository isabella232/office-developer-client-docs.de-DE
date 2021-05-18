---
title: Suchen des Symbols für eine Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409153"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="79bc8-103">Suchen des Symbols für eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="79bc8-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="79bc8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79bc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="79bc8-105">**So suchen Sie das Symbol, das einer Nachricht zugeordnet ist**</span><span class="sxs-lookup"><span data-stu-id="79bc8-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="79bc8-106">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) der Nachricht auf, um die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79bc8-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="79bc8-107">Rufen [Sie MAPIOpenFormMgr auf,](mapiopenformmgr.md) um einen **IMAPIFormMgr-Schnittstellenzeiger** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79bc8-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="79bc8-108">Übergeben Sie den **IMAPISession-Zeiger** im _pSession-Parameter._</span><span class="sxs-lookup"><span data-stu-id="79bc8-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="79bc8-109">Rufen [Sie IMAPIFormMgr::ResolveMessageClass auf,](imapiformmgr-resolvemessageclass.md) um einen **IMAPIFormInfo-Schnittstellenzeiger** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79bc8-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="79bc8-110">Verwenden Sie den **IMAPIFormInfo-Zeiger,** um [IMAPIProp::GetProps](imapiprop-getprops.md) aufrufen und die **Eigenschaften PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und/oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79bc8-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    


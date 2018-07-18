---
title: Suchen nach dem Symbol für eine Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791672"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="23301-103">Suchen nach dem Symbol für eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="23301-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="23301-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23301-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="23301-105">**Nach dem Symbol einer Nachricht**</span><span class="sxs-lookup"><span data-stu-id="23301-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="23301-106">Rufen Sie die Nachricht [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="23301-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="23301-107">Rufen Sie [MAPIOpenFormMgr](mapiopenformmgr.md) zum Abrufen eines **IMAPIFormMgr** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="23301-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="23301-108">Der Parameter _pSession_ übergeben Sie Zeigerposition **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="23301-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="23301-109">Rufen Sie [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) zum Abrufen eines **IMAPIFormInfo** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="23301-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="23301-110">Verwenden Sie den Zeiger **IMAPIFormInfo** [IMAPIProp::GetProps](imapiprop-getprops.md) aufrufen und Abrufen der **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und/oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23301-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    


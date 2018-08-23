---
title: Suchen nach dem Symbol für eine Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567811"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="288ef-103">Suchen nach dem Symbol für eine Nachricht</span><span class="sxs-lookup"><span data-stu-id="288ef-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="288ef-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="288ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="288ef-105">**Nach dem Symbol einer Nachricht**</span><span class="sxs-lookup"><span data-stu-id="288ef-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="288ef-106">Rufen Sie die Nachricht [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="288ef-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="288ef-107">Rufen Sie [MAPIOpenFormMgr](mapiopenformmgr.md) zum Abrufen eines **IMAPIFormMgr** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="288ef-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="288ef-108">Der Parameter _pSession_ übergeben Sie Zeigerposition **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="288ef-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="288ef-109">Rufen Sie [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) zum Abrufen eines **IMAPIFormInfo** Schnittstelle Zeigers.</span><span class="sxs-lookup"><span data-stu-id="288ef-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="288ef-110">Verwenden Sie den Zeiger **IMAPIFormInfo** [IMAPIProp::GetProps](imapiprop-getprops.md) aufrufen und Abrufen der **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und/oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="288ef-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    


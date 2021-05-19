---
title: Folder-Associated Informationstabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426415"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="23ada-103">Folder-Associated Informationstabellen</span><span class="sxs-lookup"><span data-stu-id="23ada-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="23ada-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23ada-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23ada-105">MAPI definiert das MAPI_ASSOCIATED für verschiedene MAPI-Komponenten, die beim Umgang mit zugeordneten Informationstabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23ada-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="23ada-106">Jeder Ordner in einem Nachrichtenspeicher sollte eine zugeordnete Inhaltstabelle zusammen mit seiner Standardinhaltstabelle haben.</span><span class="sxs-lookup"><span data-stu-id="23ada-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="23ada-107">Clientanwendungen speichern spezielle Nachrichten in der zugeordneten Inhaltstabelle eines Ordners, um Formulare und Ansichten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="23ada-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="23ada-108">Um Formulare und Ansichten zu unterstützen, muss ihr Nachrichtenspeicheranbieter verknüpfte Inhaltstabellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="23ada-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="23ada-109">Um zugeordnete Inhaltstabellen zu implementieren, muss Ihr Speicheranbieter die folgenden Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="23ada-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="23ada-110">Unterstützen Sie MAPI_ASSOCIATED-Flag in der [IMAPIContainer::GetContentsTable-Methode,](imapicontainer-getcontentstable.md) damit Clientanwendungen die zugeordnete Inhaltstabelle des Ordners anstelle der Standardinhaltstabelle erhalten können.</span><span class="sxs-lookup"><span data-stu-id="23ada-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="23ada-111">Unterstützen Sie MAPI_ASSOCIATED-Flag in der [IMAPIFolder::CreateMessage-Methode,](imapifolder-createmessage.md) damit Clientanwendungen Nachrichten zur zugeordneten Inhaltstabelle eines Ordners hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="23ada-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="23ada-112">Legen Sie MAPI_ACCESS_CREATE_ASSOCIATED -Bit in **der PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) -Eigenschaft für Ordnerobjekte.</span><span class="sxs-lookup"><span data-stu-id="23ada-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="23ada-113">Unterstützt das DEL_ASSOCIATED in der [IMAPIFolder::EmptyFolder-Methode.](imapifolder-emptyfolder.md)</span><span class="sxs-lookup"><span data-stu-id="23ada-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="23ada-114">Legen Sie MSGFLAG_ASSOCIATED bit in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft für Nachrichten in der zugeordneten Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="23ada-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="23ada-115">Expose and respond to **the PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span><span class="sxs-lookup"><span data-stu-id="23ada-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="23ada-116">Verwalten sie **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) -Eigenschaft in Ordnern.</span><span class="sxs-lookup"><span data-stu-id="23ada-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="23ada-117">Die Eigenschaft PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) enthält kein Bit, um anzugeben, ob ihr Nachrichtenspeicheranbieter verknüpfte Inhaltstabellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23ada-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="23ada-118">Wenn der Nachrichtenspeicheranbieter sie nicht unterstützt, sollte MAPI_E_NO_SUPPORT, wenn Clientanwendungen eine der oben genannten Methoden mit dem MAPI_ASSOCIATED aufrufen.</span><span class="sxs-lookup"><span data-stu-id="23ada-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23ada-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23ada-119">See also</span></span>



[<span data-ttu-id="23ada-120">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="23ada-120">Message Store Features</span></span>](message-store-features.md)


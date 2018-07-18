---
title: Informationstabellen, die Ordnern zugeordnet sind
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791711"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="5f577-103">Informationstabellen, die Ordnern zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="5f577-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="5f577-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f577-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f577-105">MAPI definiert das MAPI_ASSOCIATED-Flag für verschiedene MAPI-Komponenten beim Umgang mit zugehörigen Informationstabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f577-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="5f577-106">Jeden Ordner in einem Nachrichtenspeicher sollte eine zugeordnete Inhaltstabelle zusammen mit dessen standard-Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="5f577-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="5f577-107">Clientanwendungen speichern spezielle Nachrichten in einen Ordner zugeordneten Inhaltstabelle, Formulare und Ansichten enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="5f577-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="5f577-108">Zur Unterstützung der Formulare und Ansichten muss Ihre Nachricht Speicheranbieter tatsächlich zugeordneten Inhalt Tabellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="5f577-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="5f577-109">Um zugeordneten Inhalt Tabellen zu implementieren, muss ein Speicheranbieter Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="5f577-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="5f577-110">Das Flag MAPI_ASSOCIATED in der [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode unterstützt, damit Clientanwendungen den Ordner zugeordneten Inhaltstabelle anstelle der standard Inhaltstabelle abrufen können.</span><span class="sxs-lookup"><span data-stu-id="5f577-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="5f577-111">Unterstützung für das Flag MAPI_ASSOCIATED in die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode Clientanwendungen Nachrichten zu einem Ordner zugeordnete Inhaltstabelle hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="5f577-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="5f577-112">Legen Sie das MAPI_ACCESS_CREATE_ASSOCIATED Bit in die Eigenschaft **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) auf Folder-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5f577-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="5f577-113">Unterstützung für das Flag DEL_ASSOCIATED in die [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5f577-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="5f577-114">Legen Sie das bit in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) für Nachrichten in der zugehörigen Inhaltstabelle MSGFLAG_ASSOCIATED.</span><span class="sxs-lookup"><span data-stu-id="5f577-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="5f577-115">Verfügbar zu machen und reagieren auf die **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft auf den Ordner.</span><span class="sxs-lookup"><span data-stu-id="5f577-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="5f577-116">Verwalten der **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))-Eigenschaft auf den Ordner.</span><span class="sxs-lookup"><span data-stu-id="5f577-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="5f577-117">Es ist keine Bit in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um anzugeben, ob Ihre Nachricht Speicheranbieter zugeordneten Inhalt Tabellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f577-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="5f577-118">Wenn Ihre Nachricht Speicheranbieter diese nicht unterstützt, sollte beim Aufruf von Clientanwendungen eine der oben beschriebenen Methoden mit dem MAPI_ASSOCIATED-Flag MAPI_E_NO_SUPPORT zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5f577-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f577-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f577-119">See also</span></span>



[<span data-ttu-id="5f577-120">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="5f577-120">Message Store Features</span></span>](message-store-features.md)


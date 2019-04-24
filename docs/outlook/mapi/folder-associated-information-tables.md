---
title: Ordner zugeordnete Informationstabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342552"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="6d169-103">Ordner zugeordnete Informationstabellen</span><span class="sxs-lookup"><span data-stu-id="6d169-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="6d169-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d169-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d169-105">MAPI definiert das MAPI_ASSOCIATED-Flag für verschiedene MAPI-Komponenten, die beim Umgang mit zugeordneten Informationstabellen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d169-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="6d169-106">Jeder Ordner in einem Nachrichtenspeicher sollte über eine zugehörige Inhaltstabelle sowie die Tabelle mit den Standardinhalten verfügen.</span><span class="sxs-lookup"><span data-stu-id="6d169-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="6d169-107">Client Anwendungen speichern spezielle Nachrichten in der zugeordneten Inhaltstabelle eines Ordners, um Formulare und Ansichten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6d169-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="6d169-108">Zur Unterstützung von Formularen und Ansichten muss der Nachrichtenspeicher Anbieter zugehörige Inhaltstabellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="6d169-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="6d169-109">Um zugeordnete Inhaltstabellen zu implementieren, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="6d169-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="6d169-110">Unterstützen Sie das MAPI_ASSOCIATED-Flag in der [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode, sodass Clientanwendungen die Tabelle mit den zugeordneten Inhalten des Ordners anstelle der Standardinhalts Tabelle abrufen können.</span><span class="sxs-lookup"><span data-stu-id="6d169-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="6d169-111">Unterstützen Sie das MAPI_ASSOCIATED-Flag in der [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode, sodass Clientanwendungen der Tabelle zugeordnete Inhaltsstoffe eines Ordners Nachrichten hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="6d169-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="6d169-112">Legen Sie das MAPI_ACCESS_CREATE_ASSOCIATED-Bit in der **PR_ACCESS** ([pidtagaccess (](pidtagaccess-canonical-property.md))-Eigenschaft für Folder-Objekte fest.</span><span class="sxs-lookup"><span data-stu-id="6d169-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="6d169-113">Unterstützen Sie das DEL_ASSOCIATED-Flag in der [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6d169-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="6d169-114">Legen Sie das MSGFLAG_ASSOCIATED-Bit in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft für Nachrichten in der Tabelle zugeordnete Inhalte fest.</span><span class="sxs-lookup"><span data-stu-id="6d169-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="6d169-115">Verfügbar machen und reagieren auf die **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft in Ordnern.</span><span class="sxs-lookup"><span data-stu-id="6d169-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="6d169-116">Verwalten der **PR_ASSOC_CONTENT_COUNT** ([pidtagassociatedcontentcount (](pidtagassociatedcontentcount-canonical-property.md))-Eigenschaft für Ordner.</span><span class="sxs-lookup"><span data-stu-id="6d169-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="6d169-117">Die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft gibt kein Bit an, um anzugeben, ob der Nachrichtenspeicher Anbieter zugeordnete Inhaltstabellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d169-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="6d169-118">Wenn Ihr Nachrichtenspeicher Anbieter diese nicht unterstützt, sollte MAPI_E_NO_SUPPORT zurückgegeben werden, wenn Clientanwendungen eine der obigen Methoden mit dem MAPI_ASSOCIATED-Flag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6d169-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d169-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d169-119">See also</span></span>



[<span data-ttu-id="6d169-120">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="6d169-120">Message Store Features</span></span>](message-store-features.md)


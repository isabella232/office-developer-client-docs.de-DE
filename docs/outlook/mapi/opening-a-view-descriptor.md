---
title: Öffnen einer Ansichtsbeschreibung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413038"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="3332d-103">Öffnen einer Ansichtsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="3332d-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="3332d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3332d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3332d-105">Viele Ordner können mit einer Normalansicht, einer Standardansicht oder einer beliebigen Anzahl von personalisierten Ansichten geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3332d-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="3332d-106">In einer Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3332d-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="3332d-107">Die Normalansicht wird verwendet, wenn keine Alternative Ansicht vorhanden ist und Sie den Ordner zum ersten Mal öffnen.</span><span class="sxs-lookup"><span data-stu-id="3332d-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="3332d-108">Wenn eine Alternative Ansicht vorhanden ist, müssen Sie Sie verwenden, um den Ordner zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3332d-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="3332d-109">Eine Ansicht wird in einer Nachricht beschrieben, die als Ansichts Deskriptor bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3332d-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="3332d-110">Ansichts Deskriptoren werden in der Regel als zugeordnete Nachrichten erstellt und können in den Ordnern allgemeine oder persönliche Ansicht oder in einem beliebigen IPM-Ordner angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3332d-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="3332d-111">So öffnen Sie einen Ansichts Deskriptor</span><span class="sxs-lookup"><span data-stu-id="3332d-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="3332d-112">Rufen Sie [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable auf, um die zugeordnete Inhaltstabelle für den Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3332d-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="3332d-113">Erstellen Sie eine Einschränkung, die nur Nachrichten sucht, deren Nachrichtenklasse für Ansichts Deskriptoren reserviert ist, und rufen Sie [IMAPITable:: Restrict](imapitable-restrict.md) auf, um die Tabelle zu begrenzen, und [IMAPITable:: QueryRows](imapitable-queryrows.md) , um die entsprechenden Zeilen abzurufen, oder...</span><span class="sxs-lookup"><span data-stu-id="3332d-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="3332d-114">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Ordners auf, um die zugehörige **PR_DEFAULT_VIEW_ENTRYID** ([pidtagdefaultviewentryid (](pidtagdefaultviewentryid-canonical-property.md))-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3332d-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="3332d-115">**PR_DEFAULT_VIEW_ENTRYID** enthält die Eintrags-ID für die Nachricht, die den Standard Ansichts Deskriptor für einen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="3332d-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="3332d-116">Dieser Aufruf kann erfolgreich ausgeführt werden, wenn der Ordner die Verwendung des MAPI_ASSOCIATED-Flags für Aufrufe von [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontentable unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3332d-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="3332d-117">Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit der Eintrags-ID des Ansichts Deskriptors auf, um Sie zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3332d-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    


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
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="ae889-103">Öffnen einer Ansichtsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ae889-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="ae889-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae889-105">Viele Ordner können mit einer normalen Ansicht, einer Standardansicht oder einer beliebigen Anzahl personalisierter Ansichten geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ae889-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="ae889-106">In einer Ansicht wird beschrieben, wie der Inhalt eines Ordners angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae889-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="ae889-107">Die Normalansicht wird verwendet, wenn es keine alternative Ansicht gibt und Sie den Ordner zum ersten Mal öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae889-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="ae889-108">Wenn eine alternative Ansicht vorhanden ist, müssen Sie sie zum Öffnen des Ordners verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae889-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="ae889-109">Eine Ansicht wird in einer Meldung beschrieben, die als Ansichtsdeskriptor bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ae889-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="ae889-110">Ansichtsdeskriptoren werden in der Regel als zugeordnete Nachrichten erstellt und können entweder in den allgemeinen oder persönlichen Ansichtsordnern oder in einem beliebigen IPM-Ordner angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ae889-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="ae889-111">So öffnen Sie einen Ansichtsdeskriptor</span><span class="sxs-lookup"><span data-stu-id="ae889-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="ae889-112">Rufen [Sie IMAPIContainer::GetContentsTable auf,](imapicontainer-getcontentstable.md) um die zugeordnete Inhaltstabelle für den Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae889-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="ae889-113">Erstellen Sie eine Einschränkung, die nur Nachrichten mit der Nachrichtenklasse sucht, die für Ansichtsdeskriptoren reserviert ist, und rufen Sie [IMAPITable::Restrict](imapitable-restrict.md) auf, um die Tabelle und [IMAPITable::QueryRows](imapitable-queryrows.md) einzuschränken, um die entsprechenden Zeilen abzurufen, oder...</span><span class="sxs-lookup"><span data-stu-id="ae889-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="ae889-114">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Ordners auf, um die **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae889-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="ae889-115">**PR_DEFAULT_VIEW_ENTRYID** enthält die Eintrags-ID für die Nachricht, die den Standardansichtsdeskriptor für einen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="ae889-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="ae889-116">Dieser Aufruf ist erfolgreich, wenn der Ordner die Verwendung des MAPI_ASSOCIATED für Aufrufe von [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) und [IMAPIContainer::GetContentsTable unterstützt.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="ae889-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="ae889-117">Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) mit dem Eintragsbezeichner des Ansichtsdeskriptors auf, um ihn zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae889-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    


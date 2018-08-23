---
title: Durchlaufen des Posteingangsordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594488"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="836c9-103">Durchlaufen des Posteingangsordners</span><span class="sxs-lookup"><span data-stu-id="836c9-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="836c9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="836c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="836c9-105">**Durchlaufen aller Nachrichten im Posteingang**</span><span class="sxs-lookup"><span data-stu-id="836c9-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="836c9-106">Rufen Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , um die Eintrags-ID des Posteingangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="836c9-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="836c9-107">Rufen Sie **IMAPIFolder::OpenEntry** , um den Posteingang zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="836c9-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="836c9-108">Rufen Sie den Posteingang [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode zum Abrufen der Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="836c9-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="836c9-109">Rufen Sie den Inhalt der Tabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode zum Beschränken der Spalte auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) festgelegt und alle anderen Spalten, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="836c9-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="836c9-110">Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen einer Gruppe von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="836c9-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="836c9-111">Bis alle Zeilen in der Inhaltstabelle mehr vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="836c9-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="836c9-112">Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen der Nachricht, durch die Eintrags-ID aus jeder Zeile dargestellt.</span><span class="sxs-lookup"><span data-stu-id="836c9-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="836c9-113">Weisen Sie des _LppUnk_ -Parameters auf einen lokalen **IMessage** -Schnittstellenzeiger.</span><span class="sxs-lookup"><span data-stu-id="836c9-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="836c9-114">Arbeiten Sie mit den Eigenschaften der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="836c9-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="836c9-115">Heben Sie den Zeiger auf den durch den Parameter _LppUnk_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="836c9-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="836c9-116">Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) zum Abrufen der nächsten Gruppe von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="836c9-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="836c9-117">Version der Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="836c9-117">Release the contents table.</span></span>
    


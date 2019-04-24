---
title: Download-Hierarchie Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337009"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="e7d05-103">Download-Hierarchie Status</span><span class="sxs-lookup"><span data-stu-id="e7d05-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="e7d05-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7d05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e7d05-105">In diesem Thema wird beschrieben, was während des Download-Hierarchie Status des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="e7d05-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e7d05-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e7d05-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7d05-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="e7d05-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e7d05-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="e7d05-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="e7d05-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="e7d05-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e7d05-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="e7d05-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="e7d05-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="e7d05-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e7d05-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="e7d05-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="e7d05-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="e7d05-113">To this state:</span></span>  <br/> |<span data-ttu-id="e7d05-114">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="e7d05-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e7d05-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="e7d05-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e7d05-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="e7d05-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e7d05-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7d05-117">Description</span></span>

<span data-ttu-id="e7d05-118">Dieser Status initiiert das Herunterladen einer Strukturhierarchie von Ordnern von einem Server in den lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="e7d05-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="e7d05-119">Outlook initialisiert die zugeordnete **DNHIER** -Datenstruktur mit einem Zeiger auf die Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e7d05-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="e7d05-120">Der Client downloadet die Hierarchie und fügt neue Ordner oder Änderungen in Ordner im lokalen Speicher ein.</span><span class="sxs-lookup"><span data-stu-id="e7d05-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="e7d05-121">Der Downloadprozess übernimmt die Microsoft Exchange-inkrementelle Änderungs Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="e7d05-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e7d05-122">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7d05-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="e7d05-123">Wenn dieser Status endet, wird der lokale Speicher zum Synchronize-Status zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7d05-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7d05-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7d05-124">See also</span></span>



[<span data-ttu-id="e7d05-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="e7d05-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e7d05-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="e7d05-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e7d05-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e7d05-127">SYNCSTATE</span></span>](syncstate.md)


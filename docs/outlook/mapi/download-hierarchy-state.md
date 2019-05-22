---
title: Download des Hierarchie Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337009"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="b9767-103">Download des Hierarchie Status</span><span class="sxs-lookup"><span data-stu-id="b9767-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="b9767-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b9767-105">In diesem Thema wird beschrieben, was während des Download-Hierarchie Status des Replikationsstatus Computers geschieht.</span><span class="sxs-lookup"><span data-stu-id="b9767-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b9767-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b9767-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9767-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b9767-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b9767-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="b9767-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="b9767-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="b9767-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b9767-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="b9767-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="b9767-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="b9767-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b9767-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="b9767-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="b9767-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="b9767-113">To this state:</span></span>  <br/> |<span data-ttu-id="b9767-114">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="b9767-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b9767-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="b9767-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b9767-116">Ein Client, der von einem Zustand in einen anderen wechselt, muss schließlich aus dem letzteren zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="b9767-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b9767-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9767-117">Description</span></span>

<span data-ttu-id="b9767-118">Dieser Status initiiert das Herunterladen einer Strukturhierarchie von Ordnern von einem Server in den lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="b9767-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="b9767-119">Outlook initialisiert die zugeordnete **DNHIER** -Datenstruktur mit einem Zeiger auf die Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="b9767-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="b9767-120">Der Client lädt die Hierarchie herunter und fügt neue Ordner oder Änderungen an Ordnern im lokalen Speicher ein.</span><span class="sxs-lookup"><span data-stu-id="b9767-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="b9767-121">Der Downloadprozess übernimmt Microsoft Exchange die inkrementelle Änderungs Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="b9767-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b9767-122">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9767-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="b9767-123">Wenn dieser Zustand endet, kehrt der lokale Speicher zum Synchronize-Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="b9767-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9767-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9767-124">See also</span></span>



[<span data-ttu-id="b9767-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="b9767-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b9767-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="b9767-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b9767-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b9767-127">SYNCSTATE</span></span>](syncstate.md)


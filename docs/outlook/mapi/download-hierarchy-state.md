---
title: Hierarchiestatus herunterladen
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
# <a name="download-hierarchy-state"></a><span data-ttu-id="40cb6-103">Hierarchiestatus herunterladen</span><span class="sxs-lookup"><span data-stu-id="40cb6-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="40cb6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40cb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="40cb6-105">In diesem Thema wird beschrieben, was während des Status der Downloadhierarchie des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="40cb6-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="40cb6-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="40cb6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40cb6-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="40cb6-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="40cb6-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="40cb6-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="40cb6-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="40cb6-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="40cb6-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="40cb6-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="40cb6-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="40cb6-111">From this state:</span></span>  <br/> |[<span data-ttu-id="40cb6-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="40cb6-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="40cb6-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="40cb6-113">To this state:</span></span>  <br/> |<span data-ttu-id="40cb6-114">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="40cb6-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="40cb6-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="40cb6-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="40cb6-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="40cb6-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="40cb6-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40cb6-117">Description</span></span>

<span data-ttu-id="40cb6-118">Dieser Zustand initiiert das Herunterladen einer Strukturhierarchie von Ordnern von einem Server in den lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="40cb6-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="40cb6-119">Outlook initialisiert die zugeordnete **DNHIER-Datenstruktur** mit einem Zeiger auf die Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="40cb6-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="40cb6-120">Der Client lädt die Hierarchie herunter und fügt neue Ordner oder Änderungen an Ordnern im lokalen Speicher ein.</span><span class="sxs-lookup"><span data-stu-id="40cb6-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="40cb6-121">Der Downloadprozess übernimmt microsoft Exchange Incremental Change Synchronization (ICS).</span><span class="sxs-lookup"><span data-stu-id="40cb6-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="40cb6-122">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="40cb6-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="40cb6-123">Wenn dieser Status endet, kehrt der lokale Speicher in den Synchronisierungsstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="40cb6-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40cb6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40cb6-124">See also</span></span>



[<span data-ttu-id="40cb6-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="40cb6-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="40cb6-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="40cb6-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="40cb6-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="40cb6-127">SYNCSTATE</span></span>](syncstate.md)


---
title: Leerlaufzustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419478"
---
# <a name="idle-state"></a><span data-ttu-id="9e058-103">Leerlaufzustand</span><span class="sxs-lookup"><span data-stu-id="9e058-103">Idle State</span></span>

  
  
<span data-ttu-id="9e058-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9e058-105">In diesem Thema wird beschrieben, was während des Leerlaufzustands des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="9e058-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9e058-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9e058-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e058-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="9e058-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9e058-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="9e058-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="9e058-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="9e058-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="9e058-110">*Keine*</span><span class="sxs-lookup"><span data-stu-id="9e058-110">*None*</span></span>  <br/> |
|<span data-ttu-id="9e058-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="9e058-111">From this state:</span></span>  <br/> | <span data-ttu-id="9e058-112">*Nicht zutreffend*</span><span class="sxs-lookup"><span data-stu-id="9e058-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="9e058-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="9e058-113">To this state:</span></span>  <br/> |[<span data-ttu-id="9e058-114">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="9e058-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="9e058-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="9e058-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9e058-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="9e058-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9e058-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e058-117">Description</span></span>

<span data-ttu-id="9e058-118">In diesem Zustand geschieht nichts.</span><span class="sxs-lookup"><span data-stu-id="9e058-118">Nothing happens in this state.</span></span> <span data-ttu-id="9e058-119">Ein lokaler Speicher befindet sich in diesem Zustand, bevor die Replikation initiiert wird und nachdem die Replikation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9e058-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9e058-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e058-120">See also</span></span>



[<span data-ttu-id="9e058-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="9e058-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9e058-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9e058-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9e058-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="9e058-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9e058-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9e058-124">SYNCSTATE</span></span>](syncstate.md)


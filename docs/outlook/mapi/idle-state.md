---
title: Leerlauf
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792040"
---
# <a name="idle-state"></a><span data-ttu-id="c0b3b-103">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="c0b3b-103">Idle State</span></span>

  
  
<span data-ttu-id="c0b3b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0b3b-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="c0b3b-105">In diesem Thema wird beschrieben, was geschieht, während die Leerlauf des Computers Zustand Replikation.</span><span class="sxs-lookup"><span data-stu-id="c0b3b-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c0b3b-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c0b3b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0b3b-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="c0b3b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c0b3b-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="c0b3b-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="c0b3b-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="c0b3b-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="c0b3b-110">*None*</span><span class="sxs-lookup"><span data-stu-id="c0b3b-110">*None*</span></span>  <br/> |
|<span data-ttu-id="c0b3b-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="c0b3b-111">From this state:</span></span>  <br/> | <span data-ttu-id="c0b3b-112">*Nicht zutreffend*</span><span class="sxs-lookup"><span data-stu-id="c0b3b-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="c0b3b-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="c0b3b-113">To this state:</span></span>  <br/> |[<span data-ttu-id="c0b3b-114">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="c0b3b-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="c0b3b-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="c0b3b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c0b3b-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c0b3b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c0b3b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0b3b-117">Description</span></span>

<span data-ttu-id="c0b3b-118">In diesem Status ohne Wirkung.</span><span class="sxs-lookup"><span data-stu-id="c0b3b-118">Nothing happens in this state.</span></span> <span data-ttu-id="c0b3b-119">Ein lokales Speichers wird in diesem Status vor Replikation ausgeführt werden und nach dem Replikation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c0b3b-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0b3b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b3b-120">See also</span></span>



[<span data-ttu-id="c0b3b-121">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="c0b3b-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c0b3b-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c0b3b-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c0b3b-123">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="c0b3b-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c0b3b-124">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="c0b3b-124">SYNCSTATE</span></span>](syncstate.md)


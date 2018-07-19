---
title: Status „Leerlauf“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792040"
---
# <a name="idle-state"></a><span data-ttu-id="61d55-103">Status „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="61d55-103">Idle State</span></span>

  
  
<span data-ttu-id="61d55-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61d55-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="61d55-105">In diesem Thema wird beschrieben, was geschieht, während die Leerlauf des Computers Zustand Replikation.</span><span class="sxs-lookup"><span data-stu-id="61d55-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="61d55-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="61d55-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61d55-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="61d55-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="61d55-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="61d55-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="61d55-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="61d55-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="61d55-110">*None*</span><span class="sxs-lookup"><span data-stu-id="61d55-110">*None*</span></span>  <br/> |
|<span data-ttu-id="61d55-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="61d55-111">From this state:</span></span>  <br/> | <span data-ttu-id="61d55-112">*Nicht zutreffend*</span><span class="sxs-lookup"><span data-stu-id="61d55-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="61d55-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="61d55-113">To this state:</span></span>  <br/> |[<span data-ttu-id="61d55-114">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="61d55-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="61d55-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="61d55-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="61d55-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="61d55-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="61d55-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61d55-117">Description</span></span>

<span data-ttu-id="61d55-118">In diesem Status ohne Wirkung.</span><span class="sxs-lookup"><span data-stu-id="61d55-118">Nothing happens in this state.</span></span> <span data-ttu-id="61d55-119">Ein lokales Speichers wird in diesem Status vor Replikation ausgeführt werden und nach dem Replikation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="61d55-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61d55-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61d55-120">See also</span></span>



[<span data-ttu-id="61d55-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="61d55-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="61d55-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="61d55-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="61d55-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="61d55-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="61d55-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="61d55-124">SYNCSTATE</span></span>](syncstate.md)


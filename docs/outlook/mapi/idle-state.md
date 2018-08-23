---
title: Status „Leerlauf“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591800"
---
# <a name="idle-state"></a><span data-ttu-id="71556-103">Status „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="71556-103">Idle State</span></span>

  
  
<span data-ttu-id="71556-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71556-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="71556-105">In diesem Thema wird beschrieben, was geschieht, während die Leerlauf des Computers Zustand Replikation.</span><span class="sxs-lookup"><span data-stu-id="71556-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="71556-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="71556-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71556-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="71556-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="71556-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="71556-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="71556-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="71556-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="71556-110">*None*</span><span class="sxs-lookup"><span data-stu-id="71556-110">*None*</span></span>  <br/> |
|<span data-ttu-id="71556-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="71556-111">From this state:</span></span>  <br/> | <span data-ttu-id="71556-112">*Nicht zutreffend*</span><span class="sxs-lookup"><span data-stu-id="71556-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="71556-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="71556-113">To this state:</span></span>  <br/> |[<span data-ttu-id="71556-114">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="71556-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="71556-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="71556-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="71556-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="71556-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="71556-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71556-117">Description</span></span>

<span data-ttu-id="71556-118">In diesem Status ohne Wirkung.</span><span class="sxs-lookup"><span data-stu-id="71556-118">Nothing happens in this state.</span></span> <span data-ttu-id="71556-119">Ein lokales Speichers wird in diesem Status vor Replikation ausgeführt werden und nach dem Replikation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="71556-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71556-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71556-120">See also</span></span>



[<span data-ttu-id="71556-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="71556-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="71556-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="71556-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="71556-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="71556-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="71556-124">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="71556-124">SYNCSTATE</span></span>](syncstate.md)


---
title: Status „Downloadtabelle“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791596"
---
# <a name="download-table-state"></a><span data-ttu-id="eb17e-103">Status „Downloadtabelle“</span><span class="sxs-lookup"><span data-stu-id="eb17e-103">Download Table State</span></span>

  
  
<span data-ttu-id="eb17e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb17e-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="eb17e-105">In diesem Thema wird beschrieben, während der Tabelle Downloadstatus von der Replikation Zustandsautomat erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb17e-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="eb17e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="eb17e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb17e-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="eb17e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="eb17e-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="eb17e-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="eb17e-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="eb17e-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="eb17e-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="eb17e-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="eb17e-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="eb17e-111">From this state:</span></span>  <br/> |[<span data-ttu-id="eb17e-112">Synchronisieren von Inhalt Zustand</span><span class="sxs-lookup"><span data-stu-id="eb17e-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="eb17e-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="eb17e-113">To this state:</span></span>  <br/> |<span data-ttu-id="eb17e-114">Synchronisieren von Inhalt Zustand</span><span class="sxs-lookup"><span data-stu-id="eb17e-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="eb17e-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="eb17e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="eb17e-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb17e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="eb17e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb17e-117">Description</span></span>

<span data-ttu-id="eb17e-118">Dieser Status wird initiiert, einen Ordner herunterladen.</span><span class="sxs-lookup"><span data-stu-id="eb17e-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="eb17e-119">Während dieser Zustand initialisiert Outlook die zugeordnete **DNTBL** -Datenstruktur mit Informationen zu den Ordner.</span><span class="sxs-lookup"><span data-stu-id="eb17e-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="eb17e-120">Der Client den Ordnerinhalt downloads und aktualisiert den Ordner auf dem lokalen Speicher mit neuen Inhalt, geändert oder vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="eb17e-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="eb17e-121">Der Downloadvorgang nimmt Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="eb17e-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="eb17e-122">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb17e-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="eb17e-123">Wenn dieser Status beendet ist, gibt der lokale Speicher auf den Status der Synchronize-Inhalt zurück.</span><span class="sxs-lookup"><span data-stu-id="eb17e-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb17e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb17e-124">See also</span></span>



[<span data-ttu-id="eb17e-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="eb17e-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="eb17e-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="eb17e-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="eb17e-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="eb17e-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="eb17e-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="eb17e-128">SYNCSTATE</span></span>](syncstate.md)


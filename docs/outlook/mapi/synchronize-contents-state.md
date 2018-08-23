---
title: Status „Inhalts synchronisieren“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2bdbeb39cce1e62569f364875c3828cdd530c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577247"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="3d146-103">Status „Inhalts synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="3d146-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="3d146-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d146-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3d146-105">In diesem Thema wird beschrieben, was geschieht, während die Synchronize Inhalt Zustand des Computers Zustand Replikation.</span><span class="sxs-lookup"><span data-stu-id="3d146-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3d146-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="3d146-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d146-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="3d146-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3d146-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="3d146-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="3d146-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="3d146-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3d146-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="3d146-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="3d146-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="3d146-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3d146-112">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="3d146-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="3d146-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="3d146-113">To this state:</span></span>  <br/> |<span data-ttu-id="3d146-114">[Tabelle Zustand herunterladen](download-table-state.md), [Hochladen Tabelle Zustand](upload-table-state.md), oder Zustand synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3d146-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3d146-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="3d146-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3d146-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3d146-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3d146-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d146-117">Description</span></span>

<span data-ttu-id="3d146-118">Dieser Status wird initiiert einen der beiden Replikationsprozesse: Hochladen der Inhalt der Ordner auf einem lokalen Speicher oder eine vollständige Synchronisierung angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d146-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="3d146-119">In eine vollständige Synchronisierung, für die einzelnen von den angegebenen Ordnern Inhalt zuerst hochgeladen und dann heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3d146-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="3d146-120">Synchronisieren je nach den *UlFlags* legen Sie in der entsprechenden **[SYNC](sync.md)** -Struktur in der vorherigen Zustand, Outlook initialisiert [out] Member in der Struktur **SYNCCONT** um Informationen zu den Inhalt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3d146-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="3d146-121">Über die gleiche **SYNCCONT** -Struktur erhält der Client die Anzahl der Ordner, die Inhalt besitzen, hoch- oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3d146-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="3d146-122">Der Client wird jeder dieser Ordner durchlaufen werden durch den lokalen Speicher auf den Status des Upload-Tabelle einen Ordner hochladen verschieben oder verschieben den lokalen Speicher in den Downloadstatus Tabelle, um den Ordner herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="3d146-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="3d146-123">Darüber hinaus erhält der Client Eintrags-IDs für die Ordner Replikation erfordern.</span><span class="sxs-lookup"><span data-stu-id="3d146-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="3d146-124">Wenn dieser Status beendet wird, bereinigt Outlook internen Informationen.</span><span class="sxs-lookup"><span data-stu-id="3d146-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="3d146-125">Der lokale Speicher zurück in den Synchronize-Zustand.</span><span class="sxs-lookup"><span data-stu-id="3d146-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3d146-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d146-126">See also</span></span>



[<span data-ttu-id="3d146-127">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="3d146-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3d146-128">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3d146-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3d146-129">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="3d146-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3d146-130">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="3d146-130">SYNCSTATE</span></span>](syncstate.md)


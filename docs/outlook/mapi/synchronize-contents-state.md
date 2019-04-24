---
title: Synchronisieren des Inhaltsstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349567"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="4fb54-103">Synchronisieren des Inhaltsstatus</span><span class="sxs-lookup"><span data-stu-id="4fb54-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="4fb54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fb54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4fb54-105">In diesem Thema wird beschrieben, was während des Status "Inhalt synchronisieren" des Replikationsstatus Computers geschieht.</span><span class="sxs-lookup"><span data-stu-id="4fb54-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4fb54-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4fb54-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fb54-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="4fb54-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4fb54-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="4fb54-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="4fb54-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="4fb54-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4fb54-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="4fb54-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="4fb54-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="4fb54-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4fb54-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="4fb54-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="4fb54-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="4fb54-113">To this state:</span></span>  <br/> |<span data-ttu-id="4fb54-114">[Tabellenstatus herunterladen](download-table-state.md), [Tabellenstatus hochladen](upload-table-state.md)oder Status Synchronisieren</span><span class="sxs-lookup"><span data-stu-id="4fb54-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4fb54-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="4fb54-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4fb54-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="4fb54-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4fb54-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fb54-117">Description</span></span>

<span data-ttu-id="4fb54-118">Dieser Status initiiert einen der beiden Replikationsprozesse: Hochladen der Inhalte bestimmter Ordner in einem lokalen Speicher oder eine vollständige Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="4fb54-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="4fb54-119">Bei einer vollständigen Synchronisierung für jeden der angegebenen Ordner werden die Inhalte zuerst hochgeladen und dann heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="4fb54-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="4fb54-120">Abhängig vom *ulFlags* -Satz in der entsprechenden **[Synchronisierungs](sync.md)** Struktur im vorherigen Synchronisierungsstatus initialisiert Outlook [out]-Elemente in der **SYNCCONT** -Struktur, um Informationen zu den Inhalten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4fb54-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="4fb54-121">Über dieselbe **SYNCCONT** -Struktur ruft der Client die Anzahl der Ordner ab, die Inhalte hoch-oder heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4fb54-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="4fb54-122">Der Client durchläuft jeden dieser Ordner, indem er den lokalen Speicher in den Status der hochgeladenen Tabelle verschiebt, um einen Ordner hochzuladen, oder den lokalen Speicher in den Status der Download Tabelle verschiebt, um den Ordner herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4fb54-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="4fb54-123">Darüber hinaus erhält der Client Eintrags-IDs für die Ordner, die eine Replikation erfordern.</span><span class="sxs-lookup"><span data-stu-id="4fb54-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="4fb54-124">Wenn dieser Status endet, bereinigt Outlook seine internen Informationen.</span><span class="sxs-lookup"><span data-stu-id="4fb54-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="4fb54-125">Der lokale Speicher wird zum Synchronisierungsstatus zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4fb54-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fb54-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fb54-126">See also</span></span>



[<span data-ttu-id="4fb54-127">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4fb54-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4fb54-128">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4fb54-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4fb54-129">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4fb54-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4fb54-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4fb54-130">SYNCSTATE</span></span>](syncstate.md)


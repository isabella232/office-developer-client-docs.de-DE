---
title: Status "Inhalt synchronisieren"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438470"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="c2138-103">Status "Inhalt synchronisieren"</span><span class="sxs-lookup"><span data-stu-id="c2138-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="c2138-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c2138-105">In diesem Thema wird beschrieben, was während des Synchronisierungsinhaltsstatus des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="c2138-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c2138-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c2138-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2138-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="c2138-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c2138-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="c2138-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="c2138-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="c2138-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="c2138-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="c2138-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="c2138-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="c2138-111">From this state:</span></span>  <br/> |[<span data-ttu-id="c2138-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="c2138-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="c2138-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="c2138-113">To this state:</span></span>  <br/> |<span data-ttu-id="c2138-114">[Tabellenstatus herunterladen,](download-table-state.md) [Tabellenstatus hochladen](upload-table-state.md)oder Synchronisieren</span><span class="sxs-lookup"><span data-stu-id="c2138-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c2138-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="c2138-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c2138-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="c2138-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c2138-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2138-117">Description</span></span>

<span data-ttu-id="c2138-118">Dieser Zustand initiiert einen der beiden Replikationsprozesse: Das Hochladen des Inhalts der angegebenen Ordner in einem lokalen Speicher oder eine vollständige Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="c2138-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="c2138-119">Bei einer vollständigen Synchronisierung werden die Inhalte für jeden der angegebenen Ordner zuerst hochgeladen und dann heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="c2138-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="c2138-120">Abhängig von *den ulFlags,* die in der entsprechenden **[SYNC-Struktur](sync.md)** im vorherigen Synchronisierungsstatus festgelegt sind, initialisiert Outlook [out]-Elemente in der **SYNCCONT-Struktur,** um Informationen zu den Inhalten zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="c2138-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="c2138-121">Über die gleiche **SYNCCONT-Struktur** ruft der Client die Anzahl der Ordner ab, für die Inhalte hochgeladen oder heruntergeladen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c2138-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="c2138-122">Der Client durchrundet jeden dieser Ordner, indem er den lokalen Speicher in den Status der Uploadtabelle zum Hochladen eines Ordners oder den lokalen Speicher in den Zustand der Downloadtabelle verschieben, um den Ordner herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="c2138-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="c2138-123">Darüber hinaus ruft der Client Eintrags-IDs für die Ordner ab, die eine Replikation erfordern.</span><span class="sxs-lookup"><span data-stu-id="c2138-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="c2138-124">Wenn dieser Zustand endet, Outlook interne Informationen bereinigt.</span><span class="sxs-lookup"><span data-stu-id="c2138-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="c2138-125">Der lokale Speicher kehrt zum Synchronisierungsstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="c2138-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2138-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2138-126">See also</span></span>



[<span data-ttu-id="c2138-127">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="c2138-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c2138-128">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c2138-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c2138-129">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="c2138-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c2138-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="c2138-130">SYNCSTATE</span></span>](syncstate.md)


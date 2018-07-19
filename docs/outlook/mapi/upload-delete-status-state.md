---
title: Status „Status der Upload-Löschung“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795803"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="4ccf9-103">Status „Status der Upload-Löschung“</span><span class="sxs-lookup"><span data-stu-id="4ccf9-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="4ccf9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ccf9-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="4ccf9-105">In diesem Thema wird beschrieben, was geschieht, während der Upload löschen Status Zustand der Replikation Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4ccf9-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4ccf9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ccf9-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="4ccf9-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4ccf9-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="4ccf9-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="4ccf9-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="4ccf9-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4ccf9-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="4ccf9-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="4ccf9-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="4ccf9-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4ccf9-112">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="4ccf9-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4ccf9-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="4ccf9-113">To this state:</span></span>  <br/> |<span data-ttu-id="4ccf9-114">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="4ccf9-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4ccf9-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4ccf9-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4ccf9-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ccf9-117">Description</span></span>

<span data-ttu-id="4ccf9-118">Dieser Status wird initiiert, auf einem Server aktualisieren, die Outlook-Elemente (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), die in einem Ordner in einem lokalen Speicher angegeben, die in den vorstehenden Upload-Tabelle gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="4ccf9-119">Während dieser Zustand initialisiert Outlook Elemente in der zugeordneten **UPDEL** Datenstruktur mit Informationen für die Elemente, die aus dem Ordner verschoben oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="4ccf9-120">Der Client löscht die angegebenen Elemente im Ordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="4ccf9-121">Um Elemente zu unterscheiden, die verschoben wurden, im Gegensatz zu müssen gelöscht wurden, muss der Client die *Pupmov* Member in der Struktur **UPDEL** identifiziert überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="4ccf9-122">Wenn dieser Status beendet ist, löscht Outlook die interne Informationen zurück, der angibt, dass das Element gelöscht wurde. Daher müssen Outlook nicht mehr einen Datensatz des Elements.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="4ccf9-123">Auf den Upload Tabelle Status gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="4ccf9-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ccf9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ccf9-124">See also</span></span>



[<span data-ttu-id="4ccf9-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4ccf9-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4ccf9-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4ccf9-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4ccf9-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4ccf9-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4ccf9-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4ccf9-128">SYNCSTATE</span></span>](syncstate.md)


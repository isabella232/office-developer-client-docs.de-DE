---
title: Hochladen Statusstatus löschen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425841"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="4efc7-103">Hochladen Statusstatus löschen</span><span class="sxs-lookup"><span data-stu-id="4efc7-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="4efc7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4efc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4efc7-105">In diesem Thema wird beschrieben, was während des Statusstatus zum Löschen des Uploads des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="4efc7-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4efc7-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4efc7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4efc7-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="4efc7-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4efc7-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="4efc7-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="4efc7-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="4efc7-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4efc7-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="4efc7-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="4efc7-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="4efc7-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4efc7-112">Hochladen Tabellenstatus</span><span class="sxs-lookup"><span data-stu-id="4efc7-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4efc7-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="4efc7-113">To this state:</span></span>  <br/> |<span data-ttu-id="4efc7-114">Hochladen Tabellenstatus</span><span class="sxs-lookup"><span data-stu-id="4efc7-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4efc7-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="4efc7-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4efc7-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="4efc7-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4efc7-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4efc7-117">Description</span></span>

<span data-ttu-id="4efc7-118">Dieser Status initiiert die Aktualisierung auf einem Server, der Outlook Elemente (E-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal) enthält, die in einem Ordner in einem lokalen Speicher gelöscht wurden, der in einem vorherigen Uploadtabelle-Status angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4efc7-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="4efc7-119">Während dieses Status initialisiert Outlook Mitglieder in der zugeordneten **UPDEL-Datenstruktur** mit Informationen für die Elemente, die gelöscht oder aus dem Ordner verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="4efc7-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="4efc7-120">Der Client löscht dann die angegebenen Elemente im Ordner auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="4efc7-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="4efc7-121">Um elemente zu unterscheiden, die verschoben wurden und nicht gelöscht wurden, muss der Client die  *pupmov-Mitglieder*  überprüfen, die in der **UPDEL-Struktur identifiziert** wurden.</span><span class="sxs-lookup"><span data-stu-id="4efc7-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="4efc7-122">Wenn dieser Status endet, Outlook die internen Informationen gelöscht, die angeben, dass das Element gelöscht wurde. folglich Outlook nicht mehr über einen Datensatz des Elements verfügen.</span><span class="sxs-lookup"><span data-stu-id="4efc7-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="4efc7-123">Der lokale Speicher kehrt zum Status der Uploadtabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4efc7-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4efc7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4efc7-124">See also</span></span>



[<span data-ttu-id="4efc7-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4efc7-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4efc7-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4efc7-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4efc7-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4efc7-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4efc7-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4efc7-128">SYNCSTATE</span></span>](syncstate.md)


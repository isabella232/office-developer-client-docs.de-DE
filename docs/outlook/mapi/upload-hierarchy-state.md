---
title: Hierarchie Status hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415425"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="36b05-103">Hierarchie Status hochladen</span><span class="sxs-lookup"><span data-stu-id="36b05-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="36b05-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36b05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="36b05-105">In diesem Thema wird beschrieben, was während des Upload-Hierarchie Status des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="36b05-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="36b05-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="36b05-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36b05-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="36b05-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="36b05-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="36b05-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="36b05-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="36b05-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="36b05-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="36b05-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="36b05-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="36b05-111">From this state:</span></span>  <br/> |[<span data-ttu-id="36b05-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="36b05-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="36b05-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="36b05-113">To this state:</span></span>  <br/> |<span data-ttu-id="36b05-114">[Ordner Status hochladen](upload-folder-state.md)oder Status Synchronisieren</span><span class="sxs-lookup"><span data-stu-id="36b05-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="36b05-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="36b05-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="36b05-116">Ein Client, der einen Status zu einem anderen abgibt, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="36b05-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="36b05-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36b05-117">Description</span></span>

<span data-ttu-id="36b05-118">Dieser Status initiiert das Hochladen einer Ordnerstruktur Hierarchie, die in einem vorhergehenden Synchronisierungsstatus angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="36b05-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="36b05-119">Outlook bestimmt die Anzahl der Ordner, die in dieser Hierarchie erstellt oder geändert wurden, und initialisiert *cEnt* in uphere. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="36b05-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="36b05-120">In Outlook wird auch die Anzahl der hochgeladenen Ordner mit einem anderen Mitglieds *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="36b05-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="36b05-121">Um jeden *cEnt* -Ordner hochzuladen, verschiebt der Client den lokalen Speicher in den Upload-Ordner Status und kehrt zum Upload-Hierarchie Status zurück, wenn der Ordner Upload abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="36b05-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="36b05-122">Wenn der Upload-Hierarchie Status endet, wird der lokale Speicher zum Synchronize-Status zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="36b05-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36b05-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36b05-123">See also</span></span>



[<span data-ttu-id="36b05-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="36b05-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="36b05-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="36b05-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="36b05-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="36b05-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="36b05-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="36b05-127">SYNCSTATE</span></span>](syncstate.md)


---
title: Hochladen Hierarchiestatus
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
# <a name="upload-hierarchy-state"></a><span data-ttu-id="12fe9-103">Hochladen Hierarchiestatus</span><span class="sxs-lookup"><span data-stu-id="12fe9-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="12fe9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12fe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="12fe9-105">In diesem Thema wird beschrieben, was während des Uploadhierarchiestatus des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="12fe9-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="12fe9-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="12fe9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12fe9-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="12fe9-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="12fe9-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="12fe9-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="12fe9-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="12fe9-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="12fe9-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="12fe9-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="12fe9-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="12fe9-111">From this state:</span></span>  <br/> |[<span data-ttu-id="12fe9-112">Zustand „Synchronisieren“</span><span class="sxs-lookup"><span data-stu-id="12fe9-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="12fe9-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="12fe9-113">To this state:</span></span>  <br/> |<span data-ttu-id="12fe9-114">[Hochladen Ordnerstatus](upload-folder-state.md)oder Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="12fe9-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="12fe9-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="12fe9-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="12fe9-116">Ein Client, der einen Zustand in einen anderen verlässt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="12fe9-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="12fe9-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12fe9-117">Description</span></span>

<span data-ttu-id="12fe9-118">Dieser Zustand initiiert das Hochladen einer Ordnerstrukturhierarchie, die in einem vorherigen Synchronisierungsstatus angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="12fe9-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="12fe9-119">Outlook bestimmt die Anzahl der Ordner, die in dieser Hierarchie erstellt oder geändert wurden, und initialisiert *cEnt* in **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="12fe9-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="12fe9-120">Outlook behält auch die Anzahl der hochgeladenen Ordner mit einem anderen Mitglied *iEnt bei.*</span><span class="sxs-lookup"><span data-stu-id="12fe9-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="12fe9-121">Um jeden der  *cEnt-Ordner*  hochzuladen, verschiebt der Client den lokalen Speicher in den Uploadordnerstatus und kehrt zum Status der Uploadhierarchie zurück, wenn der Ordnerupload abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="12fe9-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="12fe9-122">Wenn der Uploadhierarchiestatus endet, kehrt der lokale Speicher in den Synchronisierungsstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="12fe9-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12fe9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12fe9-123">See also</span></span>



[<span data-ttu-id="12fe9-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="12fe9-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="12fe9-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="12fe9-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="12fe9-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="12fe9-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="12fe9-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="12fe9-127">SYNCSTATE</span></span>](syncstate.md)


---
title: Status „Uploadhierarchie“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572186"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="b28cb-103">Status „Uploadhierarchie“</span><span class="sxs-lookup"><span data-stu-id="b28cb-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="b28cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b28cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b28cb-105">In diesem Thema wird beschrieben, was geschieht, während die Hierarchie Zustand der Replikation Zustandsautomat hochladen.</span><span class="sxs-lookup"><span data-stu-id="b28cb-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b28cb-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b28cb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b28cb-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="b28cb-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b28cb-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="b28cb-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="b28cb-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="b28cb-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b28cb-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="b28cb-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="b28cb-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="b28cb-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b28cb-112">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="b28cb-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="b28cb-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="b28cb-113">To this state:</span></span>  <br/> |<span data-ttu-id="b28cb-114">[Hochladen der Ordner Zustand](upload-folder-state.md), oder Zustand synchronisieren</span><span class="sxs-lookup"><span data-stu-id="b28cb-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b28cb-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="b28cb-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b28cb-116">Ein Client, der einem Zustand zu einem anderen ausgehenden muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b28cb-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b28cb-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b28cb-117">Description</span></span>

<span data-ttu-id="b28cb-118">Dieser Status Hochladen einer Struktur Ordnerhierarchie, die in einem vorherigen angegeben wurde initiiert synchronisieren Zustand.</span><span class="sxs-lookup"><span data-stu-id="b28cb-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="b28cb-119">Outlook bestimmt die Anzahl der Ordner, in denen, die in dieser Hierarchie und initialisiert *cEnt* in **UPHIER**geändert oder erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b28cb-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="b28cb-120">Outlook zählt auch die Anzahl der hochgeladenen Ordnern mit einem anderen Element *iEnt* an.</span><span class="sxs-lookup"><span data-stu-id="b28cb-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="b28cb-121">Um jeden Ordner *cEnt* hochzuladen, verschiebt der Client den lokalen Speicher in den Ordner hochladen Zustand, auf den Upload Hierarchie Status zurückgeben, wenn der Ordner Hochladevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b28cb-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="b28cb-122">Nach Ende der Upload Hierarchie Zustand gibt der lokale Speicher auf den Status synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b28cb-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b28cb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b28cb-123">See also</span></span>



[<span data-ttu-id="b28cb-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="b28cb-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b28cb-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b28cb-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b28cb-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="b28cb-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b28cb-127">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="b28cb-127">SYNCSTATE</span></span>](syncstate.md)


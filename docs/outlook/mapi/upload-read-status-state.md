---
title: Upload lesen Status Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795806"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="f6dcb-103">Upload lesen Status Zustand</span><span class="sxs-lookup"><span data-stu-id="f6dcb-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="f6dcb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6dcb-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f6dcb-105">In diesem Thema wird beschrieben, was geschieht, während der Upload Status Zustand des Computers Zustand Replikation lesen.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f6dcb-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f6dcb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6dcb-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="f6dcb-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="f6dcb-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="f6dcb-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="f6dcb-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="f6dcb-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="f6dcb-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="f6dcb-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="f6dcb-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="f6dcb-111">From this state:</span></span>  <br/> |[<span data-ttu-id="f6dcb-112">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="f6dcb-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="f6dcb-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="f6dcb-113">To this state:</span></span>  <br/> |<span data-ttu-id="f6dcb-114">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="f6dcb-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="f6dcb-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="f6dcb-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="f6dcb-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6dcb-117">Description</span></span>

<span data-ttu-id="f6dcb-118">Dieser Status wird initiiert, Hochladen des Status Lesen von Elementen in einem Ordner, in den vorstehenden Upload-Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="f6dcb-119">Während dieser Zustand initialisiert Outlook die zugeordnete **UPREAD** -Datenstruktur mit Informationen für diese Elemente im Ordner, deren Status Lesen geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="f6dcb-120">Der Client aktualisiert anschließend den lesen Status dieser Elemente auf dem Server als gelesen oder ungelesen.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="f6dcb-121">Wenn dieser Status beendet ist, löscht Outlook die interne Informationen über das Element gelesen-Status, verhindert, dass das Element gelesen-Status wird erneut hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="f6dcb-122">Auf den Upload Tabelle Status gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="f6dcb-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6dcb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6dcb-123">See also</span></span>



[<span data-ttu-id="f6dcb-124">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="f6dcb-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f6dcb-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f6dcb-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f6dcb-126">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="f6dcb-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f6dcb-127">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="f6dcb-127">SYNCSTATE</span></span>](syncstate.md)


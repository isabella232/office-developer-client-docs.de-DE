---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418337"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="8bcf5-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bcf5-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="8bcf5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bcf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bcf5-105">Übergibt den Speicheranbieter während eines Aufrufs von [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md)als Feld in der MAPISIB-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8bcf5-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="8bcf5-106">Der Speicheranbieter verwendet diese Schnittstelle, um Microsoft Feedback Outlook status der Synchronisierung zu geben.</span><span class="sxs-lookup"><span data-stu-id="8bcf5-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bcf5-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8bcf5-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="8bcf5-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="8bcf5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8bcf5-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="8bcf5-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="8bcf5-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8bcf5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8bcf5-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="8bcf5-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="8bcf5-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8bcf5-112">Called by:</span></span>  <br/> |<span data-ttu-id="8bcf5-113">Store Anbieter</span><span class="sxs-lookup"><span data-stu-id="8bcf5-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="8bcf5-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8bcf5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8bcf5-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="8bcf5-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8bcf5-116">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8bcf5-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8bcf5-117">Progress</span><span class="sxs-lookup"><span data-stu-id="8bcf5-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="8bcf5-118">Der Speicheranbieter ruft diese Funktion regelmäßig auf, um den Status im Dialogfeld Senden/Empfangen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8bcf5-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8bcf5-119">Error</span><span class="sxs-lookup"><span data-stu-id="8bcf5-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="8bcf5-120">Wenn während der Synchronisierung Fehler auftreten, ruft der Speicheranbieter diese Funktion auf, um Details zur Verfügung zu stellen, die im Dialogfeld Senden/Empfangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8bcf5-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8bcf5-121">Done</span><span class="sxs-lookup"><span data-stu-id="8bcf5-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="8bcf5-122">Der Speicheranbieter ruft diese Funktion auf, um Outlook Synchronisierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="8bcf5-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8bcf5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bcf5-123">See also</span></span>



[<span data-ttu-id="8bcf5-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bcf5-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="8bcf5-125">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bcf5-125">MAPI Interfaces</span></span>](mapi-interfaces.md)


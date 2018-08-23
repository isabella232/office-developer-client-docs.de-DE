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
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593711"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="72e70-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72e70-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="72e70-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72e70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72e70-105">Übergibt Speicheranbieter als Feld auf der Struktur MAPISIB während eines Anrufs auf [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="72e70-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="72e70-106">Der Anbieter verwendet diese Schnittstelle ihr Feedback an Microsoft Outlook über den Status der Synchronisierung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="72e70-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72e70-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="72e70-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="72e70-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="72e70-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="72e70-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="72e70-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="72e70-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="72e70-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="72e70-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="72e70-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="72e70-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="72e70-112">Called by:</span></span>  <br/> |<span data-ttu-id="72e70-113">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="72e70-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="72e70-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="72e70-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="72e70-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="72e70-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="72e70-116">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="72e70-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="72e70-117">Progress</span><span class="sxs-lookup"><span data-stu-id="72e70-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="72e70-118">Speicheranbieter ruft in regelmäßigen Abständen diese Funktion zum Aktualisieren des Status im Dialogfeld senden/empfangen.</span><span class="sxs-lookup"><span data-stu-id="72e70-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="72e70-119">Fehler</span><span class="sxs-lookup"><span data-stu-id="72e70-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="72e70-120">Wenn während der Synchronisierung Fehler auftreten, ruft der Anbieter diese Funktion, um Details bereitstellen, die im Dialogfeld Senden/Empfangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="72e70-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="72e70-121">Fertig</span><span class="sxs-lookup"><span data-stu-id="72e70-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="72e70-122">Speicheranbieter ruft diese Funktion, um Outlook zu informieren, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="72e70-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72e70-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72e70-123">See also</span></span>



[<span data-ttu-id="72e70-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72e70-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="72e70-125">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="72e70-125">MAPI Interfaces</span></span>](mapi-interfaces.md)


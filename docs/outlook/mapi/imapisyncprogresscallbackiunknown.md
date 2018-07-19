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
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792441"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="daa2c-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="daa2c-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="daa2c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="daa2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="daa2c-105">Übergibt Speicheranbieter als Feld auf der Struktur MAPISIB während eines Anrufs auf [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="daa2c-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="daa2c-106">Der Anbieter verwendet diese Schnittstelle ihr Feedback an Microsoft Outlook über den Status der Synchronisierung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="daa2c-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daa2c-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="daa2c-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="daa2c-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="daa2c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="daa2c-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="daa2c-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="daa2c-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="daa2c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="daa2c-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="daa2c-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="daa2c-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="daa2c-112">Called by:</span></span>  <br/> |<span data-ttu-id="daa2c-113">Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="daa2c-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="daa2c-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="daa2c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="daa2c-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="daa2c-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="daa2c-116">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="daa2c-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="daa2c-117">Progress</span><span class="sxs-lookup"><span data-stu-id="daa2c-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="daa2c-118">Speicheranbieter ruft in regelmäßigen Abständen diese Funktion zum Aktualisieren des Status im Dialogfeld senden/empfangen.</span><span class="sxs-lookup"><span data-stu-id="daa2c-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="daa2c-119">Fehler</span><span class="sxs-lookup"><span data-stu-id="daa2c-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="daa2c-120">Wenn während der Synchronisierung Fehler auftreten, ruft der Anbieter diese Funktion, um Details bereitstellen, die im Dialogfeld Senden/Empfangen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="daa2c-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="daa2c-121">Fertig</span><span class="sxs-lookup"><span data-stu-id="daa2c-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="daa2c-122">Speicheranbieter ruft diese Funktion, um Outlook zu informieren, dass die Synchronisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="daa2c-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daa2c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="daa2c-123">See also</span></span>



[<span data-ttu-id="daa2c-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="daa2c-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="daa2c-125">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="daa2c-125">MAPI Interfaces</span></span>](mapi-interfaces.md)


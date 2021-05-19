---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405592"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="21c17-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21c17-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="21c17-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21c17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21c17-105">Stellt einen Mechanismus zum Synchronisieren von E-Mails anstelle der Transport-API bereit.</span><span class="sxs-lookup"><span data-stu-id="21c17-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="21c17-106">Diese Schnittstelle wird für ein Store-Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="21c17-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="21c17-107">Mit dieser Schnittstelle und [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)kann ein Transportanbieter bessere Fortschritts- und Fehlermeldungen bereitstellen als diejenigen, die im Dialogfeld Senden/Empfangen in Microsoft Outlook angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="21c17-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="21c17-108">Der Posteingang befindet sich weiterhin im Standardspeicher.</span><span class="sxs-lookup"><span data-stu-id="21c17-108">The outbox is still in the default store.</span></span> <span data-ttu-id="21c17-109">Outlook verwendet weiterhin die Transport-APIs zum Senden von E-Mails, da die ausgehende Nachricht nicht im externen Speicher gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="21c17-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21c17-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="21c17-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="21c17-111">Speicher- und Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="21c17-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="21c17-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="21c17-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="21c17-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="21c17-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="21c17-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="21c17-114">Called by:</span></span>  <br/> |<span data-ttu-id="21c17-115">Store- und Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="21c17-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="21c17-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="21c17-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="21c17-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="21c17-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="21c17-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="21c17-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="21c17-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="21c17-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="21c17-120">Implementiert von Nachrichtenspeicheranbietern.</span><span class="sxs-lookup"><span data-stu-id="21c17-120">Implemented by message store providers.</span></span> <span data-ttu-id="21c17-121">Diese Methode wird von Outlook 2010 und Outlook 2013 aufgerufen, um die Synchronisierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="21c17-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21c17-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21c17-122">See also</span></span>



[<span data-ttu-id="21c17-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21c17-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="21c17-124">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="21c17-124">MAPI Interfaces</span></span>](mapi-interfaces.md)


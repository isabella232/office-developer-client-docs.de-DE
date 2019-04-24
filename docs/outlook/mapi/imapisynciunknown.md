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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341279"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="eabbd-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eabbd-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="eabbd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eabbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eabbd-105">Stellt einen Mechanismus zum Synchronisieren von e-Mails anstelle der Transport-API bereit.</span><span class="sxs-lookup"><span data-stu-id="eabbd-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="eabbd-106">Diese Schnittstelle wird für ein Store-Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="eabbd-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="eabbd-107">Mithilfe dieser Schnittstelle und [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)kann ein Transportanbieter bessere Fortschritte und Fehlermeldungen als die anzeigen, die im Dialogfeld senden/empfangen in Microsoft Outlook angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="eabbd-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="eabbd-108">Der Postausgang befindet sich noch im Standardspeicher.</span><span class="sxs-lookup"><span data-stu-id="eabbd-108">The outbox is still in the default store.</span></span> <span data-ttu-id="eabbd-109">Outlook verwendet weiterhin die Transport-APIs zum Senden von e-Mails, da sich die ausgehende Nachricht nicht im externen Speicher befinden kann.</span><span class="sxs-lookup"><span data-stu-id="eabbd-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eabbd-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="eabbd-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="eabbd-111">Speicher-und Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="eabbd-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="eabbd-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="eabbd-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="eabbd-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="eabbd-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="eabbd-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="eabbd-114">Called by:</span></span>  <br/> |<span data-ttu-id="eabbd-115">Speicher-und Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="eabbd-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="eabbd-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="eabbd-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eabbd-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="eabbd-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eabbd-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="eabbd-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="eabbd-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="eabbd-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="eabbd-120">Von Nachrichtenspeicher Anbietern implementiert.</span><span class="sxs-lookup"><span data-stu-id="eabbd-120">Implemented by message store providers.</span></span> <span data-ttu-id="eabbd-121">Diese Methode wird von Outlook 2010 und Outlook 2013 aufgerufen, um die Synchronisierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="eabbd-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eabbd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eabbd-122">See also</span></span>



[<span data-ttu-id="eabbd-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eabbd-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="eabbd-124">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="eabbd-124">MAPI Interfaces</span></span>](mapi-interfaces.md)


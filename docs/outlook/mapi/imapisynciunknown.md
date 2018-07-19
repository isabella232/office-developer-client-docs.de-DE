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
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792430"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="a38e5-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a38e5-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="a38e5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a38e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a38e5-105">Bietet einen Mechanismus zum Synchronisieren von e-Mail statt der Transport-API.</span><span class="sxs-lookup"><span data-stu-id="a38e5-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="a38e5-106">Diese Schnittstelle wird auf ein Store-Objekt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a38e5-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="a38e5-107">Mithilfe dieser Schnittstelle und [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), ein Transportdienstes bieten eine bessere Bearbeitung und Fehlermeldungen als die, die im Dialogfeld senden/empfangen in Microsoft Outlook angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a38e5-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="a38e5-108">Im Ordner Postausgang ist noch in der Standard-Informationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="a38e5-108">The outbox is still in the default store.</span></span> <span data-ttu-id="a38e5-109">Outlook wird weiterhin die Transport-APIs verwenden, um e-Mail-Nachrichten senden, da die ausgehende Nachricht im externen Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="a38e5-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a38e5-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="a38e5-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a38e5-111">Anbieter für Speicher und transport</span><span class="sxs-lookup"><span data-stu-id="a38e5-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="a38e5-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a38e5-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a38e5-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="a38e5-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="a38e5-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a38e5-114">Called by:</span></span>  <br/> |<span data-ttu-id="a38e5-115">Anbieter für Speicher und Transport</span><span class="sxs-lookup"><span data-stu-id="a38e5-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="a38e5-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="a38e5-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a38e5-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="a38e5-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a38e5-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="a38e5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a38e5-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="a38e5-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="a38e5-120">Nachricht Zeichenfolgeneigenschaften implementiert.</span><span class="sxs-lookup"><span data-stu-id="a38e5-120">Implemented by message store providers.</span></span> <span data-ttu-id="a38e5-121">Diese Methode wird von Outlook 2010 und Outlook 2013, um die Synchronisierung starten aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a38e5-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a38e5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a38e5-122">See also</span></span>



[<span data-ttu-id="a38e5-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a38e5-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="a38e5-124">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a38e5-124">MAPI Interfaces</span></span>](mapi-interfaces.md)


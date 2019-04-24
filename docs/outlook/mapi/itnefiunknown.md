---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315036"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="505d2-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="505d2-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="505d2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="505d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="505d2-105">Stellt Methoden zum Kapseln von MAPI-Eigenschaften bereit, die von einem Messagingsystem nicht in binäre Streams unterstützt werden, die an Nachrichten angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="505d2-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="505d2-106">Das für diese Kapselung verwendete Format ist das Transport neutrale Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="505d2-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="505d2-107">Der Ziel Transportanbieter oder die MAPI-basierte Clientanwendung kann dann beim Empfang einer Nachricht, die eine TNEF-Anlage enthält, die Eigenschaften aus der Anlage wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="505d2-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="505d2-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="505d2-108">Header file:</span></span>  <br/> |<span data-ttu-id="505d2-109">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="505d2-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="505d2-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="505d2-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="505d2-111">TNEF-Objekte</span><span class="sxs-lookup"><span data-stu-id="505d2-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="505d2-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="505d2-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="505d2-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="505d2-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="505d2-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="505d2-114">Called by:</span></span>  <br/> |<span data-ttu-id="505d2-115">Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways</span><span class="sxs-lookup"><span data-stu-id="505d2-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="505d2-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="505d2-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="505d2-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="505d2-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="505d2-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="505d2-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="505d2-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="505d2-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="505d2-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="505d2-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="505d2-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="505d2-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="505d2-122">Ermöglicht dem aufrufenden Dienstanbieter oder Gateway das Hinzufügen von Eigenschaften zur Kapselung einer Nachricht oder Anlage.</span><span class="sxs-lookup"><span data-stu-id="505d2-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="505d2-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="505d2-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="505d2-124">Extrahiert die Eigenschaften aus einer TNEF-Kapselung.</span><span class="sxs-lookup"><span data-stu-id="505d2-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="505d2-125">Finish</span><span class="sxs-lookup"><span data-stu-id="505d2-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="505d2-126">Die Verarbeitung für alle in der Warteschlange befindlichen TNEF-Vorgänge wird abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="505d2-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="505d2-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="505d2-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="505d2-128">Öffnet eine Stream-Schnittstelle für den Text einer gekapselte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="505d2-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="505d2-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="505d2-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="505d2-130">Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage fest, ohne die ursprüngliche Nachricht oder Anlage zu ändern.</span><span class="sxs-lookup"><span data-stu-id="505d2-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="505d2-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="505d2-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="505d2-132">Codiert eine Ansicht für die Empfängertabelle einer Nachricht im TNEF-Datenstrom für die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="505d2-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="505d2-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="505d2-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="505d2-134">Verarbeitet einzelne Komponenten aus einer Nachricht nacheinander in einem TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="505d2-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="505d2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="505d2-135">See also</span></span>



[<span data-ttu-id="505d2-136">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="505d2-136">MAPI Interfaces</span></span>](mapi-interfaces.md)


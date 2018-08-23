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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1803707b46b9b58e7372e7e58cc36241d0ebdb4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571724"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="42175-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42175-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="42175-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42175-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42175-105">Bietet Methoden zum Kapseln von MAPI-Eigenschaften, die nicht von einem messaging-System in binären Streams unterstützt werden, die Nachrichten zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="42175-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="42175-106">Das Format für diese Kapselung ist der Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="42175-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="42175-107">Die Ziel-Transport-Anbieter oder MAPI-basierter Client-Anwendung können Sie dann auf Empfangen einer Nachricht, die TNEF-Anlage enthält, die Eigenschaften aus der Anlage wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="42175-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42175-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="42175-108">Header file:</span></span>  <br/> |<span data-ttu-id="42175-109">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="42175-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="42175-110">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="42175-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="42175-111">TNEF-Objekte</span><span class="sxs-lookup"><span data-stu-id="42175-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="42175-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="42175-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="42175-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="42175-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="42175-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="42175-114">Called by:</span></span>  <br/> |<span data-ttu-id="42175-115">Transport-Provider, Anbieter Nachricht und gateways</span><span class="sxs-lookup"><span data-stu-id="42175-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="42175-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="42175-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="42175-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="42175-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="42175-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="42175-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="42175-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="42175-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="42175-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="42175-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="42175-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="42175-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="42175-122">Ermöglicht die aufrufende Dienstanbieter oder Gateway Eigenschaften, die Kapselung einer Nachricht oder eine Anlage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="42175-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="42175-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="42175-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="42175-124">Extrahiert die Eigenschaften von TNEF-Kapselung.</span><span class="sxs-lookup"><span data-stu-id="42175-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="42175-125">Finish</span><span class="sxs-lookup"><span data-stu-id="42175-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="42175-126">Beendet Verarbeitung für alle TNEF-Vorgänge, die sich in der Warteschlange und wartet.</span><span class="sxs-lookup"><span data-stu-id="42175-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="42175-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="42175-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="42175-128">Öffnet eine Stream-Schnittstelle für den Text der Fehlermeldung der gekapselte.</span><span class="sxs-lookup"><span data-stu-id="42175-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="42175-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="42175-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="42175-130">Legt den Wert einer oder mehrerer Eigenschaften für eine gekapselte Nachricht oder Anlage ohne Ändern der ursprünglichen Nachricht oder Anlage fest.</span><span class="sxs-lookup"><span data-stu-id="42175-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="42175-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="42175-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="42175-132">Codiert eine Ansicht für die Empfänger einer Nachricht-Tabelle in der TNEF-Datenstrom für die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="42175-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="42175-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="42175-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="42175-134">Verarbeitet aus einer Nachricht an eine einzelne Komponenten zu einem Zeitpunkt in einem TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="42175-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42175-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42175-135">See also</span></span>



[<span data-ttu-id="42175-136">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="42175-136">MAPI Interfaces</span></span>](mapi-interfaces.md)


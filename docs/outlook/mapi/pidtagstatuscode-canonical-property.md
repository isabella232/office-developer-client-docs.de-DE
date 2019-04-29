---
title: Kanonische Pidtagstatuscode (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418514"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="5ec05-103">Kanonische Pidtagstatuscode (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5ec05-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="5ec05-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ec05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ec05-105">Enthält eine Bitmaske von Flags, die den aktuellen Status einer Sitzungs Ressource kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="5ec05-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="5ec05-106">Alle Dienstanbieter legen Statuscodes fest, ebenso wie MAPI, um den Status des Subsystems, den MAPI-Spooler und das integrierte Adressbuch zu melden.</span><span class="sxs-lookup"><span data-stu-id="5ec05-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ec05-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5ec05-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ec05-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="5ec05-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="5ec05-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5ec05-109">Identifier:</span></span>  <br/> |<span data-ttu-id="5ec05-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="5ec05-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="5ec05-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5ec05-111">Data type:</span></span>  <br/> |<span data-ttu-id="5ec05-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5ec05-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5ec05-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5ec05-113">Area:</span></span>  <br/> |<span data-ttu-id="5ec05-114">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="5ec05-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ec05-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ec05-115">Remarks</span></span>

<span data-ttu-id="5ec05-116">Der Statuscode muss in der Datei MAPISVC. inf für alle Anbieter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5ec05-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="5ec05-117">Status Objekte werden von MAPI und von allen Dienstanbietern implementiert.</span><span class="sxs-lookup"><span data-stu-id="5ec05-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="5ec05-118">Es gibt zwei Sätze gültiger Werte für Statuscodes, ein Satz für alle Status-Objekte und ein weiterer Satz nur für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="5ec05-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="5ec05-119">Alle Status-Objekte können diese Eigenschaft auf die folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="5ec05-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="5ec05-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="5ec05-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="5ec05-121">Gibt an, dass die Ressource betriebsbereit ist.</span><span class="sxs-lookup"><span data-stu-id="5ec05-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="5ec05-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="5ec05-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="5ec05-123">Gibt an, dass die Ressource ein Problem aufWeist.</span><span class="sxs-lookup"><span data-stu-id="5ec05-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="5ec05-124">Für Dienstanbieter gibt STATUS_FAILURE an, dass der Anbieter in Kürze heruntergefahren werden kann, um die aktuelle Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="5ec05-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="5ec05-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5ec05-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="5ec05-126">Gibt an, dass nur lokale Daten oder Dienste verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5ec05-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="5ec05-127">Transport Anbieter können auch die **PR_STATUS_CODE** -Eigenschaften ihrer Statusobjekte auf die folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="5ec05-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="5ec05-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="5ec05-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="5ec05-129">Gibt an, dass der Transportanbieter eine eingehende Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="5ec05-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="5ec05-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="5ec05-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="5ec05-131">Gibt an, dass der Transportanbieter eingehende Nachrichten empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="5ec05-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="5ec05-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="5ec05-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="5ec05-133">Gibt an, dass der Transportanbieter Nachrichten aus der eingehenden Warteschlange herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="5ec05-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="5ec05-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="5ec05-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="5ec05-135">Gibt an, dass der Transportanbieter eine ausgehende Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="5ec05-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="5ec05-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="5ec05-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="5ec05-137">Gibt an, dass der Transportanbieter ausgehende Nachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5ec05-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="5ec05-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="5ec05-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="5ec05-139">Gibt an, dass der Transportanbieter Nachrichten aus der ausgehenden Warteschlange hoch lädt.</span><span class="sxs-lookup"><span data-stu-id="5ec05-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="5ec05-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5ec05-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="5ec05-141">Gibt an, dass der Transportanbieter den Remotezugriff unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ec05-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5ec05-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5ec05-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5ec05-143">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5ec05-143">Header files</span></span>

<span data-ttu-id="5ec05-144">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5ec05-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ec05-145">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5ec05-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ec05-146">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5ec05-146">Mapitags.h</span></span>
  
> <span data-ttu-id="5ec05-147">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5ec05-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ec05-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ec05-148">See also</span></span>



[<span data-ttu-id="5ec05-149">Kanonische Pidtagstatusstring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5ec05-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="5ec05-150">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ec05-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ec05-151">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5ec05-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ec05-152">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5ec05-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ec05-153">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5ec05-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


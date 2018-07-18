---
title: PidTagStatusCode (kanonische Eigenschaft)
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795207"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="45fbc-103">PidTagStatusCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45fbc-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="45fbc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45fbc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45fbc-105">Enthält eine Bitmaske der Flags, die den aktuellen Status einer Sitzung Ressource angeben.</span><span class="sxs-lookup"><span data-stu-id="45fbc-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="45fbc-106">Alle-Dienstanbieter festzulegen Statuscodes, wie MAPI, um den Bericht über den Status des Teilsystems, die MAPI-Warteschlange und das integrierte-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="45fbc-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45fbc-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45fbc-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="45fbc-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="45fbc-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="45fbc-109">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="45fbc-109">Identifier:</span></span>  <br/> |<span data-ttu-id="45fbc-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="45fbc-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="45fbc-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45fbc-111">Data type:</span></span>  <br/> |<span data-ttu-id="45fbc-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45fbc-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45fbc-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45fbc-113">Area:</span></span>  <br/> |<span data-ttu-id="45fbc-114">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="45fbc-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45fbc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45fbc-115">Remarks</span></span>

<span data-ttu-id="45fbc-116">Der Statuscode muss für alle Anbieter in der Datei "Mapisvc.inf" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="45fbc-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="45fbc-117">Status-Objekte werden MAPI und von allen Dienstanbietern implementiert.</span><span class="sxs-lookup"><span data-stu-id="45fbc-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="45fbc-118">Es gibt zwei Sätze von gültigen Werten für Statuscodes, eine Gruppe für alle Objekte, Status und einen weiteren Satz für Transportanbieter nur ein.</span><span class="sxs-lookup"><span data-stu-id="45fbc-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="45fbc-119">Alle Status-Objekte können diese Eigenschaft auf die folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="45fbc-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="45fbc-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="45fbc-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="45fbc-121">Gibt an, dass die Ressource ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="45fbc-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="45fbc-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="45fbc-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="45fbc-123">Gibt an, dass die Ressource ein Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="45fbc-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="45fbc-124">Für Dienstanbieter gibt STATUS_FAILURE an, dass der Anbieter bald heruntergefahren werden kann, um die aktuelle Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="45fbc-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="45fbc-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="45fbc-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="45fbc-126">Gibt an, dass nur lokale Daten oder Dienste zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="45fbc-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="45fbc-127">Transportanbieter können auch ihr Status des Objekts **PR_STATUS_CODE** Eigenschaften auf die folgenden Werte festlegen:</span><span class="sxs-lookup"><span data-stu-id="45fbc-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="45fbc-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="45fbc-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="45fbc-129">Gibt an, dass der Adressbuchhierarchie eine eingehende Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="45fbc-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="45fbc-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="45fbc-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="45fbc-131">Gibt an, dass der Adressbuchhierarchie eingehende Nachrichten empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="45fbc-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="45fbc-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="45fbc-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="45fbc-133">Gibt an, dass der Adressbuchhierarchie aus der Warteschlange für eingehende Nachrichten heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="45fbc-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="45fbc-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="45fbc-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="45fbc-135">Gibt an, dass der Adressbuchhierarchie eine ausgehende Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="45fbc-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="45fbc-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="45fbc-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="45fbc-137">Gibt an, dass der Adressbuchhierarchie ausgehende Nachrichten verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="45fbc-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="45fbc-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="45fbc-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="45fbc-139">Gibt an, dass der Adressbuchhierarchie Nachrichten aus der ausgehenden Warteschlange hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="45fbc-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="45fbc-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="45fbc-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="45fbc-141">Gibt an, dass der Adressbuchhierarchie Remotezugriff unterstützt.</span><span class="sxs-lookup"><span data-stu-id="45fbc-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="45fbc-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45fbc-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="45fbc-143">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="45fbc-143">Header files</span></span>

<span data-ttu-id="45fbc-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45fbc-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="45fbc-145">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="45fbc-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="45fbc-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45fbc-146">Mapitags.h</span></span>
  
> <span data-ttu-id="45fbc-147">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45fbc-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45fbc-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45fbc-148">See also</span></span>



[<span data-ttu-id="45fbc-149">PidTagStatusString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45fbc-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="45fbc-150">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45fbc-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45fbc-151">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45fbc-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45fbc-152">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45fbc-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45fbc-153">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45fbc-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


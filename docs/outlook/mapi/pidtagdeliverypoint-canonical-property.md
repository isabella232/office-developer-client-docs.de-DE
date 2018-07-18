---
title: PidTagDeliveryPoint (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794310"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="35acf-103">PidTagDeliveryPoint (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35acf-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="35acf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35acf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35acf-105">Gibt die Art der funktionalen Entität, mit der eine Nachricht wurde oder wird an den Empfänger übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="35acf-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35acf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35acf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35acf-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="35acf-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="35acf-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="35acf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35acf-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="35acf-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="35acf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35acf-110">Data type:</span></span>  <br/> |<span data-ttu-id="35acf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="35acf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="35acf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35acf-112">Area:</span></span>  <br/> |<span data-ttu-id="35acf-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="35acf-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35acf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35acf-114">Remarks</span></span>

<span data-ttu-id="35acf-115">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="35acf-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="35acf-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="35acf-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="35acf-117">An eine Verteilerliste gesendet, die wiederum die Nachricht an mehrere Empfänger verteilen kann eine Übermittlung zeigen.</span><span class="sxs-lookup"><span data-stu-id="35acf-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="35acf-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="35acf-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="35acf-119">An einen Nachrichtenspeicher anstatt direkt an einen Empfänger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="35acf-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="35acf-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="35acf-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="35acf-121">Eine Access Organizational Unit (AU) als eine physische Bereitstellung Access Einheit (PDAU), wie ein FAX System zugestellt.</span><span class="sxs-lookup"><span data-stu-id="35acf-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="35acf-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="35acf-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="35acf-123">An eine physische Bereitstellung Access Einheit wie eine human postalische Netzbetreiber übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="35acf-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="35acf-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="35acf-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="35acf-125">An ein physisches Delivery System Leser, wie eine herkömmliche postalische Postfach übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="35acf-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="35acf-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="35acf-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="35acf-127">Übermittelt eine private Benutzer-Agent (UA), wie ein Client in einem internen messaging-System.</span><span class="sxs-lookup"><span data-stu-id="35acf-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="35acf-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="35acf-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="35acf-129">An eine öffentliche Benutzer-Agent oder öffentlichen Dienstanbieter übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="35acf-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="35acf-130">Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, d. h., einem MAPI-Client.</span><span class="sxs-lookup"><span data-stu-id="35acf-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35acf-131">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35acf-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35acf-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="35acf-132">Header files</span></span>

<span data-ttu-id="35acf-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35acf-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="35acf-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="35acf-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="35acf-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35acf-135">Mapitags.h</span></span>
  
> <span data-ttu-id="35acf-136">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="35acf-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35acf-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35acf-137">See also</span></span>



[<span data-ttu-id="35acf-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35acf-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35acf-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35acf-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35acf-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35acf-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35acf-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35acf-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


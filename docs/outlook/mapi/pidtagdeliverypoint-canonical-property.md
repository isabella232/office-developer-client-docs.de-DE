---
title: Kanonische Pidtagdeliverypoint (-Eigenschaft
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
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360879"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="e37e2-103">Kanonische Pidtagdeliverypoint (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e37e2-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="e37e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e37e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e37e2-105">Gibt die Art der funktionalen Entität an, anhand derer eine Nachricht an den Empfänger übermittelt wurde oder wäre.</span><span class="sxs-lookup"><span data-stu-id="e37e2-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e37e2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e37e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e37e2-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="e37e2-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="e37e2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e37e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e37e2-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="e37e2-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="e37e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e37e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="e37e2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e37e2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e37e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e37e2-112">Area:</span></span>  <br/> |<span data-ttu-id="e37e2-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="e37e2-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e37e2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e37e2-114">Remarks</span></span>

<span data-ttu-id="e37e2-115">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="e37e2-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="e37e2-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="e37e2-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="e37e2-117">An eine Verteilerliste zuGestellt, ein Zustellungs Punkt, der die Nachricht wiederum an viele Empfänger verteilen kann.</span><span class="sxs-lookup"><span data-stu-id="e37e2-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="e37e2-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="e37e2-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="e37e2-119">Wird an einen Nachrichtenspeicher anstatt direkt an einen Empfänger überMittelt.</span><span class="sxs-lookup"><span data-stu-id="e37e2-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="e37e2-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="e37e2-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="e37e2-121">Wird an eine andere Zugriffseinheit (AU) als eine physische Zustellungs Zugriffseinheit (PDAU) (beispielsweise ein FAX) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e37e2-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="e37e2-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="e37e2-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="e37e2-123">An eine physische Zustellungs Einheit übermittelt, beispielsweise einen menschlichen postalischen Spediteur.</span><span class="sxs-lookup"><span data-stu-id="e37e2-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="e37e2-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="e37e2-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="e37e2-125">An einen Systembenutzer für physische Zustellungen, wie ein herkömmliches Post Postfach, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e37e2-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="e37e2-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="e37e2-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="e37e2-127">Wird an einen privaten Benutzer-Agent (UA), beispielsweise einen Client in einem internen Messagingsystem, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e37e2-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="e37e2-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="e37e2-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="e37e2-129">An einen öffentlichen Benutzer-Agent oder einen öffentlichen Dienstanbieter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e37e2-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="e37e2-130">Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, also ein MAPI-Client.</span><span class="sxs-lookup"><span data-stu-id="e37e2-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e37e2-131">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e37e2-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e37e2-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e37e2-132">Header files</span></span>

<span data-ttu-id="e37e2-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e37e2-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="e37e2-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e37e2-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="e37e2-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e37e2-135">Mapitags.h</span></span>
  
> <span data-ttu-id="e37e2-136">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e37e2-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e37e2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e37e2-137">See also</span></span>



[<span data-ttu-id="e37e2-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e37e2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e37e2-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e37e2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e37e2-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e37e2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e37e2-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e37e2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


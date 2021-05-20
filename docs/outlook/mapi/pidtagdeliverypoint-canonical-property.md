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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439422"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="ed3e8-103">PidTagDeliveryPoint (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed3e8-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="ed3e8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed3e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed3e8-105">Gibt die Art der funktionalen Entität an, mit der eine Nachricht an den Empfänger übermittelt wurde oder hätte.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed3e8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ed3e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed3e8-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="ed3e8-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="ed3e8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ed3e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed3e8-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="ed3e8-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="ed3e8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ed3e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed3e8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ed3e8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ed3e8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ed3e8-112">Area:</span></span>  <br/> |<span data-ttu-id="ed3e8-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="ed3e8-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed3e8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed3e8-114">Remarks</span></span>

<span data-ttu-id="ed3e8-115">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="ed3e8-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="ed3e8-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="ed3e8-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="ed3e8-117">An eine Verteilerliste zugestellt, ein Zustellungspunkt, der die Nachricht wiederum an viele Empfänger verteilen kann.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="ed3e8-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="ed3e8-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="ed3e8-119">An einen Nachrichtenspeicher anstatt direkt an einen Empfänger zugestellt.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="ed3e8-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="ed3e8-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="ed3e8-121">Wird an eine andere Zugriffseinheit (Access Unit, AU) als eine physische Zustellungszugriffseinheit (PHYSICAL Delivery Access Unit, PDAU) übermittelt, z. B. ein FAX-System.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="ed3e8-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="ed3e8-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="ed3e8-123">An eine physische Zustellungszugriffseinheit, z. B. ein menschliches Postunternehmen, zugestellt.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="ed3e8-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="ed3e8-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="ed3e8-125">Zugestellt an einen physischen Systempatron, z. B. ein herkömmliches Postpostfach.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="ed3e8-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="ed3e8-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="ed3e8-127">An einen privaten Benutzer-Agent (PRIVATE User Agent, UA) übermittelt, z. B. an einen Client in einem eigenen Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="ed3e8-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="ed3e8-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="ed3e8-129">An einen öffentlichen Benutzer-Agent oder öffentlichen Dienstanbieter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="ed3e8-130">Der Standardwert ist MAPI_MH_DP_PRIVATE_UA, d. h. ein MAPI-Client.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed3e8-131">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ed3e8-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ed3e8-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ed3e8-132">Header files</span></span>

<span data-ttu-id="ed3e8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed3e8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed3e8-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed3e8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed3e8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ed3e8-136">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ed3e8-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed3e8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed3e8-137">See also</span></span>



[<span data-ttu-id="ed3e8-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed3e8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed3e8-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ed3e8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed3e8-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ed3e8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed3e8-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ed3e8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


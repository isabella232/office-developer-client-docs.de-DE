---
title: Kanonische Pidtagproviderordinal (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438351"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="daf39-103">Kanonische Pidtagproviderordinal (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="daf39-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="daf39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daf39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daf39-105">Enthält den nullbasierten Index der Position eines Dienstanbieters in der Anbieter Tabelle.</span><span class="sxs-lookup"><span data-stu-id="daf39-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daf39-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="daf39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="daf39-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="daf39-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="daf39-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="daf39-108">Identifier:</span></span>  <br/> |<span data-ttu-id="daf39-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="daf39-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="daf39-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="daf39-110">Data type:</span></span>  <br/> |<span data-ttu-id="daf39-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="daf39-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="daf39-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="daf39-112">Area:</span></span>  <br/> |<span data-ttu-id="daf39-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="daf39-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daf39-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="daf39-114">Remarks</span></span>

<span data-ttu-id="daf39-115">Diese Eigenschaft wird von MAPI berechnet.</span><span class="sxs-lookup"><span data-stu-id="daf39-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="daf39-116">Rufen Sie die Anbieter Tabelle ab, indem Sie die [IMsgServiceAdmin:: GetProvider](imsgserviceadmin-getprovidertable.md) Table-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="daf39-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="daf39-117">Sortieren Sie die Anbieter Tabelle für diese Eigenschaft, um den Transportauftrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="daf39-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="daf39-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="daf39-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="daf39-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="daf39-119">Header files</span></span>

<span data-ttu-id="daf39-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="daf39-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="daf39-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="daf39-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="daf39-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="daf39-122">Mapitags.h</span></span>
  
> <span data-ttu-id="daf39-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="daf39-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="daf39-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="daf39-124">See also</span></span>



[<span data-ttu-id="daf39-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="daf39-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="daf39-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="daf39-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="daf39-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="daf39-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="daf39-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="daf39-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


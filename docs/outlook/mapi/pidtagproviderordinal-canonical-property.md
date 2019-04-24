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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286439"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="1a97b-103">Kanonische Pidtagproviderordinal (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a97b-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="1a97b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a97b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a97b-105">Enthält den nullbasierten Index der Position eines Dienstanbieters in der Anbieter Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1a97b-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a97b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1a97b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a97b-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="1a97b-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="1a97b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1a97b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a97b-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="1a97b-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="1a97b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1a97b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a97b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a97b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a97b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1a97b-112">Area:</span></span>  <br/> |<span data-ttu-id="1a97b-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="1a97b-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a97b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a97b-114">Remarks</span></span>

<span data-ttu-id="1a97b-115">Diese Eigenschaft wird von MAPI berechnet.</span><span class="sxs-lookup"><span data-stu-id="1a97b-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="1a97b-116">Rufen Sie die Anbieter Tabelle ab, indem Sie die [IMsgServiceAdmin:: GetProvider](imsgserviceadmin-getprovidertable.md) Table-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1a97b-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="1a97b-117">Sortieren Sie die Anbieter Tabelle für diese Eigenschaft, um den Transportauftrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1a97b-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a97b-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1a97b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1a97b-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="1a97b-119">Header files</span></span>

<span data-ttu-id="1a97b-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1a97b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a97b-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="1a97b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a97b-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1a97b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1a97b-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1a97b-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a97b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a97b-124">See also</span></span>



[<span data-ttu-id="1a97b-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a97b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a97b-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a97b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a97b-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1a97b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a97b-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1a97b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


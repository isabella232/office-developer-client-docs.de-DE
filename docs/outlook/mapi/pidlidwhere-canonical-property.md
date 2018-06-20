---
title: Kanonische PidLidWhere-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 127627b79782a2a785b00b79b9940b66256a08eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793917"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="dcb0d-103">Kanonische PidLidWhere-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dcb0d-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="dcb0d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcb0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcb0d-105">Gibt den Speicherort eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcb0d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dcb0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcb0d-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="dcb0d-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="dcb0d-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="dcb0d-108">Property set:</span></span>  <br/> |<span data-ttu-id="dcb0d-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="dcb0d-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="dcb0d-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="dcb0d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dcb0d-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dcb0d-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="dcb0d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dcb0d-112">Data type:</span></span>  <br/> |<span data-ttu-id="dcb0d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dcb0d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dcb0d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dcb0d-114">Area:</span></span>  <br/> |<span data-ttu-id="dcb0d-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="dcb0d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcb0d-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcb0d-116">Remarks</span></span>

<span data-ttu-id="dcb0d-117">Der Wert dieser Eigenschaft sollte den Wert der Eigenschaft **DispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) aus der zugeordneten Besprechung identisch sein.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dcb0d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dcb0d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcb0d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dcb0d-119">Protocol specifications</span></span>

<span data-ttu-id="dcb0d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcb0d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcb0d-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dcb0d-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcb0d-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcb0d-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcb0d-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dcb0d-124">Header files</span></span>

<span data-ttu-id="dcb0d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dcb0d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcb0d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dcb0d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcb0d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcb0d-127">See also</span></span>



[<span data-ttu-id="dcb0d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcb0d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcb0d-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dcb0d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcb0d-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dcb0d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcb0d-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dcb0d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


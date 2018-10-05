---
title: PidLidWhere (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390562"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="d40db-103">PidLidWhere (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d40db-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="d40db-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d40db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d40db-105">Gibt den Speicherort eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d40db-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d40db-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d40db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d40db-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="d40db-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="d40db-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d40db-108">Property set:</span></span>  <br/> |<span data-ttu-id="d40db-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="d40db-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="d40db-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d40db-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d40db-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d40db-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="d40db-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d40db-112">Data type:</span></span>  <br/> |<span data-ttu-id="d40db-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d40db-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d40db-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d40db-114">Area:</span></span>  <br/> |<span data-ttu-id="d40db-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="d40db-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d40db-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d40db-116">Remarks</span></span>

<span data-ttu-id="d40db-117">Der Wert dieser Eigenschaft sollte den Wert der Eigenschaft **DispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) aus der zugeordneten Besprechung identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d40db-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d40db-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d40db-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d40db-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d40db-119">Protocol specifications</span></span>

<span data-ttu-id="d40db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d40db-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d40db-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d40db-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d40db-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d40db-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d40db-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d40db-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d40db-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d40db-124">Header files</span></span>

<span data-ttu-id="d40db-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d40db-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d40db-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d40db-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d40db-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d40db-127">See also</span></span>



[<span data-ttu-id="d40db-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d40db-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d40db-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d40db-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d40db-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d40db-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d40db-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d40db-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


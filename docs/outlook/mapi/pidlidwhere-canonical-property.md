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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360431"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="9364e-103">PidLidWhere (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9364e-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="9364e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9364e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9364e-105">Gibt den Speicherort eines Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="9364e-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9364e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9364e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9364e-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="9364e-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="9364e-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="9364e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9364e-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="9364e-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="9364e-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9364e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9364e-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9364e-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="9364e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9364e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9364e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9364e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9364e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9364e-114">Area:</span></span>  <br/> |<span data-ttu-id="9364e-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="9364e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9364e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9364e-116">Remarks</span></span>

<span data-ttu-id="9364e-117">Der Wert dieser Eigenschaft sollte mit dem Wert der **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md))-Eigenschaft aus der zugeordneten Besprechung identisch sein.</span><span class="sxs-lookup"><span data-stu-id="9364e-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9364e-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9364e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9364e-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9364e-119">Protocol specifications</span></span>

<span data-ttu-id="9364e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9364e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9364e-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9364e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9364e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9364e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9364e-123">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="9364e-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9364e-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9364e-124">Header files</span></span>

<span data-ttu-id="9364e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9364e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9364e-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9364e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9364e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9364e-127">See also</span></span>



[<span data-ttu-id="9364e-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9364e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9364e-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9364e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9364e-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9364e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9364e-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9364e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


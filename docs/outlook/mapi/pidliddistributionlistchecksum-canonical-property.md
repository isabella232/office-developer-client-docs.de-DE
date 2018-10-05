---
title: PidLidDistributionListChecksum (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383906"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="dc999-103">PidLidDistributionListChecksum (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dc999-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="dc999-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc999-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc999-105">Gibt die 32-Bit-CRC polynomial Prüfsumme für eine persönliche Verteilerliste Kontrollkästchen (CRC-32).</span><span class="sxs-lookup"><span data-stu-id="dc999-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc999-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dc999-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc999-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="dc999-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="dc999-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="dc999-108">Property set:</span></span>  <br/> |<span data-ttu-id="dc999-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="dc999-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="dc999-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="dc999-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dc999-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="dc999-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="dc999-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dc999-112">Data type:</span></span>  <br/> |<span data-ttu-id="dc999-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc999-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc999-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dc999-114">Area:</span></span>  <br/> |<span data-ttu-id="dc999-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="dc999-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc999-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc999-116">Remarks</span></span>

<span data-ttu-id="dc999-117">Der Wert dieser Eigenschaft kann verwendet werden, zu erkennen, wann die **DispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft aktualisiert wurde, ohne die Aktualisierung der anderen persönlichen Verteilerliste Liste Elementeigenschaften durch den CRC-32 auf dem vorhandenen computing der Wert der **DispidDLMembers** und diese mit dem Wert der Eigenschaft **DispidDLChecksum** zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="dc999-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dc999-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dc999-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc999-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dc999-119">Protocol specifications</span></span>

<span data-ttu-id="dc999-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc999-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc999-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dc999-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc999-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc999-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc999-123">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dc999-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc999-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dc999-124">Header files</span></span>

<span data-ttu-id="dc999-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc999-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc999-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dc999-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc999-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc999-127">See also</span></span>



[<span data-ttu-id="dc999-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc999-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc999-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc999-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc999-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dc999-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc999-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dc999-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


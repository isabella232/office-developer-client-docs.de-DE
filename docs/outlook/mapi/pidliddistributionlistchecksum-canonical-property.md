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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357610"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="09b39-103">PidLidDistributionListChecksum (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="09b39-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="09b39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09b39-105">Gibt die 32-Bit-Zyklische Redundanzprüfung (CRC-32) für eine persönliche Verteilerliste an.</span><span class="sxs-lookup"><span data-stu-id="09b39-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09b39-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="09b39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09b39-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="09b39-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="09b39-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="09b39-108">Property set:</span></span>  <br/> |<span data-ttu-id="09b39-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="09b39-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="09b39-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="09b39-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="09b39-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="09b39-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="09b39-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="09b39-112">Data type:</span></span>  <br/> |<span data-ttu-id="09b39-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="09b39-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="09b39-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="09b39-114">Area:</span></span>  <br/> |<span data-ttu-id="09b39-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="09b39-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09b39-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09b39-116">Remarks</span></span>

<span data-ttu-id="09b39-117">Der Wert dieser Eigenschaft kann verwendet werden, um zu erkennen, wann die **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft aktualisiert wurde, ohne die anderen Eigenschaften der Mitglieder der persönlichen Verteilerliste zu aktualisieren, indem der CRC-32 anhand des vorhandenen Werts von **dispidDLMembers** ermittelt und mit dem Wert der **dispidDLChecksum-Eigenschaft** verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="09b39-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="09b39-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="09b39-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09b39-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="09b39-119">Protocol specifications</span></span>

<span data-ttu-id="09b39-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09b39-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09b39-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="09b39-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="09b39-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09b39-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09b39-123">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="09b39-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09b39-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="09b39-124">Header files</span></span>

<span data-ttu-id="09b39-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09b39-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="09b39-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="09b39-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09b39-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09b39-127">See also</span></span>



[<span data-ttu-id="09b39-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="09b39-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09b39-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="09b39-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09b39-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="09b39-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09b39-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="09b39-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


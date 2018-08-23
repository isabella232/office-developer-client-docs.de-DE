---
title: PidLidDistributionListOneOffMembers (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ef60c13923753eb7e349b91a5a4727958ebb73e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580236"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="92d19-103">PidLidDistributionListOneOffMembers (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="92d19-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="92d19-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92d19-105">Gibt die Liste der einmaligen EntryIds, die die Elemente der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="92d19-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92d19-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="92d19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92d19-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="92d19-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="92d19-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="92d19-108">Property set:</span></span>  <br/> |<span data-ttu-id="92d19-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="92d19-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="92d19-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="92d19-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="92d19-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="92d19-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="92d19-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="92d19-112">Data type:</span></span>  <br/> |<span data-ttu-id="92d19-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="92d19-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="92d19-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="92d19-114">Area:</span></span>  <br/> |<span data-ttu-id="92d19-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="92d19-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92d19-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="92d19-116">Remarks</span></span>

<span data-ttu-id="92d19-117">Diese einmaligen EntryIds kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="92d19-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="92d19-118">Wenn der Client oder der Server wird diese Eigenschaft festzulegen, müssen sie mit der **DispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft synchronisiert: für jeden Eintrag in der **DispidDLOneOffMembers** -Eigenschaft muss ein Eintrag in der gleichen vorhanden sein Positionieren Sie in der **DispidDLMembers** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92d19-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="92d19-119">Beim Festlegen von **DispidDLOneOffMembers**muss der Client oder der Server sicher, dass die Gesamtgröße der Größe von weniger als 15.000 Bytes.</span><span class="sxs-lookup"><span data-stu-id="92d19-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92d19-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="92d19-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92d19-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="92d19-121">Protocol specifications</span></span>

<span data-ttu-id="92d19-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92d19-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92d19-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="92d19-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92d19-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92d19-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92d19-125">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="92d19-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92d19-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="92d19-126">Header files</span></span>

<span data-ttu-id="92d19-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92d19-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="92d19-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="92d19-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92d19-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92d19-129">See also</span></span>



[<span data-ttu-id="92d19-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92d19-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92d19-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92d19-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92d19-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="92d19-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92d19-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="92d19-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


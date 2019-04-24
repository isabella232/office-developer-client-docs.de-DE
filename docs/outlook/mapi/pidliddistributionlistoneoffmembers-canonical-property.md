---
title: Kanonische Pidliddistributionlistoneoffmembers (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335049"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="bbafb-103">Kanonische Pidliddistributionlistoneoffmembers (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bbafb-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="bbafb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbafb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbafb-105">Gibt die Liste der einmaligen EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bbafb-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bbafb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bbafb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbafb-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="bbafb-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="bbafb-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="bbafb-108">Property set:</span></span>  <br/> |<span data-ttu-id="bbafb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="bbafb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="bbafb-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="bbafb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bbafb-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="bbafb-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="bbafb-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bbafb-112">Data type:</span></span>  <br/> |<span data-ttu-id="bbafb-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbafb-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bbafb-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bbafb-114">Area:</span></span>  <br/> |<span data-ttu-id="bbafb-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="bbafb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbafb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbafb-116">Remarks</span></span>

<span data-ttu-id="bbafb-117">Diese einmalige EntryIds Kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="bbafb-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="bbafb-118">Wenn der Client oder der Server diese Eigenschaft festlegen, muss Sie mit der **dispidDLMembers** ([pidliddistributionlistmembers (](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft synchronisiert werden: für jeden Eintrag in der **dispidDLOneOffMembers** -Eigenschaft muss ein Eintrag in derselben Position in der **dispidDLMembers** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bbafb-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="bbafb-119">Beim Festlegen von **dispidDLOneOffMembers**muss der Client oder der Server sicherstellen, dass seine Gesamtgröße kleiner als 15.000 Byte ist.</span><span class="sxs-lookup"><span data-stu-id="bbafb-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bbafb-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bbafb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbafb-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bbafb-121">Protocol specifications</span></span>

<span data-ttu-id="bbafb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbafb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbafb-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="bbafb-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbafb-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbafb-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbafb-125">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bbafb-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbafb-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bbafb-126">Header files</span></span>

<span data-ttu-id="bbafb-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bbafb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbafb-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bbafb-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbafb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbafb-129">See also</span></span>



[<span data-ttu-id="bbafb-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbafb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbafb-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbafb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbafb-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bbafb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbafb-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bbafb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


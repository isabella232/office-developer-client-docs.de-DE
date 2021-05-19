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
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335049"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="baf3f-103">PidLidDistributionListOneOffMembers (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="baf3f-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="baf3f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baf3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baf3f-105">Gibt die Liste der einmal verwendeten EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="baf3f-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="baf3f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="baf3f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="baf3f-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="baf3f-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="baf3f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="baf3f-108">Property set:</span></span>  <br/> |<span data-ttu-id="baf3f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="baf3f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="baf3f-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="baf3f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="baf3f-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="baf3f-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="baf3f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="baf3f-112">Data type:</span></span>  <br/> |<span data-ttu-id="baf3f-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="baf3f-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="baf3f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="baf3f-114">Area:</span></span>  <br/> |<span data-ttu-id="baf3f-115">Kontakt</span><span class="sxs-lookup"><span data-stu-id="baf3f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baf3f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="baf3f-116">Remarks</span></span>

<span data-ttu-id="baf3f-117">Diese einmal verwendeten EntryIds kapseln Anzeigenamen und E-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="baf3f-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="baf3f-118">Wenn der Client oder der Server diese Eigenschaft festlegen, muss sie mit der **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md))-Eigenschaft synchronisiert werden: Für jeden Eintrag in der **dispidDLOneOffMembers-Eigenschaft** muss ein Eintrag an derselben Position in der **dispidDLMembers-Eigenschaft** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="baf3f-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="baf3f-119">Beim Festlegen **von dispidDLOneOffMembers** muss der Client oder der Server sicherstellen, dass die Gesamtgröße weniger als 15.000 Byte beträgt.</span><span class="sxs-lookup"><span data-stu-id="baf3f-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="baf3f-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="baf3f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="baf3f-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="baf3f-121">Protocol specifications</span></span>

<span data-ttu-id="baf3f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="baf3f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="baf3f-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="baf3f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="baf3f-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="baf3f-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="baf3f-125">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="baf3f-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="baf3f-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="baf3f-126">Header files</span></span>

<span data-ttu-id="baf3f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="baf3f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="baf3f-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="baf3f-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="baf3f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baf3f-129">See also</span></span>



[<span data-ttu-id="baf3f-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="baf3f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="baf3f-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="baf3f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="baf3f-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="baf3f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="baf3f-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="baf3f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


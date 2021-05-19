---
title: PidLidLogEnd (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336925"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="428fd-103">PidLidLogEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="428fd-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="428fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="428fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="428fd-105">Stellt das Enddatum und die Uhrzeit für die Journalnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="428fd-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="428fd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="428fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="428fd-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="428fd-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="428fd-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="428fd-108">Property set:</span></span>  <br/> |<span data-ttu-id="428fd-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="428fd-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="428fd-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="428fd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="428fd-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="428fd-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="428fd-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="428fd-112">Data type:</span></span>  <br/> |<span data-ttu-id="428fd-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="428fd-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="428fd-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="428fd-114">Area:</span></span>  <br/> |<span data-ttu-id="428fd-115">Journal</span><span class="sxs-lookup"><span data-stu-id="428fd-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="428fd-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="428fd-116">Remarks</span></span>

<span data-ttu-id="428fd-117">Der Zeitpunkt, zu dem die Aktivität in Coordinated Universal Time The (UTC) endete, der gleich der **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft und größer als oder gleich der **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md))-Eigenschaft sein muss.</span><span class="sxs-lookup"><span data-stu-id="428fd-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="428fd-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="428fd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="428fd-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="428fd-119">Protocol specifications</span></span>

<span data-ttu-id="428fd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="428fd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="428fd-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="428fd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="428fd-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="428fd-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="428fd-123">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="428fd-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="428fd-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="428fd-124">Header files</span></span>

<span data-ttu-id="428fd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="428fd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="428fd-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="428fd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="428fd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="428fd-127">See also</span></span>



[<span data-ttu-id="428fd-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="428fd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="428fd-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="428fd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="428fd-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="428fd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="428fd-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="428fd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


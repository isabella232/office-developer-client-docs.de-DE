---
title: Kanonische Pidlidlogend (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336925"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="28a57-103">Kanonische Pidlidlogend (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28a57-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="28a57-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28a57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28a57-105">Stellt das Enddatum und die Endzeit für die Journalnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="28a57-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28a57-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="28a57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28a57-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="28a57-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="28a57-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="28a57-108">Property set:</span></span>  <br/> |<span data-ttu-id="28a57-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="28a57-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="28a57-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="28a57-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28a57-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="28a57-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="28a57-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="28a57-112">Data type:</span></span>  <br/> |<span data-ttu-id="28a57-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="28a57-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="28a57-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="28a57-114">Area:</span></span>  <br/> |<span data-ttu-id="28a57-115">Journal</span><span class="sxs-lookup"><span data-stu-id="28a57-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28a57-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28a57-116">Remarks</span></span>

<span data-ttu-id="28a57-117">Der Zeitpunkt, zu dem die Aktivität in der koordinierten weltZeit (UTC) endete, die der **dispidCommonEnd** ([pidlidcommonend (](pidlidcommonend-canonical-property.md))-Eigenschaft und der **dispidLogStart** ([pidlidlogstart (](pidlidlogstart-canonical-property.md))-Eigenschaft größer oder gleich ist.</span><span class="sxs-lookup"><span data-stu-id="28a57-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="28a57-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28a57-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28a57-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="28a57-119">Protocol specifications</span></span>

<span data-ttu-id="28a57-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28a57-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28a57-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="28a57-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28a57-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28a57-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28a57-123">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="28a57-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28a57-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="28a57-124">Header files</span></span>

<span data-ttu-id="28a57-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="28a57-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="28a57-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="28a57-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28a57-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a57-127">See also</span></span>



[<span data-ttu-id="28a57-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28a57-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28a57-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28a57-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28a57-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="28a57-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28a57-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="28a57-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


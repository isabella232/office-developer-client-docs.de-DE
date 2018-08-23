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
ms.openlocfilehash: 739fe4077fa57f0f12dd38f05f90851c5291b45a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585934"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="c7d6c-103">PidLidLogEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c7d6c-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="c7d6c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7d6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7d6c-105">Stellt das Enddatum und die Uhrzeit für die Journalnachricht.</span><span class="sxs-lookup"><span data-stu-id="c7d6c-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7d6c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c7d6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7d6c-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="c7d6c-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="c7d6c-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c7d6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="c7d6c-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="c7d6c-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="c7d6c-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="c7d6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c7d6c-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="c7d6c-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="c7d6c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c7d6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="c7d6c-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c7d6c-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c7d6c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c7d6c-114">Area:</span></span>  <br/> |<span data-ttu-id="c7d6c-115">Journal</span><span class="sxs-lookup"><span data-stu-id="c7d6c-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7d6c-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c7d6c-116">Remarks</span></span>

<span data-ttu-id="c7d6c-117">Der Zeitpunkt, wann die Aktivität in koordinierter Weltzeit The (UTC), beendet der **DispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft gleich und größer als oder gleich **DispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md))-Eigenschaft sein muss.</span><span class="sxs-lookup"><span data-stu-id="c7d6c-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7d6c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7d6c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7d6c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c7d6c-119">Protocol specifications</span></span>

<span data-ttu-id="c7d6c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7d6c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7d6c-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c7d6c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7d6c-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7d6c-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7d6c-123">Gibt die Eigenschaften und Operationen, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c7d6c-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7d6c-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c7d6c-124">Header files</span></span>

<span data-ttu-id="c7d6c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7d6c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7d6c-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c7d6c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7d6c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7d6c-127">See also</span></span>



[<span data-ttu-id="c7d6c-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7d6c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7d6c-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7d6c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7d6c-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c7d6c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7d6c-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c7d6c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


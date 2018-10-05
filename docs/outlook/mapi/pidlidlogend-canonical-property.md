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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398941"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="45107-103">PidLidLogEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="45107-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="45107-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45107-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45107-105">Stellt das Enddatum und die Uhrzeit für die Journalnachricht.</span><span class="sxs-lookup"><span data-stu-id="45107-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45107-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45107-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45107-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="45107-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="45107-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="45107-108">Property set:</span></span>  <br/> |<span data-ttu-id="45107-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="45107-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="45107-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="45107-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="45107-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="45107-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="45107-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45107-112">Data type:</span></span>  <br/> |<span data-ttu-id="45107-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="45107-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="45107-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45107-114">Area:</span></span>  <br/> |<span data-ttu-id="45107-115">Journal</span><span class="sxs-lookup"><span data-stu-id="45107-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45107-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45107-116">Remarks</span></span>

<span data-ttu-id="45107-117">Der Zeitpunkt, wann die Aktivität in koordinierter Weltzeit The (UTC), beendet der **DispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md))-Eigenschaft gleich und größer als oder gleich **DispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md))-Eigenschaft sein muss.</span><span class="sxs-lookup"><span data-stu-id="45107-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45107-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45107-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45107-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="45107-119">Protocol specifications</span></span>

<span data-ttu-id="45107-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45107-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45107-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="45107-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45107-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45107-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45107-123">Gibt die Eigenschaften und Operationen, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="45107-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45107-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="45107-124">Header files</span></span>

<span data-ttu-id="45107-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45107-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="45107-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="45107-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45107-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45107-127">See also</span></span>



[<span data-ttu-id="45107-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45107-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45107-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45107-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45107-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45107-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45107-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45107-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


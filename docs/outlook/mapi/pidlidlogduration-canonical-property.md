---
title: PidLidLogDuration (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cc2d52ec183cc336bf126b1fda9a85d41f704f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793660"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="4222a-103">PidLidLogDuration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4222a-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="4222a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4222a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4222a-105">Stellt die Dauer in Minuten, einer Nachricht Journal dar.</span><span class="sxs-lookup"><span data-stu-id="4222a-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4222a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4222a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4222a-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="4222a-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="4222a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4222a-108">Property set:</span></span>  <br/> |<span data-ttu-id="4222a-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="4222a-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="4222a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4222a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4222a-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="4222a-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="4222a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4222a-112">Data type:</span></span>  <br/> |<span data-ttu-id="4222a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4222a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4222a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4222a-114">Area:</span></span>  <br/> |<span data-ttu-id="4222a-115">Journal</span><span class="sxs-lookup"><span data-stu-id="4222a-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4222a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4222a-116">Remarks</span></span>

<span data-ttu-id="4222a-117">Die Dauer in Minuten ein, der die Aktivität, die den Unterschied zwischen den **DispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) und **DispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) Eigenschaften werden muss.</span><span class="sxs-lookup"><span data-stu-id="4222a-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4222a-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4222a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4222a-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4222a-119">Protocol specifications</span></span>

<span data-ttu-id="4222a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4222a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4222a-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4222a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4222a-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4222a-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4222a-123">Gibt die Eigenschaften und Operationen, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4222a-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4222a-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4222a-124">Header files</span></span>

<span data-ttu-id="4222a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4222a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4222a-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4222a-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4222a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4222a-127">See also</span></span>



[<span data-ttu-id="4222a-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4222a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4222a-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4222a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4222a-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4222a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4222a-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4222a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


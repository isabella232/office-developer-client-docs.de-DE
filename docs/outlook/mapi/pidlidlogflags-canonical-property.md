---
title: Kanonische Pidlidlogflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336946"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="646f4-103">Kanonische Pidlidlogflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="646f4-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="646f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="646f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="646f4-105">Enthält Metadaten zum Journal.</span><span class="sxs-lookup"><span data-stu-id="646f4-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="646f4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="646f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="646f4-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="646f4-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="646f4-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="646f4-108">Property set:</span></span>  <br/> |<span data-ttu-id="646f4-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="646f4-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="646f4-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="646f4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="646f4-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="646f4-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="646f4-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="646f4-112">Data type:</span></span>  <br/> |<span data-ttu-id="646f4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="646f4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="646f4-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="646f4-114">Area:</span></span>  <br/> |<span data-ttu-id="646f4-115">Journal</span><span class="sxs-lookup"><span data-stu-id="646f4-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="646f4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="646f4-116">Remarks</span></span>

<span data-ttu-id="646f4-117">Das Bitfeld, das Metadaten zum Journal enthält, muss NULL oder "0x40000000" sein.</span><span class="sxs-lookup"><span data-stu-id="646f4-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="646f4-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="646f4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="646f4-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="646f4-119">Protocol specifications</span></span>

<span data-ttu-id="646f4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="646f4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="646f4-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="646f4-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="646f4-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="646f4-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="646f4-123">Gibt die Eigenschaften und Vorgänge an, die für Journale zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="646f4-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="646f4-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="646f4-124">Header files</span></span>

<span data-ttu-id="646f4-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="646f4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="646f4-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="646f4-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="646f4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="646f4-127">See also</span></span>



[<span data-ttu-id="646f4-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="646f4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="646f4-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="646f4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="646f4-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="646f4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="646f4-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="646f4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


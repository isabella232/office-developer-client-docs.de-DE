---
title: Kanonische PidTagFlagCompleteTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: efaa8cf84204234697431a190a5cb6745b55ecae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794360"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="e958d-103">Kanonische PidTagFlagCompleteTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e958d-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="e958d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e958d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e958d-105">Gibt das Datum und die Uhrzeit in Coordinated Universal Time (UTC), die das Objekt "Message" als abgeschlossen gekennzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e958d-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e958d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e958d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e958d-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="e958d-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="e958d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e958d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e958d-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="e958d-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="e958d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e958d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e958d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e958d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e958d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e958d-112">Area:</span></span>  <br/> |<span data-ttu-id="e958d-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="e958d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e958d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e958d-114">Remarks</span></span>

<span data-ttu-id="e958d-115">Diese Eigenschaft wird gelöscht, wenn das Objekt "Message" nicht abgeschlossen gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="e958d-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="e958d-116">Die Zeit kleinsten Auflösung muss Minuten (der Wert muss ein Vielfaches von 600,000,000).</span><span class="sxs-lookup"><span data-stu-id="e958d-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="e958d-117">Diese Eigenschaft muss nicht vorhanden, wenn das Objekt ein Objekt bezüglich Besprechungen ist und sollte nicht auf ein Task-Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e958d-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e958d-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e958d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e958d-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e958d-119">Protocol specifications</span></span>

<span data-ttu-id="e958d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e958d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e958d-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e958d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e958d-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e958d-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e958d-123">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="e958d-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e958d-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e958d-124">Header files</span></span>

<span data-ttu-id="e958d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e958d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e958d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e958d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e958d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e958d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e958d-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e958d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e958d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e958d-129">See also</span></span>



[<span data-ttu-id="e958d-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e958d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e958d-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e958d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e958d-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e958d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e958d-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e958d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

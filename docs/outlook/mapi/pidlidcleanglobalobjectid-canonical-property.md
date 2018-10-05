---
title: PidLidCleanGlobalObjectId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400217"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="27923-103">PidLidCleanGlobalObjectId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="27923-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="27923-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27923-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27923-105">Bereinigen globale **ObjectID**gibt.</span><span class="sxs-lookup"><span data-stu-id="27923-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27923-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="27923-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27923-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="27923-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="27923-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="27923-108">Property set:</span></span>  <br/> |<span data-ttu-id="27923-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="27923-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="27923-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="27923-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="27923-111">0 x 00000023</span><span class="sxs-lookup"><span data-stu-id="27923-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="27923-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="27923-112">Data type:</span></span>  <br/> |<span data-ttu-id="27923-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="27923-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="27923-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="27923-114">Area:</span></span>  <br/> |<span data-ttu-id="27923-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="27923-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27923-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27923-116">Remarks</span></span>

<span data-ttu-id="27923-117">Das Format dieser Eigenschaft ist identisch mit der **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="27923-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="27923-118">Der Wert dieser Eigenschaft muss auf den Wert der **LID_GLOBAL_OBJID**, mit Ausnahme der YH, YL, M, gleich und D Felder müssen null sein.</span><span class="sxs-lookup"><span data-stu-id="27923-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="27923-119">Alle Objekte, die auf eine Instanz einer Terminserie (einschließlich einer verwaisten Instanz) als auch der Terminserie selbst verweisen müssen den gleichen Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="27923-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27923-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="27923-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27923-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="27923-121">Protocol specifications</span></span>

<span data-ttu-id="27923-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27923-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27923-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="27923-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27923-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27923-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27923-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="27923-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27923-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="27923-126">Header files</span></span>

<span data-ttu-id="27923-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27923-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="27923-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="27923-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27923-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27923-129">See also</span></span>



[<span data-ttu-id="27923-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27923-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27923-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27923-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27923-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="27923-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27923-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="27923-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349217"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="7c60a-103">PidLidCleanGlobalObjectId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7c60a-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="7c60a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c60a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c60a-105">Gibt die bereinigende globale **ObjectID an.**</span><span class="sxs-lookup"><span data-stu-id="7c60a-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c60a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7c60a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c60a-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="7c60a-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="7c60a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="7c60a-108">Property set:</span></span>  <br/> |<span data-ttu-id="7c60a-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="7c60a-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="7c60a-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7c60a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7c60a-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="7c60a-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="7c60a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7c60a-112">Data type:</span></span>  <br/> |<span data-ttu-id="7c60a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7c60a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7c60a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7c60a-114">Area:</span></span>  <br/> |<span data-ttu-id="7c60a-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="7c60a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c60a-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c60a-116">Remarks</span></span>

<span data-ttu-id="7c60a-117">Das Format dieser Eigenschaft ist identisch mit dem von **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7c60a-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="7c60a-118">Der Wert dieser Eigenschaft muss gleich dem Wert von **LID_GLOBAL_OBJID** sein, außer die Felder YH, YL, M und D müssen null sein.</span><span class="sxs-lookup"><span data-stu-id="7c60a-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="7c60a-119">Alle Objekte, die auf eine Instanz einer Serienserie (einschließlich einer verwaisten Instanz) verweisen, sowie die Serienserie selbst haben denselben Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7c60a-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c60a-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7c60a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c60a-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7c60a-121">Protocol specifications</span></span>

<span data-ttu-id="7c60a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c60a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c60a-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7c60a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c60a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c60a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c60a-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="7c60a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c60a-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7c60a-126">Header files</span></span>

<span data-ttu-id="7c60a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c60a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c60a-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7c60a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c60a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c60a-129">See also</span></span>



[<span data-ttu-id="7c60a-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c60a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c60a-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7c60a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c60a-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7c60a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c60a-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7c60a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


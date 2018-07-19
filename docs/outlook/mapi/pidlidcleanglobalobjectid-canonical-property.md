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
ms.openlocfilehash: a784c91a04cce572c8e30085b1760c28296a1d53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19793484"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="046d7-103">PidLidCleanGlobalObjectId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="046d7-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="046d7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="046d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="046d7-105">Bereinigen globale **ObjectID**gibt.</span><span class="sxs-lookup"><span data-stu-id="046d7-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="046d7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="046d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="046d7-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="046d7-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="046d7-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="046d7-108">Property set:</span></span>  <br/> |<span data-ttu-id="046d7-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="046d7-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="046d7-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="046d7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="046d7-111">0 x 00000023</span><span class="sxs-lookup"><span data-stu-id="046d7-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="046d7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="046d7-112">Data type:</span></span>  <br/> |<span data-ttu-id="046d7-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="046d7-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="046d7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="046d7-114">Area:</span></span>  <br/> |<span data-ttu-id="046d7-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="046d7-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="046d7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="046d7-116">Remarks</span></span>

<span data-ttu-id="046d7-117">Das Format dieser Eigenschaft ist identisch mit der **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="046d7-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="046d7-118">Der Wert dieser Eigenschaft muss auf den Wert der **LID_GLOBAL_OBJID**, mit Ausnahme der YH, YL, M, gleich und D Felder müssen null sein.</span><span class="sxs-lookup"><span data-stu-id="046d7-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="046d7-119">Alle Objekte, die auf eine Instanz einer Terminserie (einschließlich einer verwaisten Instanz) als auch der Terminserie selbst verweisen müssen den gleichen Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="046d7-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="046d7-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="046d7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="046d7-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="046d7-121">Protocol specifications</span></span>

<span data-ttu-id="046d7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="046d7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="046d7-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="046d7-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="046d7-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="046d7-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="046d7-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="046d7-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="046d7-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="046d7-126">Header files</span></span>

<span data-ttu-id="046d7-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="046d7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="046d7-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="046d7-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="046d7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="046d7-129">See also</span></span>



[<span data-ttu-id="046d7-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="046d7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="046d7-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="046d7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="046d7-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="046d7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="046d7-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="046d7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


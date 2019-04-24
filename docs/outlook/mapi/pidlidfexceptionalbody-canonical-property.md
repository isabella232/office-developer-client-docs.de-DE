---
title: Kanonische Pidlidfexceptionalbody (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327461"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="ca748-103">Kanonische Pidlidfexceptionalbody (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ca748-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="ca748-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca748-105">Gibt an, dass das eingebettete Exception-Nachrichtenobjekt einen Text aufweist, der sich vom wiederkehrenden Kalenderobjekt unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="ca748-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca748-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ca748-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca748-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="ca748-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="ca748-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ca748-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca748-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ca748-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ca748-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="ca748-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ca748-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="ca748-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="ca748-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ca748-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca748-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ca748-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ca748-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ca748-114">Area:</span></span>  <br/> |<span data-ttu-id="ca748-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="ca748-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca748-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca748-116">Remarks</span></span>

<span data-ttu-id="ca748-117">Wenn der Wert dieser Eigenschaft TRUE ist, muss das eingebettete Exception-Nachrichtenobjekt einen Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca748-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="ca748-118">Wenn der Wert dieser Eigenschaft FALSE ist oder die Eigenschaft nicht vorhanden ist, muss ein Client oder Server den Text aus dem wiederkehrenden Calendar-Objekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="ca748-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca748-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ca748-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca748-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ca748-120">Protocol specifications</span></span>

<span data-ttu-id="ca748-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca748-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca748-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="ca748-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca748-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca748-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca748-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="ca748-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca748-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ca748-125">Header files</span></span>

<span data-ttu-id="ca748-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ca748-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca748-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ca748-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca748-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca748-128">See also</span></span>



[<span data-ttu-id="ca748-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca748-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca748-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca748-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca748-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ca748-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca748-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ca748-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


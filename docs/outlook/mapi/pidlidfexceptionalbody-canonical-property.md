---
title: PidLidFExceptionalBody (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393901"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="c159f-103">PidLidFExceptionalBody (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c159f-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="c159f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c159f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c159f-105">Gibt an, dass die Ausnahme eingebettete Nachricht, dass Objekt ein Body verfügt, die von sich wiederholenden Calendar-Objekt unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="c159f-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c159f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c159f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c159f-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="c159f-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="c159f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c159f-108">Property set:</span></span>  <br/> |<span data-ttu-id="c159f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c159f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c159f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="c159f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c159f-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="c159f-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="c159f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c159f-112">Data type:</span></span>  <br/> |<span data-ttu-id="c159f-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c159f-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c159f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c159f-114">Area:</span></span>  <br/> |<span data-ttu-id="c159f-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="c159f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c159f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c159f-116">Remarks</span></span>

<span data-ttu-id="c159f-117">Wenn der Wert dieser Eigenschaft auf true festgelegt ist, eingebettet die Ausnahme Meldung, dass das Objekt einen Rumpf haben muss.</span><span class="sxs-lookup"><span data-stu-id="c159f-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="c159f-118">Wenn der Wert dieser Eigenschaft auf false festgelegt ist, oder die Eigenschaft nicht vorhanden ist, muss ein Client oder Server im Textkörper von sich wiederholenden Calendar-Objekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="c159f-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c159f-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c159f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c159f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c159f-120">Protocol specifications</span></span>

<span data-ttu-id="c159f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c159f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c159f-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c159f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c159f-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c159f-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c159f-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="c159f-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c159f-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c159f-125">Header files</span></span>

<span data-ttu-id="c159f-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c159f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c159f-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c159f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c159f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c159f-128">See also</span></span>



[<span data-ttu-id="c159f-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c159f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c159f-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c159f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c159f-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c159f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c159f-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c159f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


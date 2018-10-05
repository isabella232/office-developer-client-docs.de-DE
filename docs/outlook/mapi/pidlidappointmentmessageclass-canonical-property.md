---
title: PidLidAppointmentMessageClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7149ba5a4a0378951942df790003b6d09c1155f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393418"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="883d7-103">PidLidAppointmentMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="883d7-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="883d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="883d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="883d7-105">Gibt die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Besprechung, die aus der Besprechungsanfrage generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="883d7-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="883d7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="883d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="883d7-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="883d7-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="883d7-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="883d7-108">Property set:</span></span>  <br/> |<span data-ttu-id="883d7-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="883d7-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="883d7-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="883d7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="883d7-111">0 x 00000024</span><span class="sxs-lookup"><span data-stu-id="883d7-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="883d7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="883d7-112">Data type:</span></span>  <br/> |<span data-ttu-id="883d7-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="883d7-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="883d7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="883d7-114">Area:</span></span>  <br/> |<span data-ttu-id="883d7-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="883d7-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="883d7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="883d7-116">Remarks</span></span>

<span data-ttu-id="883d7-117">Der Wert dieser Eigenschaft muss entweder "IPM. Termin"oder"IPM vorangestellt werden. Termin. ".</span><span class="sxs-lookup"><span data-stu-id="883d7-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="883d7-118">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="883d7-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="883d7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="883d7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="883d7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="883d7-120">Protocol specifications</span></span>

<span data-ttu-id="883d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="883d7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="883d7-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="883d7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="883d7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="883d7-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="883d7-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="883d7-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="883d7-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="883d7-125">Header files</span></span>

<span data-ttu-id="883d7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="883d7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="883d7-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="883d7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="883d7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="883d7-128">See also</span></span>



[<span data-ttu-id="883d7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="883d7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="883d7-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="883d7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="883d7-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="883d7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="883d7-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="883d7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


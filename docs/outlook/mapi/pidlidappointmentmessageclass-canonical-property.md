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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358100"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="672f6-103">PidLidAppointmentMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="672f6-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="672f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="672f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="672f6-105">Gibt die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft der Besprechung an, die aus der Besprechungsanfrage generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="672f6-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="672f6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="672f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="672f6-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="672f6-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="672f6-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="672f6-108">Property set:</span></span>  <br/> |<span data-ttu-id="672f6-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="672f6-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="672f6-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="672f6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="672f6-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="672f6-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="672f6-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="672f6-112">Data type:</span></span>  <br/> |<span data-ttu-id="672f6-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="672f6-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="672f6-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="672f6-114">Area:</span></span>  <br/> |<span data-ttu-id="672f6-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="672f6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="672f6-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="672f6-116">Remarks</span></span>

<span data-ttu-id="672f6-117">Der Wert dieser Eigenschaft muss entweder "IPM" sein. Appointment" oder dem Präfix "IPM. Appointment.".</span><span class="sxs-lookup"><span data-stu-id="672f6-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="672f6-118">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="672f6-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="672f6-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="672f6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="672f6-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="672f6-120">Protocol specifications</span></span>

<span data-ttu-id="672f6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="672f6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="672f6-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="672f6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="672f6-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="672f6-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="672f6-124">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="672f6-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="672f6-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="672f6-125">Header files</span></span>

<span data-ttu-id="672f6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="672f6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="672f6-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="672f6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="672f6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="672f6-128">See also</span></span>



[<span data-ttu-id="672f6-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="672f6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="672f6-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="672f6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="672f6-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="672f6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="672f6-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="672f6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


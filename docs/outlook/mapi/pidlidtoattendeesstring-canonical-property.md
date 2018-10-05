---
title: PidLidToAttendeesString (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea0cd256b025ae519272f32522bebbe6e9e17b5e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383702"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="998e4-103">PidLidToAttendeesString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="998e4-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="998e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="998e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="998e4-105">Enthält eine Liste aller sendable Teilnehmer, die auch die erforderlichen Teilnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="998e4-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="998e4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="998e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="998e4-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="998e4-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="998e4-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="998e4-108">Property set:</span></span>  <br/> |<span data-ttu-id="998e4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="998e4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="998e4-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="998e4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="998e4-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="998e4-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="998e4-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="998e4-112">Data type:</span></span>  <br/> |<span data-ttu-id="998e4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="998e4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="998e4-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="998e4-114">Area:</span></span>  <br/> |<span data-ttu-id="998e4-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="998e4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="998e4-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="998e4-116">Remarks</span></span>

<span data-ttu-id="998e4-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="998e4-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="998e4-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="998e4-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="998e4-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="998e4-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="998e4-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="998e4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="998e4-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="998e4-121">Protocol specifications</span></span>

<span data-ttu-id="998e4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="998e4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="998e4-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="998e4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="998e4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="998e4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="998e4-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="998e4-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="998e4-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="998e4-126">Header files</span></span>

<span data-ttu-id="998e4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="998e4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="998e4-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="998e4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="998e4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="998e4-129">See also</span></span>



[<span data-ttu-id="998e4-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="998e4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="998e4-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="998e4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="998e4-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="998e4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="998e4-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="998e4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


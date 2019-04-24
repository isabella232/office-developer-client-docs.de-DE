---
title: Kanonische Pidlidnonsendableto (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345517"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="b628b-103">Kanonische Pidlidnonsendableto (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b628b-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="b628b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b628b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b628b-105">Enthält eine Liste aller nicht sendenden Teilnehmer, die ebenfalls erforderliche Teilnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="b628b-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b628b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b628b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b628b-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="b628b-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="b628b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b628b-108">Property set:</span></span>  <br/> |<span data-ttu-id="b628b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b628b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b628b-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="b628b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b628b-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="b628b-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="b628b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b628b-112">Data type:</span></span>  <br/> |<span data-ttu-id="b628b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b628b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b628b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b628b-114">Area:</span></span>  <br/> |<span data-ttu-id="b628b-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="b628b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b628b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b628b-116">Remarks</span></span>

<span data-ttu-id="b628b-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="b628b-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="b628b-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen, getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="b628b-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="b628b-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b628b-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b628b-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b628b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b628b-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b628b-121">Protocol specifications</span></span>

<span data-ttu-id="b628b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b628b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b628b-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="b628b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b628b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b628b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b628b-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="b628b-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b628b-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b628b-126">Header files</span></span>

<span data-ttu-id="b628b-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b628b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b628b-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b628b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b628b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b628b-129">See also</span></span>



[<span data-ttu-id="b628b-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b628b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b628b-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b628b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b628b-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b628b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b628b-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b628b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


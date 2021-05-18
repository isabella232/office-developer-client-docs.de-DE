---
title: PidLidNonSendableBcc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBcc
api_type:
- COM
ms.assetid: c7523896-c391-443d-bd4e-cc13f3367f08
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b7cfe1fc1068e5b5b228c4de4c9317d9bcbbc66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328735"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="519d9-103">PidLidNonSendableBcc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="519d9-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="519d9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="519d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="519d9-105">Enthält eine Liste aller nicht zu unterschätzenden Teilnehmer, die Ressourcen sind.</span><span class="sxs-lookup"><span data-stu-id="519d9-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="519d9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="519d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="519d9-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="519d9-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="519d9-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="519d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="519d9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="519d9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="519d9-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="519d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="519d9-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="519d9-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="519d9-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="519d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="519d9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="519d9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="519d9-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="519d9-114">Area:</span></span>  <br/> |<span data-ttu-id="519d9-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="519d9-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="519d9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="519d9-116">Remarks</span></span>

<span data-ttu-id="519d9-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="519d9-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="519d9-118">Separate Einträge müssen durch ein Semikolon gefolgt von einem Leerzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="519d9-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="519d9-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="519d9-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="519d9-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="519d9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="519d9-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="519d9-121">Protocol specifications</span></span>

<span data-ttu-id="519d9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="519d9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="519d9-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="519d9-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="519d9-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="519d9-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="519d9-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="519d9-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="519d9-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="519d9-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="519d9-127">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="519d9-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="519d9-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="519d9-128">Header files</span></span>

<span data-ttu-id="519d9-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="519d9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="519d9-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="519d9-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="519d9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="519d9-131">See also</span></span>



[<span data-ttu-id="519d9-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="519d9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="519d9-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="519d9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="519d9-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="519d9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="519d9-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="519d9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


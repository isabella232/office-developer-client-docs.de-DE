---
title: PidLidNonSendableTo (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e4875ff12d494b1d259c4647ff925243e55ee281
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586613"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="77c17-103">PidLidNonSendableTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77c17-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="77c17-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77c17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77c17-105">Enthält eine Liste aller senden Teilnehmer, die auch die erforderlichen Teilnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="77c17-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77c17-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="77c17-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77c17-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="77c17-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="77c17-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="77c17-108">Property set:</span></span>  <br/> |<span data-ttu-id="77c17-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="77c17-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="77c17-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="77c17-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="77c17-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="77c17-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="77c17-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="77c17-112">Data type:</span></span>  <br/> |<span data-ttu-id="77c17-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="77c17-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="77c17-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="77c17-114">Area:</span></span>  <br/> |<span data-ttu-id="77c17-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="77c17-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77c17-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="77c17-116">Remarks</span></span>

<span data-ttu-id="77c17-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="77c17-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="77c17-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="77c17-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="77c17-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="77c17-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77c17-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="77c17-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77c17-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="77c17-121">Protocol specifications</span></span>

<span data-ttu-id="77c17-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77c17-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77c17-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="77c17-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="77c17-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77c17-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77c17-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="77c17-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77c17-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="77c17-126">Header files</span></span>

<span data-ttu-id="77c17-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77c17-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="77c17-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="77c17-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77c17-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77c17-129">See also</span></span>



[<span data-ttu-id="77c17-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77c17-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77c17-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77c17-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77c17-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="77c17-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77c17-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="77c17-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidLidNonSendableCc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableCc
api_type:
- COM
ms.assetid: 170afe1f-1223-4689-825c-d21ab14b213b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 76ea38db86f678c250016c2f5e2feea3a173bb5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589385"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="35911-103">PidLidNonSendableCc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35911-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="35911-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35911-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35911-105">Enthält eine Liste aller senden Teilnehmer, die auch die optionale Teilnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="35911-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35911-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="35911-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35911-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="35911-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="35911-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="35911-108">Property set:</span></span>  <br/> |<span data-ttu-id="35911-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="35911-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="35911-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="35911-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="35911-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="35911-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="35911-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="35911-112">Data type:</span></span>  <br/> |<span data-ttu-id="35911-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35911-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="35911-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="35911-114">Area:</span></span>  <br/> |<span data-ttu-id="35911-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="35911-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35911-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="35911-116">Remarks</span></span>

<span data-ttu-id="35911-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="35911-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="35911-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="35911-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="35911-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="35911-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35911-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35911-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35911-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="35911-121">Protocol specifications</span></span>

<span data-ttu-id="35911-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35911-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35911-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="35911-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35911-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35911-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35911-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="35911-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="35911-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35911-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35911-127">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="35911-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35911-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="35911-128">Header files</span></span>

<span data-ttu-id="35911-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35911-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="35911-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="35911-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35911-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35911-131">See also</span></span>



[<span data-ttu-id="35911-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35911-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35911-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35911-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35911-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="35911-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35911-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="35911-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


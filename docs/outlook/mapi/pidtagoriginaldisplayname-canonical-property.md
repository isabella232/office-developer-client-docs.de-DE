---
title: PidTagOriginalDisplayName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4a43bc33f13d8325a55d09b5ef3031dc632cf587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794682"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="06671-103">PidTagOriginalDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="06671-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="06671-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06671-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06671-105">Enthält den ursprünglichen Anzeigenamen für einen Eintrag aus einem Adressbuch in ein persönliches Adressbuch oder anderen beschreibbaren des Adressbuchs kopiert.</span><span class="sxs-lookup"><span data-stu-id="06671-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06671-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="06671-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06671-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="06671-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="06671-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="06671-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06671-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="06671-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="06671-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="06671-110">Data type:</span></span>  <br/> |<span data-ttu-id="06671-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06671-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="06671-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="06671-112">Area:</span></span>  <br/> |<span data-ttu-id="06671-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="06671-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06671-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06671-114">Remarks</span></span>

<span data-ttu-id="06671-115">Diese Eigenschaften enthalten Informationen zu der ursprünglichen Quelle des kopierten-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="06671-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="06671-116">Bei einem Bericht nonread enthalten diese Eigenschaften eine Kopie des Anzeigenamens von der ursprünglichen Empfänger der Nachricht für den der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="06671-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="06671-117">Wenn Sie der ursprüngliche Empfänger einer Verteilerliste gehört, wird der Anzeigename der Verteilerliste für den Bericht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="06671-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="06671-118">Diese Eigenschaften können eine Clientanwendung um Änderung oder "spoofing" von Einträgen, zu verhindern, indem Sie eine unveränderte Kopie des Anzeigenamens zum Vergleichen von eigenständigen erteilen.</span><span class="sxs-lookup"><span data-stu-id="06671-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06671-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="06671-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06671-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="06671-120">Protocol specifications</span></span>

<span data-ttu-id="06671-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06671-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06671-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="06671-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06671-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06671-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06671-124">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="06671-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06671-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="06671-125">Header files</span></span>

<span data-ttu-id="06671-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06671-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="06671-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="06671-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="06671-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06671-128">Mapitags.h</span></span>
  
> <span data-ttu-id="06671-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="06671-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06671-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06671-130">See also</span></span>



[<span data-ttu-id="06671-131">PidTagTransmittableDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="06671-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="06671-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06671-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06671-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06671-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06671-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="06671-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06671-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="06671-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


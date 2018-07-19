---
title: PidTagListSubscribe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5030e48ac87408f983696a365d3234c3362346c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794573"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="4a968-103">PidTagListSubscribe (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4a968-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="4a968-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a968-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a968-105">Enthält den Wert der Liste abonnieren Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="4a968-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a968-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4a968-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a968-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="4a968-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="4a968-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4a968-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a968-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="4a968-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="4a968-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4a968-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a968-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a968-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a968-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4a968-112">Area:</span></span>  <br/> |<span data-ttu-id="4a968-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="4a968-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a968-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a968-114">Remarks</span></span>

<span data-ttu-id="4a968-115">Um eine Liste abonnieren Kopfzeilenfeld generiert werden soll, müssen die Clients den Wert dieser Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="4a968-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="4a968-116">MIME-Writer müssen den Wert dieser Eigenschaften in der Liste abonnieren Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="4a968-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="4a968-117">Wenn den Wert der Eigenschaften dieser Art Server-bezogene festlegen möchten, müssen MIME-Clients die Kopfzeile Felder wie in der folgenden Tabelle angegebenen schreiben.</span><span class="sxs-lookup"><span data-stu-id="4a968-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="4a968-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4a968-118">**Property**</span></span>|<span data-ttu-id="4a968-119">**Bevorzugte Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="4a968-119">**Preferred header field name**</span></span>|<span data-ttu-id="4a968-120">**Alternative Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="4a968-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4a968-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="4a968-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="4a968-122">Liste abonnieren</span><span class="sxs-lookup"><span data-stu-id="4a968-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="4a968-123">Abonnieren von X-Liste</span><span class="sxs-lookup"><span data-stu-id="4a968-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4a968-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4a968-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a968-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4a968-125">Protocol specifications</span></span>

<span data-ttu-id="4a968-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a968-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a968-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4a968-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a968-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a968-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a968-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="4a968-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a968-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4a968-130">Header files</span></span>

<span data-ttu-id="4a968-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a968-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a968-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4a968-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a968-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a968-133">Mapitags.h</span></span>
  
> <span data-ttu-id="4a968-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4a968-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a968-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a968-135">See also</span></span>



[<span data-ttu-id="4a968-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a968-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a968-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a968-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a968-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4a968-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a968-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4a968-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


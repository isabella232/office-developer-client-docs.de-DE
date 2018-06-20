---
title: Kanonische PidTagListSubscribe-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5030e48ac87408f983696a365d3234c3362346c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794573"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="5b7bf-103">Kanonische PidTagListSubscribe-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b7bf-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="5b7bf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b7bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b7bf-105">Enthält den Wert der Liste abonnieren Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="5b7bf-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b7bf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b7bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b7bf-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="5b7bf-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="5b7bf-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5b7bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b7bf-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="5b7bf-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="5b7bf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b7bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b7bf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5b7bf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5b7bf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b7bf-112">Area:</span></span>  <br/> |<span data-ttu-id="5b7bf-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="5b7bf-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b7bf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b7bf-114">Remarks</span></span>

<span data-ttu-id="5b7bf-115">Um eine Liste abonnieren Kopfzeilenfeld generiert werden soll, müssen die Clients den Wert dieser Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="5b7bf-116">MIME-Writer müssen den Wert dieser Eigenschaften in der Liste abonnieren Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="5b7bf-117">Wenn den Wert der Eigenschaften dieser Art Server-bezogene festlegen möchten, müssen MIME-Clients die Kopfzeile Felder wie in der folgenden Tabelle angegebenen schreiben.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="5b7bf-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="5b7bf-118">**Property**</span></span>|<span data-ttu-id="5b7bf-119">**Bevorzugte Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="5b7bf-119">**Preferred header field name**</span></span>|<span data-ttu-id="5b7bf-120">**Alternative Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="5b7bf-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b7bf-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="5b7bf-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="5b7bf-122">Liste abonnieren</span><span class="sxs-lookup"><span data-stu-id="5b7bf-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="5b7bf-123">Abonnieren von X-Liste</span><span class="sxs-lookup"><span data-stu-id="5b7bf-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5b7bf-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b7bf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b7bf-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5b7bf-125">Protocol specifications</span></span>

<span data-ttu-id="5b7bf-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7bf-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7bf-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b7bf-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b7bf-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b7bf-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b7bf-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5b7bf-130">Header files</span></span>

<span data-ttu-id="5b7bf-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b7bf-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b7bf-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b7bf-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5b7bf-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5b7bf-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5b7bf-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b7bf-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b7bf-135">See also</span></span>



[<span data-ttu-id="5b7bf-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b7bf-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b7bf-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b7bf-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b7bf-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b7bf-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b7bf-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b7bf-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


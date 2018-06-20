---
title: Kanonische PidTagListHelp-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794580"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="d372a-103">Kanonische PidTagListHelp-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d372a-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="d372a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d372a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d372a-105">Enthält den Wert der Liste-Hilfe-Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="d372a-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d372a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d372a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d372a-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="d372a-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="d372a-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="d372a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d372a-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="d372a-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="d372a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d372a-110">Data type:</span></span>  <br/> |<span data-ttu-id="d372a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d372a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d372a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d372a-112">Area:</span></span>  <br/> |<span data-ttu-id="d372a-113">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="d372a-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d372a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d372a-114">Remarks</span></span>

<span data-ttu-id="d372a-115">Um eine Liste Hilfe Kopfzeilenfeld generiert werden soll, müssen die Clients den Wert **PR_LIST_HELP** oder eine zugeordnete Eigenschaft auf den gewünschten Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d372a-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="d372a-116">MIME-Autoren müssen diesen Wert in der Liste Hilfe Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="d372a-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="d372a-117">Wenn den Wert dieser Liste Server-bezogene Eigenschaften festlegen möchten, müssen MIME-Clients die Kopfzeile Felder wie in der folgenden Tabelle angegebenen schreiben:</span><span class="sxs-lookup"><span data-stu-id="d372a-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="d372a-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="d372a-118">**Property**</span></span>|<span data-ttu-id="d372a-119">**Bevorzugte Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="d372a-119">**Preferred header field name**</span></span>|<span data-ttu-id="d372a-120">**Alternative Header-Feldname**</span><span class="sxs-lookup"><span data-stu-id="d372a-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d372a-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="d372a-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="d372a-122">Liste-Hilfe</span><span class="sxs-lookup"><span data-stu-id="d372a-122">List-Help</span></span>  <br/> |<span data-ttu-id="d372a-123">X-Liste-Hilfe</span><span class="sxs-lookup"><span data-stu-id="d372a-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d372a-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d372a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d372a-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d372a-125">Protocol specifications</span></span>

<span data-ttu-id="d372a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d372a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d372a-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d372a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d372a-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d372a-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d372a-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="d372a-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d372a-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d372a-130">Header files</span></span>

<span data-ttu-id="d372a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d372a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d372a-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d372a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d372a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d372a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d372a-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d372a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d372a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d372a-135">See also</span></span>



[<span data-ttu-id="d372a-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d372a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d372a-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d372a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d372a-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d372a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d372a-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d372a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


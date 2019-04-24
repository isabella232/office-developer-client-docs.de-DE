---
title: Kanonische Pidtaglisthelp (-Eigenschaft
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
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279629"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="a54cb-103">Kanonische Pidtaglisthelp (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a54cb-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="a54cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a54cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a54cb-105">Enthält den Wert des Listen Hilfe-Headerfelds für MIME-Nachrichten (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="a54cb-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a54cb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a54cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a54cb-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="a54cb-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="a54cb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a54cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a54cb-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="a54cb-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="a54cb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a54cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a54cb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a54cb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a54cb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a54cb-112">Area:</span></span>  <br/> |<span data-ttu-id="a54cb-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="a54cb-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a54cb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a54cb-114">Remarks</span></span>

<span data-ttu-id="a54cb-115">Um ein Listen Hilfe-Kopfzeilenfeld zu generieren, müssen Clients den Wert von **PR_LIST_HELP** oder eine zugeordnete Eigenschaft auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="a54cb-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="a54cb-116">MIME-Writer müssen diesen Wert in das Kopfzeilenfeld List-Help kopieren.</span><span class="sxs-lookup"><span data-stu-id="a54cb-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="a54cb-117">Um den Wert dieser Listenserver bezogenen Eigenschaften festzulegen, müssen MIME-Clients die Kopfzeilenfelder wie in der folgenden Tabelle angegeben schreiben:</span><span class="sxs-lookup"><span data-stu-id="a54cb-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="a54cb-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="a54cb-118">**Property**</span></span>|<span data-ttu-id="a54cb-119">**Bevorzugter Kopfzeilen Feldname**</span><span class="sxs-lookup"><span data-stu-id="a54cb-119">**Preferred header field name**</span></span>|<span data-ttu-id="a54cb-120">**Name des alternativen Kopfzeilenfelds**</span><span class="sxs-lookup"><span data-stu-id="a54cb-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a54cb-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="a54cb-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="a54cb-122">List-Hilfe</span><span class="sxs-lookup"><span data-stu-id="a54cb-122">List-Help</span></span>  <br/> |<span data-ttu-id="a54cb-123">X-List-Hilfe</span><span class="sxs-lookup"><span data-stu-id="a54cb-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a54cb-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a54cb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a54cb-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a54cb-125">Protocol specifications</span></span>

<span data-ttu-id="a54cb-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a54cb-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a54cb-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a54cb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a54cb-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a54cb-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a54cb-129">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="a54cb-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a54cb-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a54cb-130">Header files</span></span>

<span data-ttu-id="a54cb-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a54cb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a54cb-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a54cb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a54cb-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a54cb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a54cb-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a54cb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a54cb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a54cb-135">See also</span></span>



[<span data-ttu-id="a54cb-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a54cb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a54cb-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a54cb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a54cb-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a54cb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a54cb-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a54cb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


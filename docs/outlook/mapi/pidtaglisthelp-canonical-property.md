---
title: PidTagListHelp (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279629"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="43b20-103">PidTagListHelp (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43b20-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="43b20-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b20-105">Enthält den Wert einer MIME-Nachricht (Multipurpose Internet Mail Extensions) List-Help Kopfzeilenfeld.</span><span class="sxs-lookup"><span data-stu-id="43b20-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43b20-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="43b20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43b20-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="43b20-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="43b20-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="43b20-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43b20-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="43b20-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="43b20-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="43b20-110">Data type:</span></span>  <br/> |<span data-ttu-id="43b20-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43b20-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="43b20-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="43b20-112">Area:</span></span>  <br/> |<span data-ttu-id="43b20-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="43b20-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43b20-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43b20-114">Remarks</span></span>

<span data-ttu-id="43b20-115">Um ein List-Help zu generieren, müssen Clients  den Wert einer PR_LIST_HELP oder einer zugeordneten Eigenschaft auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="43b20-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="43b20-116">MIME-Writer müssen diesen Wert in das List-Help kopieren.</span><span class="sxs-lookup"><span data-stu-id="43b20-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="43b20-117">Um den Wert dieser listenserverbezogenen Eigenschaften festlegen zu können, müssen MIME-Clients die Kopfzeilenfelder wie in der folgenden Tabelle angegeben schreiben:</span><span class="sxs-lookup"><span data-stu-id="43b20-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="43b20-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="43b20-118">**Property**</span></span>|<span data-ttu-id="43b20-119">**Name des bevorzugten Kopfzeilenfelds**</span><span class="sxs-lookup"><span data-stu-id="43b20-119">**Preferred header field name**</span></span>|<span data-ttu-id="43b20-120">**Alternativer Kopfzeilenfeldname**</span><span class="sxs-lookup"><span data-stu-id="43b20-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43b20-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="43b20-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="43b20-122">List-Help</span><span class="sxs-lookup"><span data-stu-id="43b20-122">List-Help</span></span>  <br/> |<span data-ttu-id="43b20-123">X-List-Help</span><span class="sxs-lookup"><span data-stu-id="43b20-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="43b20-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43b20-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43b20-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="43b20-125">Protocol specifications</span></span>

<span data-ttu-id="43b20-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43b20-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43b20-127">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="43b20-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43b20-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43b20-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43b20-129">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="43b20-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43b20-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="43b20-130">Header files</span></span>

<span data-ttu-id="43b20-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43b20-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="43b20-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="43b20-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="43b20-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43b20-133">Mapitags.h</span></span>
  
> <span data-ttu-id="43b20-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="43b20-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43b20-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43b20-135">See also</span></span>



[<span data-ttu-id="43b20-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43b20-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43b20-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="43b20-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43b20-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="43b20-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43b20-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="43b20-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


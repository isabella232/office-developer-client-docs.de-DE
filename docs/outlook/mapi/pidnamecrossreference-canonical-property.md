---
title: Kanonische Pidnamecrossreference (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331444"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="5d53a-103">Kanonische Pidnamecrossreference (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5d53a-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="5d53a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d53a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d53a-105">Enthält einen [RFC3282] XREF-Kopfzeilen Feldwert.</span><span class="sxs-lookup"><span data-stu-id="5d53a-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d53a-106">Angezeigte Namen:</span><span class="sxs-lookup"><span data-stu-id="5d53a-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="5d53a-107">Keine</span><span class="sxs-lookup"><span data-stu-id="5d53a-107">None</span></span>  <br/> |
|<span data-ttu-id="5d53a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="5d53a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5d53a-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5d53a-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="5d53a-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="5d53a-110">Property name:</span></span>  <br/> |<span data-ttu-id="5d53a-111">XREF</span><span class="sxs-lookup"><span data-stu-id="5d53a-111">Xref</span></span>  <br/> |
|<span data-ttu-id="5d53a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5d53a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5d53a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5d53a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5d53a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5d53a-114">Area:</span></span>  <br/> |<span data-ttu-id="5d53a-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="5d53a-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d53a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d53a-116">Remarks</span></span>

<span data-ttu-id="5d53a-117">Um den Wert dieser Eigenschaft festzulegen, müssen Multipurpose Internet Message Extensions (MIME)-Clients den gewünschten Wert in ein XRef-Kopfzeilenfeld schreiben.</span><span class="sxs-lookup"><span data-stu-id="5d53a-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="5d53a-118">MIME-Leser müssen den Wert eines XRef-Kopfzeilenfelds in den Wert dieser Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="5d53a-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d53a-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d53a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d53a-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5d53a-120">Protocol specifications</span></span>

<span data-ttu-id="5d53a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d53a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d53a-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="5d53a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d53a-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d53a-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d53a-124">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5d53a-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d53a-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5d53a-125">Header files</span></span>

<span data-ttu-id="5d53a-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5d53a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d53a-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5d53a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d53a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d53a-128">See also</span></span>



[<span data-ttu-id="5d53a-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d53a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d53a-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d53a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d53a-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5d53a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d53a-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5d53a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


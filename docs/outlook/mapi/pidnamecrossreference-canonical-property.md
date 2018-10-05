---
title: PidNameCrossReference (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382498"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="54ad0-103">PidNameCrossReference (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="54ad0-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="54ad0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ad0-105">Enthält einen [RFC3282] Xref Kopfzeile der Wert des Felds.</span><span class="sxs-lookup"><span data-stu-id="54ad0-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54ad0-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="54ad0-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="54ad0-107">Keine</span><span class="sxs-lookup"><span data-stu-id="54ad0-107">None</span></span>  <br/> |
|<span data-ttu-id="54ad0-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="54ad0-108">Property set:</span></span>  <br/> |<span data-ttu-id="54ad0-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="54ad0-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="54ad0-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="54ad0-110">Property name:</span></span>  <br/> |<span data-ttu-id="54ad0-111">XRef</span><span class="sxs-lookup"><span data-stu-id="54ad0-111">Xref</span></span>  <br/> |
|<span data-ttu-id="54ad0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="54ad0-112">Data type:</span></span>  <br/> |<span data-ttu-id="54ad0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54ad0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="54ad0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="54ad0-114">Area:</span></span>  <br/> |<span data-ttu-id="54ad0-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="54ad0-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54ad0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54ad0-116">Remarks</span></span>

<span data-ttu-id="54ad0-117">Um den Wert dieser Eigenschaft festzulegen, müssen den gewünschten Wert Multipurpose Internet Message Extensions (MIME)-Clients in einer XRef Kopfzeilenfeld geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="54ad0-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="54ad0-118">MIME-Leser müssen auf den Wert dieser Eigenschaft den Wert eines Felds Kopfzeile XRef kopieren.</span><span class="sxs-lookup"><span data-stu-id="54ad0-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54ad0-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="54ad0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54ad0-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="54ad0-120">Protocol specifications</span></span>

<span data-ttu-id="54ad0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54ad0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54ad0-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="54ad0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54ad0-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54ad0-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54ad0-124">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="54ad0-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54ad0-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="54ad0-125">Header files</span></span>

<span data-ttu-id="54ad0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54ad0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="54ad0-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="54ad0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54ad0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54ad0-128">See also</span></span>



[<span data-ttu-id="54ad0-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ad0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54ad0-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ad0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54ad0-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="54ad0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54ad0-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="54ad0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


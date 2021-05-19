---
title: PidNameContentClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356350"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="ee500-103">PidNameContentClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee500-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="ee500-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee500-105">Enthält einen [RFC3282] Content-Class-Headerfeldwert.</span><span class="sxs-lookup"><span data-stu-id="ee500-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee500-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="ee500-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ee500-107">Keine</span><span class="sxs-lookup"><span data-stu-id="ee500-107">None</span></span>  <br/> |
|<span data-ttu-id="ee500-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ee500-108">Property set:</span></span>  <br/> |<span data-ttu-id="ee500-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ee500-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="ee500-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="ee500-110">Property name:</span></span>  <br/> |<span data-ttu-id="ee500-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="ee500-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="ee500-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ee500-112">Data type:</span></span>  <br/> |<span data-ttu-id="ee500-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee500-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee500-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ee500-114">Area:</span></span>  <br/> |<span data-ttu-id="ee500-115">E-Mails</span><span class="sxs-lookup"><span data-stu-id="ee500-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee500-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee500-116">Remarks</span></span>

<span data-ttu-id="ee500-117">Um den Wert dieser Eigenschaft festlegen zu können, müssen Multipurpose Internet Message Extensions (MIME)-Clients ein Content-Class-Headerfeld mit dem gewünschten Wert schreiben.</span><span class="sxs-lookup"><span data-stu-id="ee500-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="ee500-118">MIME-Reader müssen den Wert eines Content-Class-Headerfelds in den Wert dieser Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="ee500-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee500-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee500-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee500-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ee500-120">Protocol specifications</span></span>

<span data-ttu-id="ee500-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee500-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee500-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ee500-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee500-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee500-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee500-124">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="ee500-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ee500-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee500-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee500-126">Gibt die Eigenschaften von mit Rechten verwalteten codierten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="ee500-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee500-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ee500-127">Header files</span></span>

<span data-ttu-id="ee500-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee500-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee500-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ee500-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee500-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee500-130">See also</span></span>



[<span data-ttu-id="ee500-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee500-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee500-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ee500-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee500-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ee500-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee500-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ee500-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


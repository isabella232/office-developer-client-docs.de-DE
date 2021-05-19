---
title: PidNameContentBase (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331500"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="49584-103">PidNameContentBase (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="49584-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="49584-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49584-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49584-105">Enthält einen [RFC3282] Content-Base-Headerfeldwert.</span><span class="sxs-lookup"><span data-stu-id="49584-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="49584-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="49584-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="49584-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="49584-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="49584-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="49584-108">Property set:</span></span>  <br/> |<span data-ttu-id="49584-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="49584-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="49584-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="49584-110">Property name:</span></span>  <br/> |<span data-ttu-id="49584-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="49584-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="49584-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="49584-112">Data type:</span></span>  <br/> |<span data-ttu-id="49584-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="49584-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="49584-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="49584-114">Area:</span></span>  <br/> |<span data-ttu-id="49584-115">E-Mails</span><span class="sxs-lookup"><span data-stu-id="49584-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49584-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49584-116">Remarks</span></span>

<span data-ttu-id="49584-117">Um den Wert dieser Eigenschaft festlegen zu können, müssen Multipurpose Internet Message Extensions (MIME)-Clients den gewünschten Wert in ein Content-Base-Kopfzeilenfeld für eine MIME-Entität schreiben, die einem Nachrichtentext zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="49584-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="49584-118">MIME-Reader müssen den Wert eines Content-Base-Kopfzeilenfelds für eine solche MIME-Entität in den Wert dieser Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="49584-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="49584-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="49584-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="49584-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="49584-120">Protocol specifications</span></span>

<span data-ttu-id="49584-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49584-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49584-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="49584-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="49584-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="49584-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="49584-124">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="49584-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="49584-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="49584-125">Header files</span></span>

<span data-ttu-id="49584-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="49584-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="49584-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="49584-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="49584-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49584-128">See also</span></span>



[<span data-ttu-id="49584-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49584-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="49584-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="49584-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="49584-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="49584-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="49584-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="49584-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidNameAcceptLanguage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d2c2fb31b722e76034b08077632c817d6adde802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793924"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="3097c-103">PidNameAcceptLanguage (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3097c-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="3097c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3097c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3097c-105">Einen Wert für [RFC3282] Accept-Language-Header Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="3097c-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3097c-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="3097c-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3097c-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3097c-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="3097c-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="3097c-108">Property set:</span></span>  <br/> |<span data-ttu-id="3097c-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="3097c-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="3097c-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="3097c-110">Property name:</span></span>  <br/> |<span data-ttu-id="3097c-111">Akzeptieren Sie Sprache</span><span class="sxs-lookup"><span data-stu-id="3097c-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="3097c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3097c-112">Data type:</span></span>  <br/> |<span data-ttu-id="3097c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3097c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3097c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3097c-114">Area:</span></span>  <br/> |<span data-ttu-id="3097c-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="3097c-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3097c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3097c-116">Remarks</span></span>

<span data-ttu-id="3097c-117">Um den Wert dieser Eigenschaft festzulegen, sollte ein Accept-Language-Header-Feld mit den gewünschten Wert Multipurpose Internet Message Extensions (MIME) Clients geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3097c-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="3097c-118">MIME-Clients können stattdessen ein Kopfzeilenfeld X akzeptieren Sprache schreiben.</span><span class="sxs-lookup"><span data-stu-id="3097c-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="3097c-119">MIME-Leser sollten auf den Wert dieser Eigenschaft den Wert der entweder Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="3097c-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="3097c-120">Wenn beide Kopffelder vorhanden sind, sollten MIME-Leser das Accept-Language-Header-Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="3097c-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3097c-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3097c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3097c-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3097c-122">Protocol specifications</span></span>

<span data-ttu-id="3097c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3097c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3097c-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3097c-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3097c-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3097c-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3097c-126">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="3097c-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3097c-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3097c-127">Header files</span></span>

<span data-ttu-id="3097c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3097c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="3097c-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3097c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3097c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3097c-130">See also</span></span>



[<span data-ttu-id="3097c-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3097c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3097c-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3097c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3097c-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3097c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3097c-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3097c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


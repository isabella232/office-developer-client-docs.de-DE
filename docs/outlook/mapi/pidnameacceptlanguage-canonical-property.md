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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387244"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="dd56e-103">PidNameAcceptLanguage (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dd56e-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="dd56e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd56e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd56e-105">Einen Wert für [RFC3282] Accept-Language-Header Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="dd56e-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd56e-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="dd56e-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="dd56e-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="dd56e-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="dd56e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="dd56e-108">Property set:</span></span>  <br/> |<span data-ttu-id="dd56e-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="dd56e-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="dd56e-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="dd56e-110">Property name:</span></span>  <br/> |<span data-ttu-id="dd56e-111">Akzeptieren Sie Sprache</span><span class="sxs-lookup"><span data-stu-id="dd56e-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="dd56e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dd56e-112">Data type:</span></span>  <br/> |<span data-ttu-id="dd56e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd56e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dd56e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dd56e-114">Area:</span></span>  <br/> |<span data-ttu-id="dd56e-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="dd56e-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd56e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd56e-116">Remarks</span></span>

<span data-ttu-id="dd56e-117">Um den Wert dieser Eigenschaft festzulegen, sollte ein Accept-Language-Header-Feld mit den gewünschten Wert Multipurpose Internet Message Extensions (MIME) Clients geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd56e-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="dd56e-118">MIME-Clients können stattdessen ein Kopfzeilenfeld X akzeptieren Sprache schreiben.</span><span class="sxs-lookup"><span data-stu-id="dd56e-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="dd56e-119">MIME-Leser sollten auf den Wert dieser Eigenschaft den Wert der entweder Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="dd56e-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="dd56e-120">Wenn beide Kopffelder vorhanden sind, sollten MIME-Leser das Accept-Language-Header-Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd56e-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd56e-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd56e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd56e-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dd56e-122">Protocol specifications</span></span>

<span data-ttu-id="dd56e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd56e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd56e-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dd56e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd56e-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd56e-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd56e-126">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="dd56e-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd56e-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dd56e-127">Header files</span></span>

<span data-ttu-id="dd56e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd56e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd56e-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dd56e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd56e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd56e-130">See also</span></span>



[<span data-ttu-id="dd56e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd56e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd56e-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd56e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd56e-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dd56e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd56e-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dd56e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


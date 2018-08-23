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
ms.openlocfilehash: f66a570273d78f63ced110a4bdc8a12a49c531b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595244"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="fd627-103">PidNameAcceptLanguage (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fd627-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="fd627-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd627-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd627-105">Einen Wert für [RFC3282] Accept-Language-Header Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="fd627-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd627-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="fd627-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="fd627-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="fd627-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="fd627-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fd627-108">Property set:</span></span>  <br/> |<span data-ttu-id="fd627-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="fd627-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="fd627-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="fd627-110">Property name:</span></span>  <br/> |<span data-ttu-id="fd627-111">Akzeptieren Sie Sprache</span><span class="sxs-lookup"><span data-stu-id="fd627-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="fd627-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fd627-112">Data type:</span></span>  <br/> |<span data-ttu-id="fd627-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd627-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fd627-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fd627-114">Area:</span></span>  <br/> |<span data-ttu-id="fd627-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="fd627-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd627-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fd627-116">Remarks</span></span>

<span data-ttu-id="fd627-117">Um den Wert dieser Eigenschaft festzulegen, sollte ein Accept-Language-Header-Feld mit den gewünschten Wert Multipurpose Internet Message Extensions (MIME) Clients geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fd627-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="fd627-118">MIME-Clients können stattdessen ein Kopfzeilenfeld X akzeptieren Sprache schreiben.</span><span class="sxs-lookup"><span data-stu-id="fd627-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="fd627-119">MIME-Leser sollten auf den Wert dieser Eigenschaft den Wert der entweder Kopfzeilenfeld kopieren.</span><span class="sxs-lookup"><span data-stu-id="fd627-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="fd627-120">Wenn beide Kopffelder vorhanden sind, sollten MIME-Leser das Accept-Language-Header-Feld verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd627-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd627-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fd627-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd627-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fd627-122">Protocol specifications</span></span>

<span data-ttu-id="fd627-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd627-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd627-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fd627-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd627-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd627-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd627-126">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="fd627-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd627-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fd627-127">Header files</span></span>

<span data-ttu-id="fd627-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd627-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd627-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fd627-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd627-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd627-130">See also</span></span>



[<span data-ttu-id="fd627-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd627-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd627-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd627-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd627-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fd627-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd627-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fd627-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


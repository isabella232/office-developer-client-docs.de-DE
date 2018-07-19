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
ms.openlocfilehash: 21469b944bb2ce5db0576e40012335d89d48cb49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793982"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="f04f2-103">PidNameContentBase (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f04f2-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="f04f2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f04f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f04f2-105">Einen Wert für [RFC3282] Content-Base Kopfzeile Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="f04f2-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f04f2-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="f04f2-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="f04f2-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="f04f2-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="f04f2-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f04f2-108">Property set:</span></span>  <br/> |<span data-ttu-id="f04f2-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="f04f2-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="f04f2-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="f04f2-110">Property name:</span></span>  <br/> |<span data-ttu-id="f04f2-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="f04f2-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="f04f2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f04f2-112">Data type:</span></span>  <br/> |<span data-ttu-id="f04f2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f04f2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f04f2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f04f2-114">Area:</span></span>  <br/> |<span data-ttu-id="f04f2-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f04f2-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f04f2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f04f2-116">Remarks</span></span>

<span data-ttu-id="f04f2-117">Um den Wert dieser Eigenschaft festzulegen, müssen Multipurpose Internet Message Extensions (MIME) Clients den gewünschten Wert in ein Kopfzeilenfeld Content-Base auf eine Entität MIME geschrieben werden, die Textkörper einer Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f04f2-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="f04f2-118">MIME-Leser müssen auf den Wert dieser Eigenschaft den Wert eines Felds Header Content-Base für solche eine MIME-Entität kopieren.</span><span class="sxs-lookup"><span data-stu-id="f04f2-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f04f2-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f04f2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f04f2-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f04f2-120">Protocol specifications</span></span>

<span data-ttu-id="f04f2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f04f2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f04f2-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f04f2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f04f2-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f04f2-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f04f2-124">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="f04f2-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f04f2-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f04f2-125">Header files</span></span>

<span data-ttu-id="f04f2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f04f2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f04f2-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f04f2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f04f2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f04f2-128">See also</span></span>



[<span data-ttu-id="f04f2-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f04f2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f04f2-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f04f2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f04f2-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f04f2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f04f2-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f04f2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


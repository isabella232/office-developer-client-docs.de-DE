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
ms.openlocfilehash: 20dcef118a5e3f513f8330802684a59f0f0dcf73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565347"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="6a046-103">PidNameContentClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6a046-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="6a046-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a046-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a046-105">Einen Wert für [RFC3282] Content-Class Kopfzeile Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="6a046-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a046-106">Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="6a046-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="6a046-107">Keine</span><span class="sxs-lookup"><span data-stu-id="6a046-107">None</span></span>  <br/> |
|<span data-ttu-id="6a046-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6a046-108">Property set:</span></span>  <br/> |<span data-ttu-id="6a046-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="6a046-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="6a046-110">Name der Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="6a046-110">Property name:</span></span>  <br/> |<span data-ttu-id="6a046-111">"Content-Class"</span><span class="sxs-lookup"><span data-stu-id="6a046-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="6a046-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6a046-112">Data type:</span></span>  <br/> |<span data-ttu-id="6a046-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a046-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6a046-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6a046-114">Area:</span></span>  <br/> |<span data-ttu-id="6a046-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="6a046-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a046-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6a046-116">Remarks</span></span>

<span data-ttu-id="6a046-117">Um den Wert dieser Eigenschaft festzulegen, müssen ein Kopfzeilenfeld Content-Class mit den gewünschten Wert Multipurpose Internet Message Extensions (MIME) Clients geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6a046-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="6a046-118">MIME-Leser müssen den Wert eines Felds Header Content-Class auf den Wert dieser Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="6a046-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6a046-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a046-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a046-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6a046-120">Protocol specifications</span></span>

<span data-ttu-id="6a046-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a046-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a046-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6a046-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a046-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a046-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a046-124">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="6a046-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6a046-125">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a046-125">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a046-126">Gibt die Eigenschaften der codierten Nachrichten, deren Rechte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6a046-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a046-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6a046-127">Header files</span></span>

<span data-ttu-id="6a046-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a046-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a046-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6a046-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a046-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a046-130">See also</span></span>



[<span data-ttu-id="6a046-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a046-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a046-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a046-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a046-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6a046-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a046-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6a046-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


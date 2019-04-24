---
title: Kanonische Pidnamecontentclass (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356350"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="ecb9a-103">Kanonische Pidnamecontentclass (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ecb9a-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="ecb9a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb9a-105">Enthält einen [RFC3282] Content-Class-Header Feldwert.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecb9a-106">Angezeigte Namen:</span><span class="sxs-lookup"><span data-stu-id="ecb9a-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ecb9a-107">Keine</span><span class="sxs-lookup"><span data-stu-id="ecb9a-107">None</span></span>  <br/> |
|<span data-ttu-id="ecb9a-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="ecb9a-108">Property set:</span></span>  <br/> |<span data-ttu-id="ecb9a-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ecb9a-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="ecb9a-110">Eigenschaftsname:</span><span class="sxs-lookup"><span data-stu-id="ecb9a-110">Property name:</span></span>  <br/> |<span data-ttu-id="ecb9a-111">Inhaltsklasse</span><span class="sxs-lookup"><span data-stu-id="ecb9a-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="ecb9a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ecb9a-112">Data type:</span></span>  <br/> |<span data-ttu-id="ecb9a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecb9a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ecb9a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ecb9a-114">Area:</span></span>  <br/> |<span data-ttu-id="ecb9a-115">E-Mail</span><span class="sxs-lookup"><span data-stu-id="ecb9a-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecb9a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecb9a-116">Remarks</span></span>

<span data-ttu-id="ecb9a-117">Um den Wert dieser Eigenschaft festzulegen, müssen Multipurpose Internet Message Extensions (MIME)-Clients ein Content-Class-Kopfzeilenfeld mit dem gewünschten Wert schreiben.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="ecb9a-118">MIME-Leser müssen den Wert eines Kopfzeilenfelds der Inhaltsklasse in den Wert dieser Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ecb9a-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ecb9a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecb9a-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ecb9a-120">Protocol specifications</span></span>

<span data-ttu-id="ecb9a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecb9a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecb9a-122">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecb9a-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecb9a-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecb9a-124">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ecb9a-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecb9a-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecb9a-126">Gibt die Eigenschaften von Nachrichten mit verwalteten Rechten an.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecb9a-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ecb9a-127">Header files</span></span>

<span data-ttu-id="ecb9a-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ecb9a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecb9a-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ecb9a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecb9a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecb9a-130">See also</span></span>



[<span data-ttu-id="ecb9a-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecb9a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecb9a-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecb9a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecb9a-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ecb9a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecb9a-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ecb9a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


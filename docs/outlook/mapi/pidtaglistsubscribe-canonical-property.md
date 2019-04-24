---
title: Kanonische Pidtaglistsubscribe (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279657"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="cd98f-103">Kanonische Pidtaglistsubscribe (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd98f-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="cd98f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd98f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd98f-105">Enthält den Wert des Listen-subscribe-Kopf Felds für MIME-Nachrichten (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="cd98f-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd98f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cd98f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd98f-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="cd98f-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="cd98f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cd98f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd98f-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="cd98f-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="cd98f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cd98f-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd98f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cd98f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cd98f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cd98f-112">Area:</span></span>  <br/> |<span data-ttu-id="cd98f-113">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="cd98f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd98f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd98f-114">Remarks</span></span>

<span data-ttu-id="cd98f-115">Um ein Listen-subscribe-Kopfzeilenfeld zu generieren, müssen Clients den Wert dieser Eigenschaften auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="cd98f-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="cd98f-116">MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld Listen-subscribe kopieren.</span><span class="sxs-lookup"><span data-stu-id="cd98f-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="cd98f-117">Um den Wert solcher serverbezogenen Eigenschaften festzulegen, müssen die in der folgenden Tabelle angegebenen Kopfzeilenfelder von MIME-Clients geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cd98f-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="cd98f-118">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="cd98f-118">**Property**</span></span>|<span data-ttu-id="cd98f-119">**Bevorzugter Kopfzeilen Feldname**</span><span class="sxs-lookup"><span data-stu-id="cd98f-119">**Preferred header field name**</span></span>|<span data-ttu-id="cd98f-120">**Name des alternativen Kopfzeilenfelds**</span><span class="sxs-lookup"><span data-stu-id="cd98f-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd98f-121">**Pidtaglistsubscribe (**</span><span class="sxs-lookup"><span data-stu-id="cd98f-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="cd98f-122">Liste abonnieren</span><span class="sxs-lookup"><span data-stu-id="cd98f-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="cd98f-123">X-list-subscribe</span><span class="sxs-lookup"><span data-stu-id="cd98f-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cd98f-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd98f-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd98f-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cd98f-125">Protocol specifications</span></span>

<span data-ttu-id="cd98f-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd98f-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd98f-127">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cd98f-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd98f-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd98f-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd98f-129">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="cd98f-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd98f-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="cd98f-130">Header files</span></span>

<span data-ttu-id="cd98f-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cd98f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd98f-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="cd98f-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd98f-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="cd98f-133">Mapitags.h</span></span>
  
> <span data-ttu-id="cd98f-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cd98f-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd98f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd98f-135">See also</span></span>



[<span data-ttu-id="cd98f-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd98f-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd98f-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd98f-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd98f-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cd98f-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd98f-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cd98f-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


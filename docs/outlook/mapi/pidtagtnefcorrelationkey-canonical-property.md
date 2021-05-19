---
title: PidTagTnefCorrelationKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341951"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="032a7-103">PidTagTnefCorrelationKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="032a7-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="032a7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="032a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="032a7-105">Enthält einen Wert, der eine Transport Neutral Encapsulation Format (TNEF)-Anlage mit einer Nachricht korreliert.</span><span class="sxs-lookup"><span data-stu-id="032a7-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="032a7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="032a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="032a7-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="032a7-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="032a7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="032a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="032a7-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="032a7-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="032a7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="032a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="032a7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="032a7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="032a7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="032a7-112">Area:</span></span>  <br/> |<span data-ttu-id="032a7-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="032a7-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="032a7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="032a7-114">Remarks</span></span>

<span data-ttu-id="032a7-115">Es wird empfohlen, dass TNEF-Anlagenunterobjekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="032a7-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="032a7-116">Diese Eigenschaft bestimmt, ob eine eingehende TNEF-Datei zu der Nachricht gehört, an die sie angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="032a7-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="032a7-117">Es wird hauptsächlich von Transportanbietern und Gateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="032a7-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="032a7-118">In einer ausgehenden Nachricht sollte der Transportanbieter einen binären Wert berechnen, der für diese Nachricht eindeutig ist, oder einen vorhandenen Wert verwenden, der die Eindeutigkeitsanforderung erfüllt, z. B. eine Nachrichten-ID.</span><span class="sxs-lookup"><span data-stu-id="032a7-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="032a7-119">Der Transportanbieter sollte diesen Wert in dieser Eigenschaft speichern und dann die [ITnef::AddProps-Methode](itnef-addprops.md) aufrufen, um ihn zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="032a7-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="032a7-120">Der gleiche Wert sollte auch im Transportumschlag an einem vom Anbieter definierten Ort gespeichert werden, z. B. im Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="032a7-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="032a7-121">Bei einer eingehenden Nachricht sollte der Transportanbieter die [ITnef::ExtractProps-Methode](itnef-extractprops.md) aufrufen, um die TNEF-Anlage zu entkapseln und diese Eigenschaft dann mit dem wert zu vergleichen, der im Transportumschlag gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="032a7-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="032a7-122">Wenn die Werte übereinstimmen, sollte TNEF normal verarbeitet werden, d. h. alle aus der TNEF-Anlage extrahierten Eigenschaften sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="032a7-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="032a7-123">Wenn die Werte nicht übereinstimmen, sollten alle Eigenschaften aus der TNEF-Anlage ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="032a7-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="032a7-124">Wenn diese Eigenschaft nicht festgelegt ist, sollte die TNEF-Datei als Teil dieser Nachricht betrachtet werden, und die anderen aus ihr extrahierten Eigenschaften sollten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="032a7-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="032a7-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="032a7-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="032a7-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="032a7-126">Protocol specifications</span></span>

<span data-ttu-id="032a7-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="032a7-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="032a7-128">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="032a7-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="032a7-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="032a7-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="032a7-130">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="032a7-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="032a7-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="032a7-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="032a7-132">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="032a7-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="032a7-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="032a7-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="032a7-134">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="032a7-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="032a7-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="032a7-135">Header files</span></span>

<span data-ttu-id="032a7-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="032a7-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="032a7-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="032a7-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="032a7-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="032a7-138">Mapitags.h</span></span>
  
> <span data-ttu-id="032a7-139">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="032a7-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="032a7-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="032a7-140">See also</span></span>



[<span data-ttu-id="032a7-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="032a7-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="032a7-142">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="032a7-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="032a7-143">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="032a7-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="032a7-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="032a7-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


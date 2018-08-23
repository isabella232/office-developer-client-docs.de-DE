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
ms.openlocfilehash: 760196668ffb3c486803f27b50ff809177e8e6f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588615"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="0717d-103">PidTagTnefCorrelationKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0717d-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="0717d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0717d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0717d-105">Enthält einen Wert, der eine Anlage Transport Neutral Encapsulation Format (TNEF) mit einer Nachricht verknüpft.</span><span class="sxs-lookup"><span data-stu-id="0717d-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0717d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0717d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0717d-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="0717d-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="0717d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0717d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0717d-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="0717d-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="0717d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0717d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0717d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0717d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0717d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0717d-112">Area:</span></span>  <br/> |<span data-ttu-id="0717d-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="0717d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0717d-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0717d-114">Remarks</span></span>

<span data-ttu-id="0717d-115">Es wird empfohlen, dass TNEF-Anlage Unterobjekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="0717d-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="0717d-116">Diese Eigenschaft bestimmt, ob eine eingehende TNEF-Datei an die Nachricht gehört, für die Sie verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0717d-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="0717d-117">Es wird hauptsächlich von Transportanbieter und Gateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="0717d-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="0717d-118">Für eine ausgehende Nachricht sollte der Adressbuchhierarchie einen Binärwert für diese Nachricht eindeutig zu berechnen, oder verwenden einen vorhandenen Wert, der die Anforderung an die Eindeutigkeit, wie eine Nachricht-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="0717d-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="0717d-119">Der Transportdienst sollte diesen Wert in dieser Eigenschaft speichern und rufen Sie dann die [ITnef::AddProps](itnef-addprops.md) -Methode, um es kapseln.</span><span class="sxs-lookup"><span data-stu-id="0717d-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="0717d-120">Der gleiche Wert sollten auch im Umschlag Transport in einer vom Anbieter, wie der Nachrichtenkopf definierten Stelle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0717d-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="0717d-121">Auf eine eingehende Nachricht sollte der Adressbuchhierarchie rufen Sie die [ITnef::ExtractProps](itnef-extractprops.md) -Methode, die die TNEF-Anlage entkapseln und vergleichen Sie diese Eigenschaft mit dem Wert in der Transport Umschlag gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0717d-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="0717d-122">Wenn die Werte übereinstimmen, TNEF normalerweise verarbeitet werden soll, d. h., alle Eigenschaften aus der TNEF-Anlage extrahiert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0717d-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="0717d-123">Wenn die Werte nicht übereinstimmen, sollte alle Eigenschaften aus der TNEF-Anlage ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="0717d-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="0717d-124">Wenn diese Eigenschaft nicht festgelegt ist, sollte die TNEF-Datei zu dieser Nachricht gehören berücksichtigt werden, und die anderen Eigenschaften daraus extrahiert sollte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0717d-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0717d-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0717d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0717d-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0717d-126">Protocol specifications</span></span>

<span data-ttu-id="0717d-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0717d-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0717d-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0717d-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0717d-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0717d-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0717d-130">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="0717d-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0717d-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0717d-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0717d-132">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0717d-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0717d-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0717d-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0717d-134">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="0717d-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0717d-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0717d-135">Header files</span></span>

<span data-ttu-id="0717d-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0717d-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="0717d-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0717d-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="0717d-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0717d-138">Mapitags.h</span></span>
  
> <span data-ttu-id="0717d-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0717d-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0717d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0717d-140">See also</span></span>



[<span data-ttu-id="0717d-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0717d-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0717d-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0717d-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0717d-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0717d-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0717d-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0717d-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


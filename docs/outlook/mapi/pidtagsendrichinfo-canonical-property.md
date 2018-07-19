---
title: PidTagSendRichInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a85851663c22b33ea94099ac0ab14f81c424259b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795134"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="69027-103">PidTagSendRichInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="69027-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="69027-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69027-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69027-105">Enthält TRUE, wenn der Empfänger alle Nachrichteninhalt, einschließlich Rich Text Format (RTF) und Objekten Object Linking and Embedding (OLE) empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="69027-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69027-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="69027-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69027-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="69027-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="69027-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="69027-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69027-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="69027-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="69027-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="69027-110">Data type:</span></span>  <br/> |<span data-ttu-id="69027-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="69027-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="69027-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="69027-112">Area:</span></span>  <br/> |<span data-ttu-id="69027-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="69027-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69027-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69027-114">Remarks</span></span>

<span data-ttu-id="69027-115">Es wird empfohlen, dass diese Eigenschaft Verteilerliste und messaging User-Objekte verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="69027-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="69027-116">Diese Eigenschaft gibt an, ob der Absender den Empfänger zu MAPI-fähigen betrachtet.</span><span class="sxs-lookup"><span data-stu-id="69027-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="69027-117">Wenn diese Eigenschaft auf TRUE festgelegt ist, können die Transport- und Gateway des gesamten Inhalts der Nachricht, einschließlich RTF und OLE-Objekte übertragen.</span><span class="sxs-lookup"><span data-stu-id="69027-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="69027-118">Der Adressbuchhierarchie und Gateway sollte Transport Neutral Encapsulation Format (TNEF) verwenden, um alle Eigenschaften kapseln, die nicht für alle der Messagingsysteme beteiligten systemeigene sind.</span><span class="sxs-lookup"><span data-stu-id="69027-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="69027-119">Wenn diese Eigenschaft auf FALSE festgelegt ist, können der Adressbuchhierarchie und Gateway Nachrichteninhalt verwerfen, die systemeigene-Clients verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="69027-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="69027-120">Beispielsweise kann die Clients RTF nicht unterstützen, der Adressbuchhierarchie nur-Text senden.</span><span class="sxs-lookup"><span data-stu-id="69027-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="69027-121">Wenn diese Eigenschaft nicht festgelegt ist, wird durch die Implementierung der Adressbuchhierarchie, Message Transfer Agent (MTA) oder Gateway Standardverhalten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="69027-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="69027-122">Von adressbuchanbietern implementierte sind zur Unterstützung von dieser Eigenschaft nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69027-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="69027-123">Beispielsweise können ein eng gekoppelten Adresse Adressbuch und Transport Anbieter senden TNEF jedoch nie RTF-Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="69027-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="69027-124">Der Client sollte nicht der Adressbuchhierarchie voraussetzen und Gateway TNEF auf eigene Initiative verwenden.</span><span class="sxs-lookup"><span data-stu-id="69027-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="69027-125">Einige Transportanbieter und Gateways, die Unterstützung von TNEF ohne Berücksichtigung des Werts dieser Eigenschaft übertragen, aber andere ablehnen, zu erstellen oder TNEF senden, wenn sie nicht auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="69027-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="69027-126">Die Einstellung dieser Eigenschaft und die Entscheidungen basierend auf seinen Wert sind für einzelne pro Empfänger.</span><span class="sxs-lookup"><span data-stu-id="69027-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="69027-127">Der Wert von MAPI wird standardmäßig auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69027-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="69027-128">Ein Aufruf von [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) oder einen Anbieter Aufrufen [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) Client kann das **MAPI_SEND_NO_RICH_INFO** Bit im Parameter _UlFlags_ festgelegt, MAPI, um diese Eigenschaft auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69027-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="69027-129">Von der Benutzeroberfläche erstellt Fly verwenden Sie den Wert durch die Vorlage erstellen angegeben.</span><span class="sxs-lookup"><span data-stu-id="69027-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="69027-130">Wenn der Name kann nicht aufgelöst werden, aber als eine IP-Adresse (SMTP) interpretiert werden kann, ist diese Eigenschaft auf Aufrufe der [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="69027-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="69027-131">Um als eine IP-Adresse zu verstehen, muss der Anzeigename des nicht aufgelösten Eintrags im Format X@Y. Z, beispielsweise "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="69027-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69027-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="69027-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69027-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="69027-133">Protocol specifications</span></span>

<span data-ttu-id="69027-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69027-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69027-135">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="69027-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69027-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69027-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69027-137">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="69027-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="69027-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69027-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69027-139">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="69027-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="69027-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69027-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69027-141">aus dem Internet standard-e-Mail-Konventionen für die Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="69027-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69027-142">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="69027-142">Header files</span></span>

<span data-ttu-id="69027-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69027-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="69027-144">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="69027-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="69027-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69027-145">Mapitags.h</span></span>
  
> <span data-ttu-id="69027-146">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="69027-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69027-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69027-147">See also</span></span>



[<span data-ttu-id="69027-148">PidTagAttachDataObject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="69027-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="69027-149">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69027-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69027-150">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69027-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69027-151">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="69027-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69027-152">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="69027-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


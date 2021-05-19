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
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342518"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="f4ab6-103">PidTagSendRichInfo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4ab6-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="f4ab6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4ab6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4ab6-105">Enthält TRUE, wenn der Empfänger alle Nachrichteninhalte empfangen kann, einschließlich Rich Text Format (RTF) und Object Linking and Embedding (OLE)-Objekte.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4ab6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f4ab6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4ab6-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="f4ab6-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="f4ab6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f4ab6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4ab6-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="f4ab6-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="f4ab6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f4ab6-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4ab6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f4ab6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f4ab6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f4ab6-112">Area:</span></span>  <br/> |<span data-ttu-id="f4ab6-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="f4ab6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4ab6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4ab6-114">Remarks</span></span>

<span data-ttu-id="f4ab6-115">Es wird empfohlen, dass Verteilerlisten- und Messagingbenutzerobjekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="f4ab6-116">Diese Eigenschaft gibt an, ob der Absender den Empfänger als MAPI-aktiviert betrachtet.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="f4ab6-117">Wenn diese Eigenschaft auf TRUE festgelegt ist, können der Transport und das Gateway den vollständigen Inhalt der Nachricht übertragen, einschließlich RTF- und OLE-Objekten.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="f4ab6-118">Der Transportanbieter und das Gateway sollten das TNEF (Transport Neutral Encapsulation Format) verwenden, um alle Eigenschaften zu kapseln, die nicht für alle beteiligten Messagingsysteme systemeigene Sind.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="f4ab6-119">Wenn diese Eigenschaft auf FALSE festgelegt ist, können der Transportanbieter und das Gateway Nachrichteninhalte verwerfen, die von ihren systemeigenen Clients nicht verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="f4ab6-120">Wenn die Clients z. B. RTF nicht unterstützen, kann der Transportanbieter nur Nur-Text senden.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="f4ab6-121">Wenn diese Eigenschaft nicht festgelegt ist, wird das Standardverhalten durch die Implementierung des Transportanbieters, des Nachrichtenübertragungs-Agents (Message Transfer Agent, MTA) oder des Gateways bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="f4ab6-122">Adressbuchanbieter müssen diese Eigenschaft nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="f4ab6-123">Beispielsweise können ein eng gekoppelte Adressbuch- und Transportanbieter TNEF senden, aber rtF nie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="f4ab6-124">Der Client sollte nicht davon ausgehen, dass der Transportanbieter und das Gateway TNEF von sich aus verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="f4ab6-125">Einige Transportanbieter und Gateways, die TNEF unterstützen, übertragen sie ohne Rücksicht auf den Wert dieser Eigenschaft, andere ablehnen jedoch, TNEF zu erstellen oder zu senden, wenn sie nicht auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f4ab6-126">Die Einstellung dieser Eigenschaft und die Entscheidungen basierend auf ihrem Wert erfolgen pro Empfänger.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="f4ab6-127">Standardmäßig legt MAPI den Wert auf TRUE fest.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="f4ab6-128">Ein Client, der [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) aufruft, oder ein Anbieter, der [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) aufruft, kann das **MAPI_SEND_NO_RICH_INFO-Bit** im  _ulFlags-Parameter_ festlegen, wodurch MAPI diese Eigenschaft auf FALSE festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="f4ab6-129">Von der Benutzeroberfläche erstellte Einmalvorlagen verwenden den in der Erstellungsvorlage angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="f4ab6-130">Bei Aufrufen der [IAddrBook::ResolveName-Methode,](iaddrbook-resolvename.md) wenn der Name nicht aufgelöst werden kann, aber als Internetadresse (SMTP) interpretiert werden kann, wird diese Eigenschaft auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="f4ab6-131">Um als Internetadresse ausgelegt zu werden, muss der Anzeigename des nicht aufgelösten Eintrags im Format X@Y. Z, z. B. "pete@pinecone.com".</span><span class="sxs-lookup"><span data-stu-id="f4ab6-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4ab6-132">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4ab6-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4ab6-133">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f4ab6-133">Protocol specifications</span></span>

<span data-ttu-id="f4ab6-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4ab6-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4ab6-135">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4ab6-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4ab6-136">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4ab6-137">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="f4ab6-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4ab6-138">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4ab6-139">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f4ab6-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4ab6-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4ab6-141">von Internetstandard-E-Mail-Konventionen zu Nachrichtenobjekten.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4ab6-142">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f4ab6-142">Header files</span></span>

<span data-ttu-id="f4ab6-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4ab6-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4ab6-144">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4ab6-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4ab6-145">Mapitags.h</span></span>
  
> <span data-ttu-id="f4ab6-146">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f4ab6-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4ab6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4ab6-147">See also</span></span>



[<span data-ttu-id="f4ab6-148">PidTagAttachDataObject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4ab6-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="f4ab6-149">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4ab6-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4ab6-150">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f4ab6-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4ab6-151">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f4ab6-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4ab6-152">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f4ab6-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


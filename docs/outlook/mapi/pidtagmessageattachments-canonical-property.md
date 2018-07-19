---
title: PidTagMessageAttachments (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b76a73a0fde8f4531b99a58646b927724162e81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794582"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="834cc-103">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="834cc-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="834cc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="834cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="834cc-105">Enthält eine Tabelle mit Einschränkungen, die auf einer Inhaltstabelle, erhalten alle Nachrichten, die Anlage Unterobjekte enthalten, die die Suchkriterien erfüllen angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="834cc-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain attachment subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="834cc-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="834cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="834cc-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="834cc-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="834cc-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="834cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="834cc-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="834cc-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="834cc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="834cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="834cc-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="834cc-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="834cc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="834cc-112">Area:</span></span>  <br/> |<span data-ttu-id="834cc-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="834cc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="834cc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="834cc-114">Remarks</span></span>

<span data-ttu-id="834cc-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="834cc-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="834cc-116">Als Eigenschaft vom Typ PT_OBJECT kann es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="834cc-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="834cc-117">Von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der **IID_IMAPITable** Identifier anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="834cc-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="834cc-118">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, aber optional meldet oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="834cc-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="834cc-119">Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="834cc-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="834cc-120">For more information, see [Anlagentabellen](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="834cc-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="834cc-121">Diese Eigenschaft kann durch Festlegen in der Struktur [SSubRestriction](ssubrestriction.md) für Unterobjekts Einschränkung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="834cc-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="834cc-122">Dadurch wird den Client zur Begrenzung der Ansicht eines Containers auf Nachrichten mit Anlagen, die Besprechung, die bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="834cc-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="834cc-123">Eine Nachricht qualifiziert für anzeigen, wenn mindestens eine Zeile in der Tabelle Anlagen, d. h., eine Anlage, die Einschränkung Unterobjekts erfüllt.</span><span class="sxs-lookup"><span data-stu-id="834cc-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="834cc-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="834cc-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="834cc-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="834cc-125">Protocol specifications</span></span>

<span data-ttu-id="834cc-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="834cc-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="834cc-127">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="834cc-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="834cc-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="834cc-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="834cc-129">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="834cc-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="834cc-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="834cc-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="834cc-131">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="834cc-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="834cc-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="834cc-132">Header files</span></span>

<span data-ttu-id="834cc-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="834cc-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="834cc-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="834cc-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="834cc-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="834cc-135">Mapitags.h</span></span>
  
> <span data-ttu-id="834cc-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="834cc-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="834cc-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="834cc-137">See also</span></span>



[<span data-ttu-id="834cc-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="834cc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="834cc-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="834cc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="834cc-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="834cc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="834cc-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="834cc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


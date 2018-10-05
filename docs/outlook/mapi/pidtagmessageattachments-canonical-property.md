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
ms.openlocfilehash: 5f13c2825fc0127b95fbf5bc0b41d68c64556864
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384087"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="58c92-103">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="58c92-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="58c92-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58c92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58c92-105">Enthält eine Tabelle mit Einschränkungen, die auf einer Inhaltstabelle, erhalten alle Nachrichten, die Anlage Unterobjekte enthalten, die die Suchkriterien erfüllen angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="58c92-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain attachment subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58c92-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="58c92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58c92-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="58c92-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="58c92-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="58c92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58c92-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="58c92-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="58c92-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="58c92-110">Data type:</span></span>  <br/> |<span data-ttu-id="58c92-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="58c92-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="58c92-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="58c92-112">Area:</span></span>  <br/> |<span data-ttu-id="58c92-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="58c92-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58c92-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58c92-114">Remarks</span></span>

<span data-ttu-id="58c92-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="58c92-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="58c92-116">Als Eigenschaft vom Typ PT_OBJECT kann es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="58c92-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="58c92-117">Von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der **IID_IMAPITable** Identifier anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="58c92-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="58c92-118">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, aber optional meldet oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="58c92-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="58c92-119">Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="58c92-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="58c92-120">For more information, see [Anlagentabellen](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="58c92-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="58c92-121">Diese Eigenschaft kann durch Festlegen in der Struktur [SSubRestriction](ssubrestriction.md) für Unterobjekts Einschränkung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58c92-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="58c92-122">Dadurch wird den Client zur Begrenzung der Ansicht eines Containers auf Nachrichten mit Anlagen, die Besprechung, die bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="58c92-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="58c92-123">Eine Nachricht qualifiziert für anzeigen, wenn mindestens eine Zeile in der Tabelle Anlagen, d. h., eine Anlage, die Einschränkung Unterobjekts erfüllt.</span><span class="sxs-lookup"><span data-stu-id="58c92-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="58c92-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="58c92-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58c92-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="58c92-125">Protocol specifications</span></span>

<span data-ttu-id="58c92-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58c92-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58c92-127">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="58c92-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="58c92-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58c92-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58c92-129">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="58c92-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="58c92-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58c92-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58c92-131">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="58c92-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58c92-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="58c92-132">Header files</span></span>

<span data-ttu-id="58c92-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58c92-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="58c92-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="58c92-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="58c92-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58c92-135">Mapitags.h</span></span>
  
> <span data-ttu-id="58c92-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="58c92-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58c92-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58c92-137">See also</span></span>



[<span data-ttu-id="58c92-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58c92-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58c92-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58c92-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58c92-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="58c92-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58c92-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="58c92-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


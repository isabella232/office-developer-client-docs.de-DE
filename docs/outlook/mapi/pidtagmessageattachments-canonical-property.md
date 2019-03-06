---
title: Kanonische Pidtagmessageattachments (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413973"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="4da71-103">Kanonische Pidtagmessageattachments (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4da71-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="4da71-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4da71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4da71-105">Enthält eine Tabelle mit Anlagen für eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4da71-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4da71-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4da71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4da71-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="4da71-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="4da71-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4da71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4da71-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="4da71-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="4da71-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4da71-110">Data type:</span></span>  <br/> |<span data-ttu-id="4da71-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="4da71-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="4da71-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4da71-112">Area:</span></span>  <br/> |<span data-ttu-id="4da71-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="4da71-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4da71-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4da71-114">Remarks</span></span>

<span data-ttu-id="4da71-115">Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4da71-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="4da71-116">Als Eigenschaft vom Typ PT_OBJECT kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4da71-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="4da71-117">Auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den **IID_IMAPITable** -Schnittstellenbezeichner anzufordern.</span><span class="sxs-lookup"><span data-stu-id="4da71-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="4da71-118">Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber Sie kann Sie optional melden oder nicht, wenn Sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4da71-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="4da71-119">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMessage::](imessage-getattachmenttable.md) getattachmentable-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4da71-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="4da71-120">For more information, see [Anlagentabellen](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4da71-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="4da71-121">Diese Eigenschaft kann für SubObject-Einschränkungen verwendet werden, indem Sie Sie in der [SSubRestriction](ssubrestriction.md) -Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="4da71-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="4da71-122">Dadurch kann der Client die Ansicht eines Containers auf Nachrichten mit Anlagen begrenzen, die bestimmte Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4da71-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="4da71-123">Eine Nachricht kann angezeigt werden, wenn mindestens eine Zeile in der Attachments-Tabelle, also eine Anlage, der SubObject-Einschränkung entspricht.</span><span class="sxs-lookup"><span data-stu-id="4da71-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4da71-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4da71-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4da71-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4da71-125">Protocol specifications</span></span>

<span data-ttu-id="4da71-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4da71-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4da71-127">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4da71-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="4da71-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4da71-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4da71-129">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4da71-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="4da71-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4da71-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4da71-131">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="4da71-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4da71-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4da71-132">Header files</span></span>

<span data-ttu-id="4da71-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4da71-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="4da71-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4da71-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="4da71-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4da71-135">Mapitags.h</span></span>
  
> <span data-ttu-id="4da71-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4da71-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4da71-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4da71-137">See also</span></span>



[<span data-ttu-id="4da71-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4da71-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4da71-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4da71-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4da71-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4da71-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4da71-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4da71-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


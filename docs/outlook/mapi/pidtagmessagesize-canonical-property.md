---
title: Kanonische Pidtagmessagesize (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355650"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="e766a-103">Kanonische Pidtagmessagesize (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e766a-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="e766a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e766a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e766a-105">Enthält die Summe der Größen aller Eigenschaften eines Nachrichtenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e766a-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e766a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e766a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e766a-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="e766a-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="e766a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e766a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e766a-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="e766a-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="e766a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e766a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e766a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e766a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e766a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e766a-112">Area:</span></span>  <br/> |<span data-ttu-id="e766a-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="e766a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e766a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e766a-114">Remarks</span></span>

<span data-ttu-id="e766a-115">Es wird empfohlen, dass Nachrichtenobjekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="e766a-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="e766a-116">Die Größe der Nachricht gibt die ungefähre Anzahl von Bytes an, die beim Verschieben der Nachricht von einem Nachrichtenspeicher zu einem anderen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="e766a-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="e766a-117">Als Summe der Größen aller Eigenschaften des Message-Objekts ist es in der Regel erheblich größer als der Nachrichtentext allein.</span><span class="sxs-lookup"><span data-stu-id="e766a-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="e766a-118">Die meisten Nachrichtenspeicher Anbieter berechnen diese Eigenschaft für Nachrichten, die Sie verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e766a-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="e766a-119">Einige Nachrichtenspeicher Anbieter unterstützen diese Eigenschaft jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="e766a-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="e766a-120">Diese Eigenschaft ist in jedem Fall erst verfügbar, wenn die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -oder [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e766a-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e766a-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e766a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e766a-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e766a-122">Protocol specifications</span></span>

<span data-ttu-id="e766a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e766a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e766a-124">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e766a-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e766a-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e766a-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e766a-126">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="e766a-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e766a-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e766a-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e766a-128">Behandelt Ordner Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e766a-128">Handles folder operations.</span></span>
    
<span data-ttu-id="e766a-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e766a-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e766a-130">Gibt zulässige Vorgänge für die wichtigsten Nachrichtenspeicher Objekte an.</span><span class="sxs-lookup"><span data-stu-id="e766a-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e766a-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e766a-131">Header files</span></span>

<span data-ttu-id="e766a-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e766a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="e766a-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e766a-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="e766a-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e766a-134">Mapitags.h</span></span>
  
> <span data-ttu-id="e766a-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e766a-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e766a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e766a-136">See also</span></span>



[<span data-ttu-id="e766a-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e766a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e766a-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e766a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e766a-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e766a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e766a-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e766a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


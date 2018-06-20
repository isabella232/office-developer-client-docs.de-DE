---
title: Kanonische PidTagMessageSize-Eigenschaft
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
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794619"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="d2e51-103">Kanonische PidTagMessageSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2e51-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="d2e51-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2e51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2e51-105">Enthält die Summe der Größen aller Eigenschaften auf ein Meldungsobjekt in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d2e51-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2e51-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d2e51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2e51-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="d2e51-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="d2e51-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="d2e51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2e51-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="d2e51-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="d2e51-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d2e51-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2e51-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d2e51-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d2e51-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d2e51-112">Area:</span></span>  <br/> |<span data-ttu-id="d2e51-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="d2e51-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2e51-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2e51-114">Remarks</span></span>

<span data-ttu-id="d2e51-115">Es wird empfohlen, dass Message Objekte diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="d2e51-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="d2e51-116">Die Nachrichtengröße gibt die ungefähre Anzahl von Bytes, die übertragen werden, wenn die Nachricht von einem Informationsspeicher an eine andere verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d2e51-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="d2e51-117">Wird die Summe der Größen aller Eigenschaften im Message-Objekt, ist es in der Regel deutlich größer als den Nachrichtentext allein.</span><span class="sxs-lookup"><span data-stu-id="d2e51-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="d2e51-118">Die meisten Nachricht speichern Anbieter Compute diese Eigenschaft für Nachrichten, die sie behandeln.</span><span class="sxs-lookup"><span data-stu-id="d2e51-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="d2e51-119">Einige Nachricht Anbieter unterstützt diese Eigenschaft jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="d2e51-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="d2e51-120">Diese Eigenschaft ist in jedem Fall nicht verfügbar, bis die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d2e51-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d2e51-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d2e51-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2e51-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d2e51-122">Protocol specifications</span></span>

<span data-ttu-id="d2e51-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e51-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e51-124">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d2e51-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2e51-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e51-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e51-126">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="d2e51-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d2e51-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e51-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e51-128">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="d2e51-128">Handles folder operations.</span></span>
    
<span data-ttu-id="d2e51-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2e51-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2e51-130">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="d2e51-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2e51-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d2e51-131">Header files</span></span>

<span data-ttu-id="d2e51-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2e51-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2e51-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d2e51-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2e51-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2e51-134">Mapitags.h</span></span>
  
> <span data-ttu-id="d2e51-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d2e51-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2e51-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2e51-136">See also</span></span>



[<span data-ttu-id="d2e51-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2e51-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2e51-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2e51-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2e51-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d2e51-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2e51-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d2e51-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


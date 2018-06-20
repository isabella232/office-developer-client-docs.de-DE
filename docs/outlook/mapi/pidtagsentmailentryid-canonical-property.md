---
title: Kanonische PidTagSentMailEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 869f7f0bb4ea5e7222201083cb6d41754d241396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795143"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="7c89a-103">Kanonische PidTagSentMailEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c89a-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7c89a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c89a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c89a-105">Enthält die Eintrags-ID des Ordners, in dem die Nachricht nach dem Absenden verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c89a-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c89a-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7c89a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c89a-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7c89a-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7c89a-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="7c89a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c89a-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="7c89a-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="7c89a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7c89a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c89a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7c89a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7c89a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7c89a-112">Area:</span></span>  <br/> |<span data-ttu-id="7c89a-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="7c89a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c89a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c89a-114">Remarks</span></span>

<span data-ttu-id="7c89a-115">Diese Eigenschaft wird häufig von der **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))-Eigenschaft, die Clientanwendung Standardordner gesendete Elemente kopiert.</span><span class="sxs-lookup"><span data-stu-id="7c89a-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="7c89a-116">Die Clientanwendung verwendet diese Eigenschaft mit der **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft steuern, was geschieht mit einer Meldung, nachdem es gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c89a-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="7c89a-117">Eine oder die andere sollte Set, jedoch nicht beide.</span><span class="sxs-lookup"><span data-stu-id="7c89a-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c89a-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7c89a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c89a-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7c89a-119">Protocol specifications</span></span>

<span data-ttu-id="7c89a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c89a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c89a-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7c89a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c89a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c89a-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c89a-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7c89a-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7c89a-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c89a-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c89a-125">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7c89a-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c89a-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7c89a-126">Header files</span></span>

<span data-ttu-id="7c89a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c89a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c89a-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7c89a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c89a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c89a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="7c89a-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7c89a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c89a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c89a-131">See also</span></span>



[<span data-ttu-id="7c89a-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c89a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c89a-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c89a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c89a-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7c89a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c89a-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7c89a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidTagReplyRecipientEntries (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1ab8828dd2fc28a2fba1620fc251ba0a87c3e2bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794953"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="4c283-103">PidTagReplyRecipientEntries (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c283-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="4c283-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c283-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c283-105">Enthält eine Größe Array von Eintragsbezeichner für Empfänger, die eine Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c283-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c283-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4c283-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c283-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="4c283-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="4c283-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4c283-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c283-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="4c283-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="4c283-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4c283-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c283-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c283-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c283-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4c283-112">Area:</span></span>  <br/> |<span data-ttu-id="4c283-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="4c283-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c283-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c283-114">Remarks</span></span>

<span data-ttu-id="4c283-115">Diese Eigenschaft enthält eine [FLATENTRYLIST](flatentrylist.md) -Struktur und ist keine mehrwertige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c283-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="4c283-116">Wenn diese Eigenschaft nicht vorhanden ist, wird nur für den Benutzer durch die **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))-Eigenschaft identifiziert eine Antwort gesendet.</span><span class="sxs-lookup"><span data-stu-id="4c283-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="4c283-117">Wenn dies und **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))-Eigenschaften definiert sind, wird die Antwort an alle diese beiden Eigenschaften identifizierten Empfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="4c283-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="4c283-118">Ein Transportdienstes verwendet diese Eigenschaften die Logik üblichen Antworten außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="4c283-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="4c283-119">Wenn diese Eigenschaft oder die **PR_REPLY_RECIPIENT_NAMES** -Eigenschaft festgelegt ist, muss auch die anderen-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4c283-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="4c283-120">Diese Eigenschaften müssen die gleiche Anzahl von Empfängern enthalten, und sie müssen in der gleichen Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="4c283-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="4c283-121">Installationsfehler, diese Anforderungen zu beobachten kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="4c283-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c283-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4c283-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c283-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4c283-123">Protocol specifications</span></span>

<span data-ttu-id="4c283-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c283-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c283-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4c283-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c283-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c283-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c283-127">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4c283-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="4c283-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c283-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c283-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="4c283-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c283-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4c283-130">Header files</span></span>

<span data-ttu-id="4c283-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c283-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c283-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4c283-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c283-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c283-133">Mapitags.h</span></span>
  
> <span data-ttu-id="4c283-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4c283-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c283-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c283-135">See also</span></span>



[<span data-ttu-id="4c283-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c283-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c283-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c283-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c283-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4c283-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c283-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4c283-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


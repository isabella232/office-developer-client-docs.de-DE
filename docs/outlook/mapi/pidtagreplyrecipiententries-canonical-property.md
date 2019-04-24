---
title: Kanonische Pidtagreplyrecipiententries (-Eigenschaft
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
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355055"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="6e064-103">Kanonische Pidtagreplyrecipiententries (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6e064-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="6e064-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e064-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e064-105">Enthält ein großes Array von Eintrags Bezeichnern für Empfänger, die eine Antwort erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="6e064-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e064-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e064-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e064-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="6e064-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="6e064-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6e064-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e064-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="6e064-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="6e064-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e064-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e064-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e064-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e064-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e064-112">Area:</span></span>  <br/> |<span data-ttu-id="6e064-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="6e064-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e064-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e064-114">Remarks</span></span>

<span data-ttu-id="6e064-115">Diese Eigenschaft enthält eine [FLATENTRYLIST](flatentrylist.md) -Struktur und ist keine mehrwertige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e064-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="6e064-116">Wenn diese Eigenschaft nicht vorhanden ist, wird eine Antwort nur an den Benutzer gesendet, der von der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))-Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6e064-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="6e064-117">Wenn diese und die **PR_REPLY_RECIPIENT_NAMES** ([pidtagreplyrecipientnames (](pidtagreplyrecipientnames-canonical-property.md))-Eigenschaft definiert sind, wird die Antwort an alle Empfänger gesendet, die von diesen beiden Eigenschaften identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6e064-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="6e064-118">Ein Transportanbieter verwendet diese Eigenschaften, um die übliche Antwort Logik außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="6e064-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="6e064-119">Wenn diese Eigenschaft oder die **PR_REPLY_RECIPIENT_NAMES** -Eigenschaft festgelegt ist, muss auch die andere Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6e064-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="6e064-120">Diese Eigenschaften müssen dieselbe Anzahl von Empfängern enthalten, und Sie müssen diese in derselben Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e064-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="6e064-121">Die Nichteinhaltung dieser Anforderungen kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="6e064-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e064-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e064-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e064-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6e064-123">Protocol specifications</span></span>

<span data-ttu-id="6e064-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e064-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e064-125">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6e064-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e064-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e064-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e064-127">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6e064-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="6e064-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e064-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e064-129">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="6e064-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e064-130">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="6e064-130">Header files</span></span>

<span data-ttu-id="6e064-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6e064-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e064-132">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="6e064-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e064-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6e064-133">Mapitags.h</span></span>
  
> <span data-ttu-id="6e064-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6e064-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e064-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e064-135">See also</span></span>



[<span data-ttu-id="6e064-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e064-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e064-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e064-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e064-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6e064-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e064-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6e064-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


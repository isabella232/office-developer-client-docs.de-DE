---
title: PidTagReplyRecipientNames (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355174"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="461fd-103">PidTagReplyRecipientNames (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="461fd-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="461fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="461fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="461fd-105">Enthält eine Liste der Anzeigenamen für Empfänger, die eine Antwort erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="461fd-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="461fd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="461fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="461fd-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="461fd-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="461fd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="461fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="461fd-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="461fd-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="461fd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="461fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="461fd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="461fd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="461fd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="461fd-112">Area:</span></span>  <br/> |<span data-ttu-id="461fd-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="461fd-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="461fd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="461fd-114">Remarks</span></span>

<span data-ttu-id="461fd-115">Diese Eigenschaften enthalten die Durch Semikolons getrennten Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="461fd-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="461fd-116">Wenn diese Eigenschaft nicht vorhanden ist, wird eine Antwort nur an den Benutzer gesendet, der durch die **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) -Eigenschaft identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="461fd-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="461fd-117">Wenn **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und diese Eigenschaften definiert sind, wird die Antwort an alle Empfänger gesendet, die durch diese beiden Eigenschaften identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="461fd-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="461fd-118">Ein Transportanbieter verwendet diese Eigenschaften, um die übliche Antwortlogik außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="461fd-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="461fd-119">Wenn eine **PR_REPLY_RECIPIENT_ENTRIES** oder diese Eigenschaften festgelegt sind, muss auch die andere Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="461fd-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="461fd-120">Diese Eigenschaften müssen die gleiche Anzahl von Empfängern enthalten, und sie müssen sie in derselben Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="461fd-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="461fd-121">Wenn diese Anforderungen nicht erfüllt werden, kann dies zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="461fd-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="461fd-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="461fd-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="461fd-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="461fd-123">Protocol specifications</span></span>

<span data-ttu-id="461fd-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="461fd-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="461fd-125">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="461fd-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="461fd-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="461fd-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="461fd-127">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="461fd-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="461fd-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="461fd-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="461fd-129">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="461fd-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="461fd-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="461fd-130">Header files</span></span>

<span data-ttu-id="461fd-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="461fd-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="461fd-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="461fd-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="461fd-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="461fd-133">Mapitags.h</span></span>
  
> <span data-ttu-id="461fd-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="461fd-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="461fd-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="461fd-135">See also</span></span>



[<span data-ttu-id="461fd-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="461fd-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="461fd-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="461fd-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="461fd-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="461fd-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="461fd-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="461fd-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


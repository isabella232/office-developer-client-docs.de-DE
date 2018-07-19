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
ms.openlocfilehash: 5abbe14576bec9f03f0b1bf5578b68032f95f8a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794954"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="96573-103">PidTagReplyRecipientNames (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="96573-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="96573-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="96573-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="96573-105">Enthält eine Liste von Anzeigenamen für Empfänger, die eine Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="96573-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96573-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="96573-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96573-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="96573-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="96573-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="96573-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96573-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="96573-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="96573-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="96573-110">Data type:</span></span>  <br/> |<span data-ttu-id="96573-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="96573-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="96573-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="96573-112">Area:</span></span>  <br/> |<span data-ttu-id="96573-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="96573-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96573-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96573-114">Remarks</span></span>

<span data-ttu-id="96573-115">Diese Eigenschaften enthalten die angezeigten Namen durch Semikolons voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="96573-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="96573-116">Wenn diese Eigenschaft nicht vorhanden ist, wird nur für den Benutzer durch die Eigenschaft **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) identifizierten eine Antwort gesendet.</span><span class="sxs-lookup"><span data-stu-id="96573-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="96573-117">Wenn **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) und diese Eigenschaften definiert sind, wird die Antwort an alle diese beiden Eigenschaften identifizierten Empfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="96573-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="96573-118">Ein Transportdienstes verwendet diese Eigenschaften die Logik üblichen Antworten außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="96573-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="96573-119">Wenn **PR_REPLY_RECIPIENT_ENTRIES** oder diese Eigenschaften festgelegt sind, muss auch die anderen-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="96573-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="96573-120">Diese Eigenschaften müssen die gleiche Anzahl von Empfängern enthalten, und sie müssen in der gleichen Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="96573-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="96573-121">Installationsfehler, diese Anforderungen zu beobachten kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="96573-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="96573-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="96573-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96573-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="96573-123">Protocol specifications</span></span>

<span data-ttu-id="96573-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96573-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96573-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="96573-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96573-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96573-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96573-127">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="96573-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="96573-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96573-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96573-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="96573-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96573-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="96573-130">Header files</span></span>

<span data-ttu-id="96573-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96573-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="96573-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="96573-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="96573-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96573-133">Mapitags.h</span></span>
  
> <span data-ttu-id="96573-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="96573-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96573-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96573-135">See also</span></span>



[<span data-ttu-id="96573-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96573-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96573-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="96573-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96573-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="96573-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96573-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="96573-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


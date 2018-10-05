---
title: PidTagConversationTopic (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400390"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="152a7-103">PidTagConversationTopic (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="152a7-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="152a7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="152a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="152a7-105">Das Thema der ersten Nachricht in einer Unterhaltung Thread enthält.</span><span class="sxs-lookup"><span data-stu-id="152a7-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="152a7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="152a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="152a7-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="152a7-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="152a7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="152a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="152a7-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="152a7-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="152a7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="152a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="152a7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="152a7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="152a7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="152a7-112">Area:</span></span>  <br/> |<span data-ttu-id="152a7-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="152a7-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="152a7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="152a7-114">Remarks</span></span>

<span data-ttu-id="152a7-115">Eine Unterhaltungsthreads stellt eine Reihe von Nachrichten und Antworten.</span><span class="sxs-lookup"><span data-stu-id="152a7-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="152a7-116">Diese Eigenschaften werden für die erste Nachricht in einem Thread, in der Regel an die **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="152a7-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="152a7-117">Nachfolgende Nachrichten im Thread sollte im gleiche Thema ohne Änderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="152a7-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="152a7-118">Die **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))-Eigenschaft gibt die Reihenfolge Beziehung zwischen nachfolgenden Nachrichten und Antworten an.</span><span class="sxs-lookup"><span data-stu-id="152a7-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="152a7-119">Die Verwendung ist optional, auch wenn diese Eigenschaften festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="152a7-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="152a7-120">Eine Nachricht Speicheranbieter hat die Möglichkeit der Sicherstellung der, die diese Eigenschaften immer für eingehende und ausgehende Nachrichten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="152a7-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="152a7-121">Wenn diese Eigenschaften sind bereits festgelegten sollten sie nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="152a7-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="152a7-122">Wenn dies nicht der Fall ist, können **PR_NORMALIZED_SUBJECT**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="152a7-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="152a7-123">Maßnahmen sollten getroffen werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="152a7-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="152a7-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="152a7-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="152a7-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="152a7-125">Protocol specifications</span></span>

<span data-ttu-id="152a7-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="152a7-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="152a7-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="152a7-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="152a7-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="152a7-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="152a7-129">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="152a7-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="152a7-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="152a7-130">Header files</span></span>

<span data-ttu-id="152a7-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="152a7-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="152a7-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="152a7-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="152a7-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="152a7-133">Mapitags.h</span></span>
  
> <span data-ttu-id="152a7-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="152a7-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="152a7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="152a7-135">See also</span></span>



[<span data-ttu-id="152a7-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="152a7-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="152a7-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="152a7-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="152a7-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="152a7-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="152a7-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="152a7-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


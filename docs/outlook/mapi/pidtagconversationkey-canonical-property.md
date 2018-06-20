---
title: Kanonische PidTagConversationKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4aec52497e02e99423fa50f378cd35dbf366c37c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794256"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="403dd-103">Kanonische PidTagConversationKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="403dd-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="403dd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="403dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="403dd-105">Enthält den Unterhaltung Schlüssel in Microsoft Outlook verwendet nur, wenn **IPM suchen. Nachrichten-Managers** Nachrichten wie die Nachricht, Downloadverlauf für ein Konto Post Office Protocol (POP3) enthält.</span><span class="sxs-lookup"><span data-stu-id="403dd-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="403dd-106">Diese Eigenschaft ist in Microsoft Exchange Server veraltet.</span><span class="sxs-lookup"><span data-stu-id="403dd-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="403dd-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="403dd-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="403dd-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="403dd-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="403dd-109">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="403dd-109">Identifier:</span></span>  <br/> |<span data-ttu-id="403dd-110">0x000b</span><span class="sxs-lookup"><span data-stu-id="403dd-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="403dd-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="403dd-111">Data type:</span></span>  <br/> |<span data-ttu-id="403dd-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="403dd-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="403dd-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="403dd-113">Area:</span></span>  <br/> |<span data-ttu-id="403dd-114">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="403dd-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="403dd-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="403dd-115">Remarks</span></span>

<span data-ttu-id="403dd-116">Wenn Sie e-Mail-Nachrichten als Unterhaltungen und Konvertieren von Nachrichteneigenschaften in [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md)zugreifen möchten, verwenden Sie diese Eigenschaft nicht. Verwenden Sie stattdessen die kanonischen Eigenschaften [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und [Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="403dd-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="403dd-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="403dd-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="403dd-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="403dd-118">Protocol specifications</span></span>

<span data-ttu-id="403dd-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="403dd-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="403dd-120">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="403dd-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="403dd-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="403dd-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="403dd-122">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="403dd-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="403dd-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="403dd-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="403dd-124">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="403dd-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="403dd-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="403dd-125">Header files</span></span>

<span data-ttu-id="403dd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="403dd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="403dd-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="403dd-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="403dd-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="403dd-128">Mapitags.h</span></span>
  
> <span data-ttu-id="403dd-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="403dd-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="403dd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="403dd-130">See also</span></span>



[<span data-ttu-id="403dd-131">IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="403dd-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="403dd-132">MAPI-Spezialordner</span><span class="sxs-lookup"><span data-stu-id="403dd-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="403dd-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="403dd-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="403dd-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="403dd-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="403dd-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="403dd-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="403dd-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="403dd-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


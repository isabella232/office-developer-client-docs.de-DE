---
title: PidTagConversationKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334699"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="9420b-103">PidTagConversationKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9420b-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="9420b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9420b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9420b-105">Enthält den unterhaltungsschlüssel, der in Microsoft Outlook beim Suchen von **IPM verwendet wird. MessageManager-Nachrichten,** z. B. die Nachricht, die den Downloadverlauf für ein Post Office Protocol (POP3)-Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="9420b-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="9420b-106">Diese Eigenschaft ist in diesem Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9420b-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9420b-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9420b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="9420b-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="9420b-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="9420b-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9420b-109">Identifier:</span></span>  <br/> |<span data-ttu-id="9420b-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="9420b-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="9420b-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9420b-111">Data type:</span></span>  <br/> |<span data-ttu-id="9420b-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9420b-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9420b-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9420b-113">Area:</span></span>  <br/> |<span data-ttu-id="9420b-114">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="9420b-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9420b-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9420b-115">Remarks</span></span>

<span data-ttu-id="9420b-116">Verwenden Sie diese Eigenschaft nicht, wenn Sie auf E-Mail-Nachrichten als Unterhaltungen zugreifen und Nachrichteneigenschaften in [TNEF (Transport-Neutral Encapsulation Format)](transport-neutral-encapsulation-format-tnef.md)konvertieren. verwenden Sie stattdessen [die kanonischen Eigenschaften PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und [PidTagConversationTopic.](pidtagconversationtopic-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9420b-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9420b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9420b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9420b-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9420b-118">Protocol specifications</span></span>

<span data-ttu-id="9420b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9420b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9420b-120">Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9420b-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9420b-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9420b-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9420b-122">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9420b-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="9420b-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9420b-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9420b-124">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="9420b-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9420b-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9420b-125">Header files</span></span>

<span data-ttu-id="9420b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9420b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9420b-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9420b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9420b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9420b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9420b-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9420b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9420b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9420b-130">See also</span></span>



[<span data-ttu-id="9420b-131">IPM-Unterstruktur</span><span class="sxs-lookup"><span data-stu-id="9420b-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="9420b-132">MAPI-Sonderordner</span><span class="sxs-lookup"><span data-stu-id="9420b-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="9420b-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9420b-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9420b-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9420b-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9420b-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9420b-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9420b-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9420b-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


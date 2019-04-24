---
title: Kanonische Pidtagconversationkey (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334699"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="33d4a-103">Kanonische Pidtagconversationkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33d4a-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="33d4a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33d4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33d4a-105">Enthält den Unterhaltungs Schlüssel, der in Microsoft Outlook nur beim Auffinden von IPM verwendet wird **. MessageManager** -Nachrichten wie die Nachricht, die den Downloadverlauf für ein POP3-Konto (Post Office Protocol) enthält.</span><span class="sxs-lookup"><span data-stu-id="33d4a-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="33d4a-106">Diese Eigenschaft ist in Microsoft Exchange Server veraltet.</span><span class="sxs-lookup"><span data-stu-id="33d4a-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33d4a-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="33d4a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="33d4a-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="33d4a-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="33d4a-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="33d4a-109">Identifier:</span></span>  <br/> |<span data-ttu-id="33d4a-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="33d4a-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="33d4a-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="33d4a-111">Data type:</span></span>  <br/> |<span data-ttu-id="33d4a-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="33d4a-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="33d4a-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="33d4a-113">Area:</span></span>  <br/> |<span data-ttu-id="33d4a-114">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="33d4a-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33d4a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33d4a-115">Remarks</span></span>

<span data-ttu-id="33d4a-116">Wenn Sie auf e-Mail-Nachrichten als Unterhaltungen zugreifen und Nachrichteneigenschaften in das [Transport Neutral encapsulatIon Format (TNEF)](transport-neutral-encapsulation-format-tnef.md)konvertieren, verwenden Sie diese Eigenschaft nicht; Verwenden Sie stattdessen die kanonischen Eigenschaften [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) und [eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="33d4a-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33d4a-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="33d4a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33d4a-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="33d4a-118">Protocol specifications</span></span>

<span data-ttu-id="33d4a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33d4a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33d4a-120">Enthält Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="33d4a-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33d4a-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33d4a-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33d4a-122">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="33d4a-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="33d4a-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33d4a-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33d4a-124">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="33d4a-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33d4a-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="33d4a-125">Header files</span></span>

<span data-ttu-id="33d4a-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="33d4a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="33d4a-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="33d4a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="33d4a-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="33d4a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="33d4a-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="33d4a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33d4a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33d4a-130">See also</span></span>



[<span data-ttu-id="33d4a-131">IPM-unterStruktur</span><span class="sxs-lookup"><span data-stu-id="33d4a-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="33d4a-132">MAPI-Spezialordner</span><span class="sxs-lookup"><span data-stu-id="33d4a-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="33d4a-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33d4a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33d4a-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33d4a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33d4a-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="33d4a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33d4a-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="33d4a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


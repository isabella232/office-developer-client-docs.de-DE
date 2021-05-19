---
title: PidTagConversationIndex (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334720"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="2c4dc-103">PidTagConversationIndex (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2c4dc-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="2c4dc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c4dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c4dc-105">Enthält einen binären Wert, der die relative Position dieser Nachricht in einem Unterhaltungsthread angibt.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c4dc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2c4dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c4dc-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="2c4dc-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="2c4dc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2c4dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c4dc-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="2c4dc-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="2c4dc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2c4dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c4dc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c4dc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c4dc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2c4dc-112">Area:</span></span>  <br/> |<span data-ttu-id="2c4dc-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="2c4dc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c4dc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c4dc-114">Remarks</span></span>

<span data-ttu-id="2c4dc-115">Ein Unterhaltungsthread stellt eine Reihe von Nachrichten und Antworten dar.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="2c4dc-116">Diese Eigenschaft wird in der Regel mit verkettten Zeitstempelwerten implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="2c4dc-117">Die Verwendung ist optional, auch **wenn PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="2c4dc-118">MAPI bietet die [ScCreateConversationIndex-Funktion](sccreateconversationindex.md) zum Erstellen oder Aktualisieren eines Unterhaltungsindex.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="2c4dc-119">Die Funktion verwendet den aktuellen Indexwert als gezähltes Bytearray und gibt den Indexwert mit einem Zeitstempel zurück, der am Ende verkettt ist.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="2c4dc-120">Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellt, sollte **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="2c4dc-121">Ein Nachrichtenspeicheranbieter hat die Möglichkeit,  zu PR_CONVERSATION_INDEX ein- oder ausgehenden Nachrichten immer festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="2c4dc-122">Dazu ruft sie **ScCreateConversationIndex** auf, entweder mit dem vorhandenen Wert, wenn diese Eigenschaft festgelegt ist, oder mit NULL, falls nicht.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="2c4dc-123">Diese Aktion sollte ausgeführt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="2c4dc-124">Alle Nachrichten mit demselben  Wert für PR_CONVERSATION_TOPIC können für diese Eigenschaft sortiert werden, um die hierarchische Beziehung der Nachrichten zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2c4dc-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2c4dc-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c4dc-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2c4dc-126">Protocol specifications</span></span>

<span data-ttu-id="2c4dc-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c4dc-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c4dc-128">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c4dc-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c4dc-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c4dc-130">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c4dc-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2c4dc-131">Header files</span></span>

<span data-ttu-id="2c4dc-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c4dc-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c4dc-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c4dc-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c4dc-134">Mapitags.h</span></span>
  
> <span data-ttu-id="2c4dc-135">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2c4dc-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c4dc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c4dc-136">See also</span></span>



[<span data-ttu-id="2c4dc-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c4dc-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c4dc-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2c4dc-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c4dc-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2c4dc-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c4dc-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2c4dc-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


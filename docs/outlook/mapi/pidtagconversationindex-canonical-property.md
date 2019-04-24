---
title: Kanonische PidTagConversationIndex-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334720"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="8bd35-103">Kanonische PidTagConversationIndex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8bd35-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="8bd35-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bd35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bd35-105">Enthält einen Binary-Wert, der die relative Position dieser Nachricht in einem konversationsthread angibt.</span><span class="sxs-lookup"><span data-stu-id="8bd35-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bd35-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8bd35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bd35-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="8bd35-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="8bd35-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8bd35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bd35-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="8bd35-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="8bd35-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8bd35-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bd35-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8bd35-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8bd35-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8bd35-112">Area:</span></span>  <br/> |<span data-ttu-id="8bd35-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="8bd35-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bd35-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bd35-114">Remarks</span></span>

<span data-ttu-id="8bd35-115">Ein konversationsthread stellt eine Reihe von Nachrichten und Antworten dar.</span><span class="sxs-lookup"><span data-stu-id="8bd35-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="8bd35-116">Diese Eigenschaft wird normalerweise mit verketteten Zeitstempelwerten implementiert.</span><span class="sxs-lookup"><span data-stu-id="8bd35-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="8bd35-117">Die Verwendung ist optional, auch wenn **PR_CONVERSATION_TOPIC** ([eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8bd35-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="8bd35-118">MAPI stellt die [ScCreateConversationIndex](sccreateconversationindex.md) -Funktion zum Erstellen oder Aktualisieren eines Unterhaltungsindex bereit.</span><span class="sxs-lookup"><span data-stu-id="8bd35-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="8bd35-119">Die Funktion verwendet den aktuellen Indexwert als Gezähltes Bytearray und gibt den Indexwert mit einem Zeitstempel zurück, der am Ende verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="8bd35-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="8bd35-120">Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellt, sollte **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8bd35-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="8bd35-121">Ein Nachrichtenspeicher Anbieter kann sicherstellen, dass **PR_CONVERSATION_INDEX** immer für eingehende oder ausgehende Nachrichten festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8bd35-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="8bd35-122">Dies kann durch Aufrufen von **ScCreateConversationIndex**, entweder mit dem vorhandenen Wert, wenn diese Eigenschaft festgelegt ist, oder mit NULL, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="8bd35-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="8bd35-123">Diese Aktion sollte vor dem Aufruf von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8bd35-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="8bd35-124">Alle Nachrichten, die den gleichen Wert für **PR_CONVERSATION_TOPIC** haben, können nach dieser Eigenschaft sortiert werden, um die hierarchische Beziehung der Nachrichten aufzudecken.</span><span class="sxs-lookup"><span data-stu-id="8bd35-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8bd35-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8bd35-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bd35-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8bd35-126">Protocol specifications</span></span>

<span data-ttu-id="8bd35-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bd35-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bd35-128">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8bd35-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bd35-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bd35-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bd35-130">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8bd35-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bd35-131">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8bd35-131">Header files</span></span>

<span data-ttu-id="8bd35-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8bd35-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bd35-133">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8bd35-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bd35-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8bd35-134">Mapitags.h</span></span>
  
> <span data-ttu-id="8bd35-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8bd35-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bd35-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bd35-136">See also</span></span>



[<span data-ttu-id="8bd35-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bd35-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bd35-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bd35-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bd35-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8bd35-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bd35-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8bd35-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


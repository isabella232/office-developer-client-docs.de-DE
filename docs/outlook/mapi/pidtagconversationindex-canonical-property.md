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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383625"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="02c21-103">PidTagConversationIndex (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="02c21-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="02c21-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02c21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02c21-105">Enthält einen binären Wert, der die relative Position dieser Nachricht innerhalb einer Unterhaltungsthreads angibt.</span><span class="sxs-lookup"><span data-stu-id="02c21-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02c21-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="02c21-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02c21-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="02c21-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="02c21-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="02c21-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02c21-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="02c21-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="02c21-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="02c21-110">Data type:</span></span>  <br/> |<span data-ttu-id="02c21-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="02c21-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="02c21-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="02c21-112">Area:</span></span>  <br/> |<span data-ttu-id="02c21-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="02c21-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02c21-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02c21-114">Remarks</span></span>

<span data-ttu-id="02c21-115">Eine Unterhaltungsthreads stellt eine Reihe von Nachrichten und Antworten.</span><span class="sxs-lookup"><span data-stu-id="02c21-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="02c21-116">Diese Eigenschaft wird normalerweise mithilfe von verketteten Zeitstempelwerten implementiert.</span><span class="sxs-lookup"><span data-stu-id="02c21-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="02c21-117">Die Verwendung ist optional, selbst wenn **PR_CONVERSATION_TOPIC** ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="02c21-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="02c21-118">MAPI bietet die [ScCreateConversationIndex](sccreateconversationindex.md) -Funktion zum Erstellen oder Aktualisieren eines Unterhaltung Indexes.</span><span class="sxs-lookup"><span data-stu-id="02c21-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="02c21-119">Die Funktion nimmt den aktuellen Indexwert als Bytearray gezählte und gibt den Indexwert mit einem Zeitstempel verkettet, auf die Seite zurück.</span><span class="sxs-lookup"><span data-stu-id="02c21-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="02c21-120">Eine Nachricht, die eine Antwort auf eine andere Nachricht darstellen soll **ScCreateConversationIndex** verwenden, um diese Eigenschaft zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="02c21-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="02c21-121">Eine Nachricht Speicheranbieter hat die Möglichkeit der Sicherstellung, die **PR_CONVERSATION_INDEX** immer für eingehende und ausgehende Nachrichten festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="02c21-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="02c21-122">Hierzu können sie **ScCreateConversationIndex**, entweder mit den vorhandenen Wert, wenn diese Eigenschaft festgelegt ist oder mit NULL, falls noch nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02c21-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="02c21-123">Diese Aktion sollte berücksichtigt werden, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="02c21-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="02c21-124">Alle Nachrichten, die den gleichen Wert für **PR_CONVERSATION_TOPIC** aufweisen können auf diese Eigenschaft, um die hierarchische Beziehung der Nachrichten anzuzeigen sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="02c21-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02c21-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="02c21-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02c21-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="02c21-126">Protocol specifications</span></span>

<span data-ttu-id="02c21-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02c21-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02c21-128">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="02c21-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02c21-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02c21-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02c21-130">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="02c21-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02c21-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="02c21-131">Header files</span></span>

<span data-ttu-id="02c21-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02c21-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="02c21-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="02c21-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="02c21-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02c21-134">Mapitags.h</span></span>
  
> <span data-ttu-id="02c21-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="02c21-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02c21-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02c21-136">See also</span></span>



[<span data-ttu-id="02c21-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02c21-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02c21-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02c21-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02c21-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="02c21-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02c21-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="02c21-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


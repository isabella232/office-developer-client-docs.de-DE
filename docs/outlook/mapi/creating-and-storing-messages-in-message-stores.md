---
title: Erstellen und Speichern von Nachrichten in Nachrichtenspeichern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589175"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="57274-103">Erstellen und Speichern von Nachrichten in Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="57274-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="57274-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57274-p101">Wie Ihr Nachrichtenspeicheranbieter Nachrichten in dem zugrunde liegenden Speichermechanismus erstellt und speichert, ist im Wesentlichen von dem zugrunde liegenden Speichermechanismus selbst abhängig. Im Allgemeinen müssen Sie nur Code schreiben, um die Eigenschaften einer Nachricht und deren Werte zu speichern.</span><span class="sxs-lookup"><span data-stu-id="57274-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="57274-p102">Wenn der Nachrichtenspeicheranbieter eine neue Nachricht erstellt, muss der Anbieter die Nachricht mit den erforderlichen Eigenschaften für Nachrichten erstellen. Eine Liste dieser Eigenschaften ist in der Dokumentation für die [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)-Schnittstelle zu finden. Danach fügen Clientanwendungen weitere Eigenschaften mit [IMAPIProp](imapipropiunknown.md)-Methoden hinzu.</span><span class="sxs-lookup"><span data-stu-id="57274-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="57274-110">Wenn der Nachrichtenspeicheranbieter eine Nachricht im zugrunde liegenden Speichermechanismus speichert, muss der Anbieter die Eigenschaften der Nachricht durchlaufen und diese im zugrunde liegenden Speichermechanismus speichern, damit diese vollständig wiederhergestellt werden können, wenn die Nachricht später geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="57274-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="57274-p103">MAPI erfordert, dass die Eigenschaften in [IMessage](imessageimapiprop.md)-Schnittstellen abgewickelt werden, was bedeutet, dass daran vorgenommene Änderungen erst dauerhaft sind, wenn die [IMAPIProp::SaveChanges](imapiprop-savechanges.md)-Methode im Nachrichtenobjekt aufgerufen wird. Der Nachrichtenspeicheranbieter ist für das Implementieren dieses Verhaltens verantwortlich. Dies ist in der Regel nicht schwierig. Es bedeutet einfach, dass Eigenschaften im Arbeitsspeicher gehalten werden, während sie geändert werden, und dass sie im zugrunde liegenden Speichermechanismus gespeichert werden, wenn **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="57274-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="57274-114">Einige Eigenschaften in Nachrichtenobjekten haben bezüglich der **SaveChanges**-Methode eine besondere Semantik für Clientanwendungen:</span><span class="sxs-lookup"><span data-stu-id="57274-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="57274-115">Einige Eigenschaften sollten Lese-/Schreibzugriff haben, bevor **SaveChanges** aufgerufen wird, danach aber schreibgeschützt sein.</span><span class="sxs-lookup"><span data-stu-id="57274-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="57274-116">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) wird beispielsweise von der Clientanwendung festgelegt, die die Nachricht erstellt ( und verfügt daher über Lese-/Schreibzugriff), kann aber nach dem ersten Aufruf von **SaveChanges** nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="57274-116">For example, **PR_MESSAGE_FLAGS** ( [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="57274-p105">Einige Eigenschaften haben spezielle Beziehungen zu Eigenschaften in dem Ordner, in dem sie sich befinden, oder zu **IMAPIFolder**-Methoden. Die **PR_MESSAGE_FLAGS**-Eigenschaft weist beispielsweise eine Beziehung zu den Flags auf, die im [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)-Aufruf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57274-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="57274-119">Einige Eigenschaften sind möglicherweise erst verfügbar, wenn **SaveChanges** zum ersten Mal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="57274-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="57274-120">Die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft ist beispielsweise erst verfügbar, wenn **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="57274-120">For example, the **PR_ENTRYID** ( [PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="57274-121">Einige Eigenschaften können spezielle Beziehungen zu anderen Eigenschaften des Nachrichtenobjekts haben.</span><span class="sxs-lookup"><span data-stu-id="57274-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="57274-122">Beispielsweise wird die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft in der Regel von der **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))-Eigenschaft in Nachrichtenspeicheranbietern abgeleitet, die Nachrichten im Rich Text Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57274-122">For example, the **PR_BODY** ( [PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ( [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="57274-123">Einige Eigenschaften werden von mehr als einem Objekttyp im Zusammenhang mit Nachrichtenspeicheranbietern verwendet.</span><span class="sxs-lookup"><span data-stu-id="57274-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="57274-124">Beispielsweise ist die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft in Ordner- und Nachrichtenobjekten sowie in Nachrichtenspeicheranbietern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="57274-124">For example, the **PR_STORE_SUPPORT_MASK** ( [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="57274-125">Es liegt in der Verantwortung des Nachrichtenspeicheranbieters, die korrekte Semantik für derartige Eigenschaften zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="57274-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57274-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57274-126">See also</span></span>



[<span data-ttu-id="57274-127">Implementieren von Nachrichten in Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="57274-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)


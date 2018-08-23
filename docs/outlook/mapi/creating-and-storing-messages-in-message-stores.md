---
title: Erstellen und Speichern von Nachrichten in Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589175"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="d0e44-103">Erstellen und Speichern von Nachrichten in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="d0e44-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="d0e44-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0e44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0e44-p101">Wie Ihre Nachricht Speicheranbieter erstellt und speichert Nachrichten in der zugrunde liegende Speichermechanismus h�ngt stark von der zugrunde liegende Speichermechanismus selbst. Im Allgemeinen m�ssen Sie nur Code schreiben, um die Eigenschaften einer Nachricht und deren Werte beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d0e44-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="d0e44-p102">Wenn die Nachricht speichern Anbieter erstellt eine neue Nachricht, muss des Anbieters die Nachricht mit den erforderlichen Eigenschaften f�r Nachrichten zu erstellen. Eine Liste dieser Eigenschaften finden Sie in der Dokumentation f�r die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) Schnittstelle. Anschlie�end hinzuf�gen-Clientanwendungen alle zus�tzlichen Eigenschaften mit [IMAPIProp](imapipropiunknown.md) Methoden.</span><span class="sxs-lookup"><span data-stu-id="d0e44-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="d0e44-110">Wenn die Nachricht speichern Anbieter speichert eine Nachricht an die zugrunde liegende Speichermechanismus, muss der Anbieter Eigenschaften der Meldung durchlaufen, und speichern Sie sie in der zugrunde liegende Speichermechanismus, so, dass sie vollst�ndig wiederhergestellt werden k�nnen, wenn die Nachricht sp�ter ge�ffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d0e44-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="d0e44-p103">MAPI erfordert, dass die Eigenschaften f�r [IMessage](imessageimapiprop.md) Schnittstellen durchgef�hrt werden, was bedeutet, dass �nderungen vorgenommen werden, bis die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, auf das Objekt "Message aufgerufen wird" nicht dauerhaft entfernt werden. Der Nachricht Speicheranbieter ist verantwortlich f�r die Implementierung dieses Verhalten. Dies ist in der Regel nicht schwierig. Es bedeutet ganz einfach Eigenschaften im Arbeitsspeicher gedr�ckt halten, w�hrend sie ge�ndert werden und deren Aufnahme in der zugrunde liegende Speichermechanismus, wenn **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0e44-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="d0e44-114">Einige Eigenschaften f�r Nachrichtenobjekte, die haben spezielle Semantik f�r Clientanwendungen in Bezug auf die **SaveChanges** -Methode, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d0e44-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="d0e44-115">Einige Eigenschaften sollte Lese-/Schreibzugriff, bevor **SaveChanges**, aber schreibgesch�tzt danach aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0e44-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="d0e44-116">Beispielsweise **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) zunächst von der Clientanwendung, die die Nachricht erstellt (und somit besteht Lese-/Schreibzugriff) festgelegt ist, aber nicht nach dem ersten Aufruf von **SaveChanges**geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d0e44-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="d0e44-p105">Einige Eigenschaften haben spezielle Beziehungen zu Eigenschaften f�r den Ordner, den sie in oder **IMAPIFolder** Methoden sind. Beispielsweise bezieht sich die **PR_MESSAGE_FLAGS** -Eigenschaft auf die Kennzeichen f�r den Anruf [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0e44-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="d0e44-119">Einige Eigenschaften m�glicherweise nicht verf�gbar, bis **SaveChanges** zum ersten Mal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0e44-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="d0e44-120">Zum Beispiel die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) möglicherweise nicht zur Verfügung, bis **SaveChanges** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d0e44-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="d0e44-121">Einige Eigenschaften haben besondere Beziehungen mit anderen Eigenschaften auf Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d0e44-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="d0e44-122">Beispielsweise wird die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft in der Regel aus der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) in der Nachricht Anbieter abgeleitet, die Nachrichten im Rich Text Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d0e44-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="d0e44-123">Einige Eigenschaften werden von mehr als eine Objekttyp im Zusammenhang mit e-Mail-Speicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0e44-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="d0e44-124">Beispielsweise ist die **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft auf den Ordner und die Nachricht, dass Objekte sowie Nachricht Speichern von Objekten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0e44-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="d0e44-125">Es ist Aufgabe des Anbieters Nachricht an die richtige Semantik f�r solche Eigenschaften implementieren.</span><span class="sxs-lookup"><span data-stu-id="d0e44-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0e44-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0e44-126">See also</span></span>



[<span data-ttu-id="d0e44-127">Implementieren von Nachrichten in Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="d0e44-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)


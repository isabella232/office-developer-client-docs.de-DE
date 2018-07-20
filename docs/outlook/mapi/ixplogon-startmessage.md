---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3758cf72aa79dbf500138e96872352950fafbd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792886"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="fc222-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="fc222-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="fc222-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc222-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc222-105">Initiiert die Übertragung von einer eingehenden Nachricht aus der Adressbuchhierarchie auf die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fc222-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="fc222-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc222-106">Parameters</span></span>

 <span data-ttu-id="fc222-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc222-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fc222-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="fc222-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fc222-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="fc222-109">_lpMessage_</span></span>
  
> <span data-ttu-id="fc222-110">[in] Ein Zeiger auf ein Objekt "Message" (für die eingehende Nachricht), die Lese-/Schreibberechtigung hat, die von der Adressbuchhierarchie zum Aufrufen und Bearbeiten dieser Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc222-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="fc222-111">Dieses Objekt bleibt gültig bis, nachdem der Adressbuchhierarchie aus dem Aufruf von **IXPLogon::StartMessage**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc222-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="fc222-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="fc222-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="fc222-113">[out] Ein Zeiger auf ein Referenzwert, der die Nachricht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fc222-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="fc222-114">Die MAPI-Warteschlange initialisiert dieser Wert auf 1, bevor sie den Zeiger für den Transportanbieter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fc222-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc222-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc222-115">Return value</span></span>

<span data-ttu-id="fc222-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc222-116">S_OK</span></span> 
  
> <span data-ttu-id="fc222-117">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fc222-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc222-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc222-118">Remarks</span></span>

<span data-ttu-id="fc222-119">Die MAPI-Warteschlange die **IXPLogon::StartMessage** -Methode aufgerufen, um die Übertragung von einer eingehenden Nachricht aus der Adressbuchhierarchie auf die MAPI-Warteschlange zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="fc222-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="fc222-120">Vor Beginn der Adressbuchhierarchie mit der Meldung von _LpMessage_sollten sie eine Referenz zu Nachrichten im _LpulMsgRef_ -Parameter für die mögliche Verwendung durch einen Aufruf an die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode speichern.</span><span class="sxs-lookup"><span data-stu-id="fc222-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="fc222-121">Während eines Anrufs **StartMessage** die MAPI-Warteschlange verarbeitet Methoden für Objekte, die während der Übertragung der Nachricht geöffnet, und es auch für die Verarbeitung von Anlagen.</span><span class="sxs-lookup"><span data-stu-id="fc222-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="fc222-122">Diese Verarbeitung kann sehr lange dauern.</span><span class="sxs-lookup"><span data-stu-id="fc222-122">This processing can take a long time.</span></span> <span data-ttu-id="fc222-123">Transportanbieter können die [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) Callback-Funktion für die MAPI-Warteschlange während diese Verarbeitung freizugebende CPU-Zeit für andere Systemaufgaben häufig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc222-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="fc222-124">Alle Empfänger in der Empfänger Tabelle, mit der der Adressbuchhierarchie für die Nachricht erstellt, müssen alle erforderliche reagieren auf Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="fc222-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="fc222-125">Bei Bedarf kann der Anbieter einen benutzerdefinierten Empfänger zur Darstellung von eines bestimmten Empfängers erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc222-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="fc222-126">Wenn der Anbieter einen Empfänger Eintrag, der Informationen enthält erzeugen kann, sollten sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="fc222-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="fc222-127">Beispielsweise sollte ein ein Transportdienstes genügend Informationen über eine Adressbuchanbieter Empfänger Format hat, dass er eine gültige Eintrags-ID für einen Empfänger für dieses Format erstellen kann, die Eintrags-ID erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc222-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="fc222-128">Wenn alle Eigenschaften Nontransmittable empfangen werden, sollte der Adressbuchhierarchie nicht in die neue Nachricht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="fc222-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="fc222-129">Der Adressbuchhierarchie sollten jedoch alle Übertragungseinehit Eigenschaften speichern, die sie in der neuen Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="fc222-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="fc222-130">Wenn die eingehende Nachricht einen Übermittlungsbericht oder einen Unzustellbarkeitsbericht und der Adressbuchhierarchie nicht mit der [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode zum Generieren von Berichten aus der ursprünglichen Nachricht kann, sollte der Anbieter die Nachricht mit Auffüllen die entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc222-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="fc222-131">Allerdings festlegen nicht der Adressbuchhierarchie die Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fc222-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="fc222-132">Um den entsprechenden MAPI-Nachrichtenspeicher nach der Verarbeitung die eingehende Nachricht speichern, ruft der Adressbuchhierarchie die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fc222-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="fc222-133">Wenn der Adressbuchhierarchie Nachrichten zum Übergeben an die Warteschlange MAPI nicht vorhanden ist, kann die eingehende Nachricht unterbrochen werden durch den Aufruf der **StartMessage** ohne einen Aufruf **SaveChanges**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fc222-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="fc222-134">Alle Objekte, die während eines Anrufs **StartMessage** der Adressbuchhierarchie öffnet sollten vor der Rückgabe freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fc222-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="fc222-135">Der Anbieter sollte jedoch nicht Message-Objekts freigeben, die die MAPI-Warteschlange ursprünglich in der _LpMessage_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="fc222-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="fc222-136">Wenn **StartMessage** einen Fehler zurückgibt, wird die Nachricht im Prozess wird aufgehoben, ohne dass Änderungen gespeichert und geht verloren.</span><span class="sxs-lookup"><span data-stu-id="fc222-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="fc222-137">In diesem Fall sollte der Adressbuchhierarchie das Flag NOTIFY_CRITICAL_ERROR mit einem Aufruf der [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode übergeben, und rufen Sie die [IXPLogon::Poll](ixplogon-poll.md) -Methode, um die MAPI-Warteschlange zu benachrichtigen, die dass er eine Bedingung Schwerwiegender Fehler ist.</span><span class="sxs-lookup"><span data-stu-id="fc222-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="fc222-138">Weitere Informationen finden Sie unter [Interaktion mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="fc222-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc222-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc222-139">See also</span></span>



[<span data-ttu-id="fc222-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="fc222-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="fc222-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="fc222-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="fc222-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="fc222-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="fc222-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="fc222-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="fc222-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="fc222-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="fc222-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="fc222-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="fc222-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="fc222-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="fc222-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc222-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)


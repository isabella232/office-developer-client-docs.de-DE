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
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427605"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="13657-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="13657-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="13657-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13657-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13657-105">Initiiert die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="13657-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="13657-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13657-106">Parameters</span></span>

 <span data-ttu-id="13657-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13657-107">_ulFlags_</span></span>
  
> <span data-ttu-id="13657-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="13657-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="13657-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="13657-109">_lpMessage_</span></span>
  
> <span data-ttu-id="13657-110">in Ein Zeiger auf ein Nachrichtenobjekt (das die eingehende Nachricht darstellt) mit Lese-/Schreibzugriff, das vom Transportanbieter zum zugreifen und Bearbeiten dieser Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13657-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="13657-111">Dieses Objekt bleibt gültig, bis der Transportanbieter vom Aufruf an **IXPLogon:: StartMessage**zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="13657-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="13657-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="13657-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="13657-113">Out Ein Zeiger auf einen Verweiswert, der der Nachricht zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="13657-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="13657-114">Der MAPI-Spooler initialisiert diesen Wert mit 1, bevor er den Zeiger an den Transportanbieter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="13657-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13657-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13657-115">Return value</span></span>

<span data-ttu-id="13657-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="13657-116">S_OK</span></span> 
  
> <span data-ttu-id="13657-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="13657-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13657-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13657-118">Remarks</span></span>

<span data-ttu-id="13657-119">Der MAPI-Spooler Ruft die **IXPLogon:: StartMessage** -Methode auf, um die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="13657-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="13657-120">Bevor der Transportanbieter mit der Verwendung der Nachricht beginnt, auf die von _lpMessage_verwiesen wird, sollte ein Nachrichtenverweis im _lpulMsgRef_ -Parameter gespeichert werden, damit Sie von einem Aufruf der [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="13657-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="13657-121">Während eines **StartMessage** -Aufrufs verarbeitet der MAPI-Spooler Methoden für Objekte, die während der Übertragung der Nachricht geöffnet werden, und verarbeitet auch Anlagen.</span><span class="sxs-lookup"><span data-stu-id="13657-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="13657-122">Diese Verarbeitung kann sehr viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="13657-122">This processing can take a long time.</span></span> <span data-ttu-id="13657-123">Transport Anbieter können die [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) -Rückruffunktion für den MAPI-Spooler während dieser Verarbeitung häufig aufrufen, um die CPU-Zeit für andere Systemaufgaben zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="13657-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="13657-124">Alle Empfänger in der Empfängertabelle, die der Transportanbieter für die Nachricht erstellt, müssen alle erforderlichen Adressierungs Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="13657-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="13657-125">Bei Bedarf kann der Anbieter einen benutzerdefinierten Empfänger erstellen, um einen bestimmten Empfänger darzustellen.</span><span class="sxs-lookup"><span data-stu-id="13657-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="13657-126">Wenn der Anbieter jedoch einen Empfängereintrag mit weiteren Informationen erstellen kann, sollte dies der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="13657-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="13657-127">Wenn beispielsweise ein Transportanbieter über genügend Informationen zum Empfänger Format des Adressbuch Anbieters verfügt, dass er eine gültige Eintrags-ID für einen Empfänger für dieses Format erstellen kann, sollte er die Eintrags-ID erstellen.</span><span class="sxs-lookup"><span data-stu-id="13657-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="13657-128">Wenn nicht übertragbare Eigenschaften empfangen werden, sollte der Transportanbieter diese nicht in der neuen Nachricht speichern.</span><span class="sxs-lookup"><span data-stu-id="13657-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="13657-129">Der Transportanbieter sollte jedoch alle übertragenen Eigenschaften speichern, die er in der neuen Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="13657-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="13657-130">Wenn die eingehende Nachricht ein zugestellter Bericht oder ein Unzustellbarkeitsbericht ist und der Transportanbieter die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode nicht verwenden kann, um den Bericht aus der ursprünglichen Nachricht zu generieren, sollte der Anbieter die Nachricht selbst mit die entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="13657-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="13657-131">Der Transportanbieter kann jedoch die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft der Nachricht nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="13657-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="13657-132">Wenn die eingehende Nachricht nach der Verarbeitung im entsprechenden MAPI-Nachrichtenspeicher gespeichert werden soll, ruft der Transportanbieter die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="13657-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="13657-133">Wenn der Transportanbieter keine Nachrichten an den MAPI-Spooler übergibt, kann er die eingehende Nachricht beenden, indem er vom **StartMessage** -Aufruf zurückkehrt \*\*\*\*, ohne SaveChanges zu aufrufen.</span><span class="sxs-lookup"><span data-stu-id="13657-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="13657-134">Alle Objekte, die der Transportanbieter während eines **StartMessage** -Aufrufs geöffnet hat, sollten vor der Rückgabe freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="13657-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="13657-135">Der Anbieter sollte jedoch das Message-Objekt, das der MAPI-Spooler ursprünglich im _lpMessage_ -Parameter übergeben hat, nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="13657-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="13657-136">Wenn **StartMessage** einen Fehler zurückgibt, wird die Nachricht in Process ohne gespeicherte Änderungen freigegeben und geht verloren.</span><span class="sxs-lookup"><span data-stu-id="13657-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="13657-137">In diesem Fall sollte der Transportanbieter das NOTIFY_CRITICAL_ERROR-Flag mit einem Aufruf an die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode weiterleiten und die [IXPLogon::P oll](ixplogon-poll.md) -Methode aufrufen, um die MAPI-Warteschlange zu benachrichtigen, dass Sie sich in einem schwerwiegenden Fehlerzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="13657-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="13657-138">Weitere Informationen finden Sie unter [interagieren mit dem MAPI](interacting-with-the-mapi-spooler.md)-Spooler.</span><span class="sxs-lookup"><span data-stu-id="13657-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13657-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13657-139">See also</span></span>



[<span data-ttu-id="13657-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="13657-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="13657-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="13657-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="13657-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="13657-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="13657-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="13657-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="13657-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="13657-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="13657-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="13657-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="13657-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="13657-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="13657-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13657-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)


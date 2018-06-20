---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a60b813a52779b28124ab6d69b493def35b14aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792294"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="e5691-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e5691-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="e5691-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5691-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5691-105">Macht dauerhaft entfernt alle Änderungen, die seit dem letzten Speichervorgang auf ein Objekt vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e5691-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e5691-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5691-106">Parameters</span></span>

 <span data-ttu-id="e5691-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5691-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e5691-108">[in] Eine Bitmaske aus Flags, die steuert, was auf das Objekt geschieht, wenn die **IMAPIProp::SaveChanges** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e5691-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="e5691-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e5691-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="e5691-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="e5691-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="e5691-111">Gibt an, dass die Nachricht von einem Microsoft Exchange Server nicht übermittelt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e5691-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="e5691-112">Dieses Flag in Kombination mit der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode verwendet werden soll, und das Flag ITEMPROC_FORCE, um eine PST-Speichers anzuzeigen, die die Nachricht ist für Regeln für die Verarbeitung vor der Informationsspeicher für Persönliche Ordner-Datei (PST) eine benachrichtigt überwachungs-Client, der die Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="e5691-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="e5691-113">Diese Regeln, die Verarbeitung gilt nur für neue Nachrichten, die erstellt werden mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server, der keinem Exchange-Server in diesem Fall ist der Exchange-Server würde bereits Regeln für die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e5691-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="e5691-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="e5691-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="e5691-115">Änderungen geschrieben werden soll, auf das Objekt, das Überschreiben alle vorherigen Änderungen, die auf das Objekt vorgenommen wurden, und das Objekt geschlossen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="e5691-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="e5691-116">Lese-/Schreibberechtigung für muss für den Vorgang festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e5691-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="e5691-117">Das Flag FORCE_SAVE wird verwendet, nachdem ein vorherigen Aufruf von **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5691-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="e5691-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="e5691-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="e5691-119">Änderungen ein Commit ausgeführt werden soll, und das Objekt zum Lesen geöffnet beibehalten werden sollten.</span><span class="sxs-lookup"><span data-stu-id="e5691-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="e5691-120">Keine zusätzlichen Änderungen werden vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="e5691-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="e5691-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="e5691-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="e5691-122">Änderungen ein Commit ausgeführt werden soll, und das Objekt für die Berechtigung Lese-/Schreibzugriff geöffnet beibehalten werden sollten.</span><span class="sxs-lookup"><span data-stu-id="e5691-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="e5691-123">Dieses Kennzeichen werden in der Regel festgelegt, wenn das Objekt zum ersten Mal Lese-/Schreibzugriff geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e5691-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="e5691-124">Nachfolgende Änderungen am Objekt sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="e5691-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="e5691-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e5691-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e5691-126">Ermöglicht **SaveChanges** erfolgreich, möglicherweise beendet, bevor die Änderungen vollständig übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="e5691-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="e5691-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="e5691-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="e5691-128">Ermöglicht die Spamfilterung für eine Nachricht ein, die gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e5691-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="e5691-129">Unterstützung der Spamfilterung steht nur, wenn der Absender e-Mail-Adresstyp Simple Mail Transfer Protocol (SMTP ist), und die Nachricht einen Speicher für Persönliche Ordner-Datei (PST) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e5691-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5691-130">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e5691-130">Return value</span></span>

<span data-ttu-id="e5691-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5691-131">S_OK</span></span> 
  
> <span data-ttu-id="e5691-132">Das Engagement der Änderungen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e5691-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="e5691-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e5691-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e5691-134">**SaveChanges** kann nicht das Objekt geöffnet lassen für nur-Lese-Berechtigung Wenn KEEP_OPEN_READONLY festgelegt, oder Lese-/Schreibberechtigung für Wenn KEEP_OPEN_READWRITE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e5691-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="e5691-135">Es sind keine Änderungen ein Commit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5691-135">No changes are committed.</span></span> 
    
<span data-ttu-id="e5691-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="e5691-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="e5691-137">Das Objekt wurde geändert seit es geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e5691-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="e5691-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="e5691-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="e5691-139">Das Objekt wurde gelöscht, da es geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e5691-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5691-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5691-140">Remarks</span></span>

<span data-ttu-id="e5691-141">Die **IMAPIProp::SaveChanges** -Methode ändert Eigenschaft permanente für Objekte, die Unterstützung für das Transaktionsmodell verarbeiten, wie Nachrichten, Anlagen, Address Book-Container und messaging User-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e5691-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="e5691-142">Objekte, die keine für Transaktionen im Ordner, Nachrichtenspeicher und Profil Abschnitte Unterstützung, nehmen Sie Änderungen permanente sofort.</span><span class="sxs-lookup"><span data-stu-id="e5691-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="e5691-143">Kein Aufruf von **SaveChanges** ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5691-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="e5691-144">Da Dienstanbieter keine generieren einen Eintrag Bezeichner für Objekte, bis alle Eigenschaften gespeichert wurden, ein Objekt **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft möglicherweise nicht verfügbar erst nach seiner **SaveChanges** -Methode wurde aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e5691-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="e5691-145">Einige Anbieter warten Sie, bis das Flag KEEP_OPEN_READONLY festgelegt ist auf der **SaveChanges** -Anruf.</span><span class="sxs-lookup"><span data-stu-id="e5691-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="e5691-146">KEEP_OPEN_READONLY gibt an, dass die Änderungen in den aktuellen Anruf gespeichert werden die letzten Änderungen eingefügt werden, die auf dem Objekt vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="e5691-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="e5691-147">Einige Nachricht Store Implementierungen führen keine Nachrichten in einem Ordner anzeigen, die neu erstellte bis zu einem Client speichert die Nachricht mithilfe von **SaveChanges** geändert und Nachrichtenobjekte mithilfe der [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode frei.</span><span class="sxs-lookup"><span data-stu-id="e5691-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="e5691-148">Darüber hinaus können nicht einige Implementierungen Objekt eine **PR_ENTRYID** -Eigenschaft für ein neu erstelltes Objekt erst nach dem Erstellen **SaveChanges** aufgerufen wurde, und einige können dies tun, wenn **SaveChanges** mithilfe von KEEP_OPEN_READONLY aufgerufen wurde Legen Sie in _UlFlags_.</span><span class="sxs-lookup"><span data-stu-id="e5691-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e5691-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e5691-149">Notes to implementers</span></span>

<span data-ttu-id="e5691-150">Wenn Sie die Kennzeichen KEEP_OPEN_READONLY erhalten, müssen Sie die Option verlassen das Objekt Zugriff mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e5691-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="e5691-151">Jedoch kann ein Anbieter nie lassen Sie ein Objekt in einem schreibgeschützten Zustand, wenn das Flag KEEP_OPEN_READWRITE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5691-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="e5691-152">Wenn ein Client mehrere Anlagen auf mehrere Nachrichten speichert, ruft es die **SaveChanges** -Methode für jede Anlage und jede Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e5691-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="e5691-153">Häufig Clients werden für jede dieser Anrufe mit Ausnahme der letzten MAPI_DEFERRED_ERRORS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e5691-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="e5691-154">Sie können entweder mit dem letzten Aufruf oder einem früheren Anrufe Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e5691-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="e5691-155">Sie können auch die Kennzeichen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e5691-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="e5691-156">Wenn KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Fehler Aufschiebung Anforderung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e5691-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="e5691-157">Wenn MAPI_DEFERRED_ERRORS in _UlFlags_nicht festgelegt ist, ein zuvor zurückgestellte Fehler zurückgegeben werden für den Anruf **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="e5691-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="e5691-158">Gibt an, ob ein remote-Transport-Anbieter eine funktionsfähige Implementierung dieser Methode bietet ist optional und hängt von anderen Designentscheidungen in Ihrer Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e5691-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="e5691-159">Wenn Sie diese Methode implementieren, führen Sie entsprechend der Dokumentation zur.</span><span class="sxs-lookup"><span data-stu-id="e5691-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="e5691-160">Da Ordnerobjekten und Status Objekte nicht durchgeführt werden, muss mindestens eines remote Transportdienstes Implementierung der **SaveChanges** S_OK zurückgeben ohne tatsächlich keine Arbeit.</span><span class="sxs-lookup"><span data-stu-id="e5691-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e5691-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e5691-161">Notes to callers</span></span>

<span data-ttu-id="e5691-162">Wenn ein Client KEEP_OPEN_READONLY übergibt, die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufgerufen und ruft dann erneut die **SaveChanges** , kann die gleiche Implementierung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e5691-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="e5691-163">Nach Eingang eines Anrufs MAPI_E_NO_ACCESS in dem Sie KEEP_OPEN_READWRITE festgelegt, Sie haben weiterhin Lese-/Schreibberechtigung für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="e5691-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="e5691-164">Sie können auch das Kennzeichen KEEP_OPEN_READONLY oder keine Flags mit KEEP_OPEN_SUFFIX übergeben **SaveChanges** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e5691-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="e5691-165">Ob das Flag KEEP_OPEN_READWRITE von einem Anbieter unterstützt, hängt von der Anbieter-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e5691-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="e5691-166">Legen Sie keine Flags für den Parameter _UlFlags_ aus, um anzugeben, dass nur beim Aufruf von auf das Objekt nach **SaveChanges** vorgenommen werden **IUnknown**wird.</span><span class="sxs-lookup"><span data-stu-id="e5691-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e5691-167">Ein Fehler aus **SaveChanges** gibt an, dass es nicht die ausstehenden Änderungen dauerhaft entfernt wird konnte.</span><span class="sxs-lookup"><span data-stu-id="e5691-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="e5691-168">Verschiedene Anbieter behandeln fehlen Kennzeichen für den Aufruf der **SaveChanges** unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="e5691-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="e5691-169">Einige Anbieter behandelt diesen Zustand als KEEP_OPEN_READONLY. andere Anbieter interpretieren KEEP_OPEN_READWRITE identisch.</span><span class="sxs-lookup"><span data-stu-id="e5691-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="e5691-170">Noch andere Anbieter das Objekt herunter, wenn sie keine Kennzeichen für den Aufruf der **SaveChanges** erhalten.</span><span class="sxs-lookup"><span data-stu-id="e5691-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="e5691-171">Einige Eigenschaften, die in der Regel berechnete Eigenschaften können nicht verarbeitet werden, bis Sie **SaveChanges** aufrufen und in einigen Fällen **Version**.</span><span class="sxs-lookup"><span data-stu-id="e5691-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="e5691-172">Wenn Sie von massenänderungen vornehmen, wie Anlagen auf mehrere Nachrichten gespeichert zurückstellen Sie Fehler bei der Verarbeitung durch das Flag MAPI_DEFERRED_ERRORS in _UlFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e5691-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="e5691-173">Wenn Sie mehrere Anlagen auf mehrere Nachrichten speichern, stellen Sie eine **SaveChanges** Aufruf für jede Anlage und eine **SaveChanges** auf jede Nachricht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e5691-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="e5691-174">Legen Sie das MAPI_DEFERRED_ERRORS-Flag für jeden Anruf Anlage und für alle Nachrichten mit Ausnahme der letzten.</span><span class="sxs-lookup"><span data-stu-id="e5691-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="e5691-175">Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgegeben wird, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e5691-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="e5691-176">In diesem Fall warnen Sie, und Benutzer entweder, dass die Änderungen die vorherigen Änderungen zu überschreiben, oder speichern Sie das Objekt an anderer Stelle angefordert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5691-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="e5691-177">Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer um ihnen die Möglichkeit, speichern Sie das Objekt in einen anderen Speicherort zu verleihen.</span><span class="sxs-lookup"><span data-stu-id="e5691-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="e5691-178">Sie können nicht mit dem FORCE_SAVE-Flag auf ein geöffnetes Objekt **SaveChanges** aufrufen, die gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="e5691-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="e5691-179">Wenn **SaveChanges** einen Fehler zurückgibt, das Objekt, dessen Änderungen wurden zu speichernde bleibt, öffnen, unabhängig von den im Parameter _UlFlags_ festgelegten Flags.</span><span class="sxs-lookup"><span data-stu-id="e5691-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e5691-180">Die _UlFlags_ NON_EMS_XP_SAVE und SPAMFILTER_ONSAVE möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mithilfe der folgenden Werte hinzufügen: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="e5691-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="e5691-181">Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e5691-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5691-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5691-182">See also</span></span>



[<span data-ttu-id="e5691-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e5691-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="e5691-184">Kanonische-Eigenschaft PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="e5691-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="e5691-185">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5691-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="e5691-186">Speichern von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5691-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)


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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316632"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="3efea-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="3efea-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="3efea-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3efea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3efea-105">Macht alle Änderungen, die an einem Objekt seit dem letzten Speichervorgang vorgenommen wurden, dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="3efea-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3efea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3efea-106">Parameters</span></span>

 <span data-ttu-id="3efea-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3efea-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3efea-108">in Eine Bitmaske von Flags, die steuert, was mit dem Objekt geschieht, wenn die **IMAPIProp:: SaveChanges** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3efea-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="3efea-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3efea-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="3efea-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="3efea-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="3efea-111">Gibt an, dass die Nachricht nicht von einem Microsoft Exchange-Server übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="3efea-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="3efea-112">Dieses Flag sollte in Kombination mit der [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode und dem ITEMPROC_FORCE-Flag verwendet werden, um einem PST-Speicher anzuzeigen, dass die Nachricht für die Verarbeitung von Regeln berechtigt ist, bevor der PST-Speicher (Personal Folders) benachrichtigt wird. Überwachen des Clients, dass die Nachricht eingegangen ist.</span><span class="sxs-lookup"><span data-stu-id="3efea-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="3efea-113">Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf einem Server erstellt werden, der kein Exchange-Server ist, in dem der Exchange-Server bereits Regeln für die Nachricht verarbeitet hätte.</span><span class="sxs-lookup"><span data-stu-id="3efea-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="3efea-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="3efea-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="3efea-115">Änderungen sollten in das Objekt geschrieben werden, wobei alle vorherigen Änderungen, die an dem Objekt vorgenommen wurden, überschrieben werden und das Objekt geschlossen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="3efea-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="3efea-116">Die Berechtigung Lese-/Schreibzugriff muss festgelegt werden, damit der Vorgang erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3efea-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="3efea-117">Das FORCE_SAVE-Flag wird verwendet, nachdem ein vorheriger Aufruf von **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3efea-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="3efea-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="3efea-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="3efea-119">Änderungen sollten zugesichert werden, und das Objekt sollte zum Lesen geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="3efea-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="3efea-120">Es werden keine weiteren Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="3efea-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="3efea-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="3efea-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="3efea-122">Änderungen sollten zugesichert werden, und das Objekt sollte für Lese-/Schreibzugriff geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="3efea-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="3efea-123">Dieses Flag wird in der Regel festgelegt, wenn das Objekt zum ersten Mal für Lese-/Schreibzugriff geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="3efea-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="3efea-124">Nachfolgende Änderungen am Objekt sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="3efea-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="3efea-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="3efea-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="3efea-126">Ermöglicht \*\*\*\* , dass SaveChanges erfolgreich zurückgegeben wird, möglicherweise bevor die Änderungen vollständig übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3efea-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="3efea-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="3efea-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="3efea-128">Aktiviert die Spamfilterung für eine Nachricht, die gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3efea-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="3efea-129">Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3efea-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3efea-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3efea-130">Return value</span></span>

<span data-ttu-id="3efea-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="3efea-131">S_OK</span></span> 
  
> <span data-ttu-id="3efea-132">Die Verpflichtung der Änderungen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3efea-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="3efea-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3efea-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="3efea-134">**SaveChanges** kann das Objekt nur mit Leseberechtigung öffnen, wenn KEEP_OPEN_READONLY festgelegt ist, oder Lese-/Schreibzugriff Berechtigung, wenn KEEP_OPEN_READWRITE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3efea-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="3efea-135">Es werden keine Änderungen übernommen.</span><span class="sxs-lookup"><span data-stu-id="3efea-135">No changes are committed.</span></span> 
    
<span data-ttu-id="3efea-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3efea-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="3efea-137">Das Objekt wurde seit dem Öffnen geändert.</span><span class="sxs-lookup"><span data-stu-id="3efea-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="3efea-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="3efea-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="3efea-139">Das Objekt wurde seit dem Öffnen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3efea-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3efea-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3efea-140">Remarks</span></span>

<span data-ttu-id="3efea-141">Die **IMAPIProp:: SaveChanges** -Methode macht Änderungen an Eigenschaften für Objekte dauerhaft, die das Transaktionsmodell der Verarbeitung unterstützen, wie Nachrichten, Anlagen, Adressbuchcontainer und Messaging-Benutzerobjekte.</span><span class="sxs-lookup"><span data-stu-id="3efea-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="3efea-142">Objekte, die keine Transaktionen unterstützen, wie beispielsweise Ordner, Nachrichtenspeicher und Profilabschnitte, nehmen Änderungen permanent vor.</span><span class="sxs-lookup"><span data-stu-id="3efea-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="3efea-143">Es ist kein \*\*\*\* Aufruf von SaveChanges erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3efea-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="3efea-144">Da Dienstanbieter keine Eintrags-ID für Ihre Objekte generieren müssen, bis alle Eigenschaften gespeichert wurden, ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft eines Objekts möglicherweise erst nach der **SaveChanges** -Methode verfügbar. aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3efea-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="3efea-145">Einige Anbieter warten, bis das KEEP_OPEN_READONLY-Flag für den **SaveChanges** -Aufruf festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3efea-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="3efea-146">KEEP_OPEN_READONLY gibt an, dass die Änderungen, die im aktuellen Aufruf gespeichert werden sollen, die letzten Änderungen sind, die für das Objekt vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="3efea-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="3efea-147">In einigen Nachrichtenspeicher Implementierungen werden nicht neu erstellte Nachrichten in einem Ordner angezeigt, bis ein Client die Nachrichten \*\*\*\* Änderungen mithilfe von SaveChanges speichert und die Message-Objekte mithilfe der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode freigibt.</span><span class="sxs-lookup"><span data-stu-id="3efea-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="3efea-148">Darüber hinaus können einige Objekt Implementierungen eine **PR_ENTRYID** -Eigenschaft für ein neu erstelltes Objekt erst generieren, nachdem **SaveChanges** aufgerufen wurde, und einige können dies nur tun, nachdem **SaveChanges** mithilfe von KEEP_OPEN_READONLY aufgerufen wurde. festgelegt in _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="3efea-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3efea-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="3efea-149">Notes to implementers</span></span>

<span data-ttu-id="3efea-150">Wenn Sie das KEEP_OPEN_READONLY-Flag erhalten, haben Sie die Möglichkeit, den Zugriff des Objekts als Lese-/Schreibzugriff zu lassen.</span><span class="sxs-lookup"><span data-stu-id="3efea-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="3efea-151">Ein Anbieter kann jedoch nie ein Objekt in einem schreibgeschützten Zustand lassen, wenn das KEEP_OPEN_READWRITE-Flag übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3efea-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="3efea-152">Wenn ein Client mehrere Anlagen in mehreren Nachrichten speichert, ruft er \*\*\*\* die SaveChanges-Methode für jede Anlage und jede Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="3efea-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="3efea-153">Häufig werden Clients MAPI_DEFERRED_ERRORS für jeden dieser Anrufe festlegen, mit Ausnahme des letzten.</span><span class="sxs-lookup"><span data-stu-id="3efea-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="3efea-154">Sie können entweder mit dem letzten Anruf oder früheren anrufen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3efea-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="3efea-155">Sie können die Kennzeichnung sogar ignorieren.</span><span class="sxs-lookup"><span data-stu-id="3efea-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="3efea-156">Wenn KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Anforderung zur Fehler begärung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="3efea-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="3efea-157">Wenn MAPI_DEFERRED_ERRORS nicht in _ulFlags_festgelegt ist, kann einer der zuvor verzögerten Fehler für den SaveChanges \*\*\*\* -Aufruf zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3efea-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="3efea-158">Ob ein Remote Transportanbieter eine funktionale Implementierung dieser Methode bereitstellt, ist optional und hängt von anderen Entwurfsentscheidungen in ihrer Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="3efea-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="3efea-159">Wenn Sie diese Methode implementieren, tun Sie dies gemäß der Dokumentation hier.</span><span class="sxs-lookup"><span data-stu-id="3efea-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="3efea-160">Da Ordnerobjekte und Statusobjekte nicht transformiert werden, muss mindestens die Implementierung von SaveChanges durch einen \*\*\*\* Remote Transportanbieter S_OK zurückgeben, ohne dass tatsächlich eine Arbeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3efea-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3efea-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3efea-161">Notes to callers</span></span>

<span data-ttu-id="3efea-162">Wenn ein Client KEEP_OPEN_READONLY übergibt, die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode aufruft und \*\*\*\* dann SaveChanges erneut aufruft, kann für dieselbe Implementierung ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="3efea-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="3efea-163">Nachdem Sie MAPI_E_NO_ACCESS von einem Aufruf empfangen haben, in dem Sie KEEP_OPEN_READWRITE festgelegt haben, verfügen Sie weiterhin über Lese-/Schreibzugriff für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="3efea-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="3efea-164">Sie können **SaveChanges** erneut aufrufen, indem Sie entweder das KEEP_OPEN_READONLY-Flag oder keine Flags mit KEEP_OPEN_SUFFIX übergeben.</span><span class="sxs-lookup"><span data-stu-id="3efea-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="3efea-165">Ob ein Anbieter das KEEP_OPEN_READWRITE-Flag unterstützt, hängt von der Implementierung des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="3efea-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="3efea-166">Um anzugeben, dass der einzige Aufruf für das Objekt nach SaveChanges \*\*\*\* ist **IUnknown:: Release**, legen Sie keine Flags für den _ulFlags_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="3efea-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="3efea-167">Ein Fehler von **SaveChanges** gibt an, dass die ausstehenden Änderungen nicht dauerhaft vorgenommen werden konnten.</span><span class="sxs-lookup"><span data-stu-id="3efea-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="3efea-168">Unterschiedliche Anbieter behandeln das Fehlen von Flags für \*\*\*\* den SaveChanges-Aufruf anders.</span><span class="sxs-lookup"><span data-stu-id="3efea-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="3efea-169">Einige Anbieter behandeln diesen Status genauso wie KEEP_OPEN_READONLY; andere Anbieter interpretieren es genauso wie KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="3efea-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="3efea-170">Andere Anbieter haben das Objekt jedoch heruntergefahren, wenn Sie keine Flags für den **SaveChanges** -Aufruf erhalten.</span><span class="sxs-lookup"><span data-stu-id="3efea-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="3efea-171">Einige Eigenschaften, in der Regel berechnete Eigenschaften, können erst verarbeitet \*\*\*\* werden, wenn Sie SaveChanges aufrufen und in einigen Fällen **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="3efea-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="3efea-172">Wenn Sie Massenänderungen vornehmen, wie das Speichern von Anlagen in mehreren Nachrichten, verschieben Sie die Fehlerverarbeitung, indem Sie das MAPI_DEFERRED_ERRORS-Flag in _ulFlags_festlegen.</span><span class="sxs-lookup"><span data-stu-id="3efea-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="3efea-173">Wenn Sie mehrere Anlagen in mehreren Nachrichten speichern, führen \*\*\*\* Sie einen SaveChanges-Aufruf jeder Anlage und einen **SaveChanges** -Aufruf jeder Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="3efea-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="3efea-174">Legen Sie das MAPI_DEFERRED_ERRORS-Flag für jeden Anlagen Aufruf und für alle Nachrichten mit Ausnahme des letzten fest.</span><span class="sxs-lookup"><span data-stu-id="3efea-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="3efea-175">Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED zurückgibt, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3efea-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="3efea-176">Wenn dies der Fall ist, warnen Sie den Benutzer, der entweder die Änderung der Änderungen überschreiben oder das Objekt an einer anderen Stelle speichern kann.</span><span class="sxs-lookup"><span data-stu-id="3efea-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="3efea-177">Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer, Ihnen die Möglichkeit zu geben, das Objekt an einem anderen Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3efea-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="3efea-178">Sie können **SaveChanges** nicht mit dem FORCE_SAVE-Flag für ein geöffnetes Objekt aufrufen, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3efea-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="3efea-179">Wenn **SaveChanges** einen Fehler zurückgibt, bleibt das Objekt, dessen Änderungen gespeichert werden sollen, unabhängig von den im _ulFlags_ -Parameter festgelegten Flags geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3efea-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3efea-180">Die _ulFlags_ NON_EMS_XP_SAVE und SPAMFILTER_ONSAVE sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie Sie mit den folgenden Werten zu Ihrem Code hinzufügen: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="3efea-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="3efea-181">Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3efea-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3efea-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3efea-182">See also</span></span>



[<span data-ttu-id="3efea-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="3efea-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="3efea-184">Kanonische PidTagEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3efea-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="3efea-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3efea-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="3efea-186">Speichern von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3efea-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)


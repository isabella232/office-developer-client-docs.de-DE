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
# <a name="imapipropsavechanges"></a><span data-ttu-id="e1110-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e1110-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="e1110-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1110-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1110-105">Nimmt dauerhafte Änderungen vor, die seit dem letzten Speichervorgang an einem Objekt vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e1110-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e1110-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1110-106">Parameters</span></span>

 <span data-ttu-id="e1110-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1110-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e1110-108">[in] Eine Bitmaske mit Flags, die steuert, was mit dem Objekt geschieht, wenn die **IMAPIProp::SaveChanges-Methode** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e1110-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="e1110-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e1110-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="e1110-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="e1110-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="e1110-111">Gibt an, dass die Nachricht nicht von einem Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1110-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="e1110-112">Dieses Flag sollte in Kombination mit der [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) und dem ITEMPROC_FORCE-Flag verwendet werden, um einem PST-Speicher anzuzeigen, dass die Nachricht für die Regelverarbeitung berechtigt ist, bevor der Speicher für persönliche Ordner (Personal Folders File, PST) jeden Abhörclient benachrichtigt, dass die Nachricht eingetroffen ist.</span><span class="sxs-lookup"><span data-stu-id="e1110-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="e1110-113">Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server erstellt werden, der kein Exchange Server ist. In diesem Fall hätte die Exchange Server bereits Regeln für die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e1110-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="e1110-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="e1110-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="e1110-115">Änderungen sollten in das Objekt geschrieben werden, wobei alle vorherigen Änderungen überschrieben werden, die am Objekt vorgenommen wurden, und das Objekt sollte geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e1110-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="e1110-116">Die Lese-/Schreibberechtigung muss festgelegt sein, damit der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e1110-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="e1110-117">Das FORCE_SAVE wird nach einem vorherigen Aufruf von **SaveChanges** verwendet, der MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="e1110-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="e1110-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="e1110-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="e1110-119">Änderungen sollten mit einem "Committed" und dem Objekt zum Lesen geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="e1110-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="e1110-120">Es werden keine weiteren Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="e1110-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="e1110-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="e1110-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="e1110-122">Änderungen sollten für Lese-/Schreibzugriff geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="e1110-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="e1110-123">Dieses Flag wird in der Regel festgelegt, wenn das Objekt zum ersten Mal für Lese-/Schreibberechtigungen geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e1110-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="e1110-124">Nachfolgende Änderungen am Objekt sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="e1110-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="e1110-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e1110-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e1110-126">Ermöglicht **es SaveChanges,** erfolgreich zurückzukehren, möglicherweise bevor die Änderungen vollständig vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e1110-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="e1110-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="e1110-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="e1110-128">Aktiviert die Spamfilterung für eine Nachricht, die gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e1110-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="e1110-129">Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e1110-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1110-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1110-130">Return value</span></span>

<span data-ttu-id="e1110-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1110-131">S_OK</span></span> 
  
> <span data-ttu-id="e1110-132">Die Verpflichtung der Änderungen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e1110-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="e1110-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e1110-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e1110-134">**SaveChanges kann** das Objekt nicht für schreibgeschützte Berechtigungen öffnen, wenn KEEP_OPEN_READONLY festgelegt ist, oder Lese-/Schreibberechtigungen, KEEP_OPEN_READWRITE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e1110-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="e1110-135">Es werden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="e1110-135">No changes are committed.</span></span> 
    
<span data-ttu-id="e1110-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="e1110-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="e1110-137">Das Objekt hat sich seit dem Öffnen geändert.</span><span class="sxs-lookup"><span data-stu-id="e1110-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="e1110-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="e1110-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="e1110-139">Das Objekt wurde seit dem Öffnen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e1110-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1110-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1110-140">Remarks</span></span>

<span data-ttu-id="e1110-141">Die **IMAPIProp::SaveChanges-Methode macht Eigenschaftsänderungen** für Objekte dauerhaft, die das Transaktionsmodell der Verarbeitung unterstützen, z. B. Nachrichten, Anlagen, Adressbuchcontainer und Messagingbenutzerobjekte.</span><span class="sxs-lookup"><span data-stu-id="e1110-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="e1110-142">Objekte, die Keine Transaktionen unterstützen, z. B. Ordner, Nachrichtenspeicher und Profilabschnitte, nehmen Änderungen sofort dauerhaft vor.</span><span class="sxs-lookup"><span data-stu-id="e1110-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="e1110-143">Es ist kein **Aufruf von SaveChanges** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e1110-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="e1110-144">Da Dienstanbieter erst nach dem Speichern aller Eigenschaften eine Eintrags-ID für ihre Objekte generieren müssen, ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft eines Objekts möglicherweise erst verfügbar, nachdem die **SaveChanges-Methode** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e1110-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="e1110-145">Einige Anbieter warten, bis das KEEP_OPEN_READONLY für den **SaveChanges-Aufruf festgelegt** ist.</span><span class="sxs-lookup"><span data-stu-id="e1110-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="e1110-146">KEEP_OPEN_READONLY gibt an, dass die änderungen, die im aktuellen Aufruf gespeichert werden sollen, die letzten Änderungen sind, die am Objekt vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="e1110-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="e1110-147">Einige Nachrichtenspeicherimplementierungen zeigen neu erstellte Nachrichten erst in einem Ordner an, wenn ein Client die Nachrichtenänderungen mithilfe von **SaveChanges** speichert und die Nachrichtenobjekte mithilfe der [IUnknown::Release-Methode freilässt.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1110-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="e1110-148">Darüber hinaus können einige Objektimplementierungen erst nach dem Aufruf von **SaveChanges** eine **PR_ENTRYID-Eigenschaft** für ein neu erstelltes Objekt generieren, und einige können dies erst tun, nachdem **SaveChanges** mithilfe von KEEP_OPEN_READONLY in _ulFlags_ aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e1110-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e1110-149">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e1110-149">Notes to implementers</span></span>

<span data-ttu-id="e1110-150">Wenn Sie das KEEP_OPEN_READONLY erhalten, haben Sie die Möglichkeit, den Zugriff des Objekts als Lese-/Schreibzugriff zu lassen.</span><span class="sxs-lookup"><span data-stu-id="e1110-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="e1110-151">Ein Anbieter kann ein Objekt jedoch niemals in einem schreibgeschützten Zustand be lassen, wenn KEEP_OPEN_READWRITE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1110-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="e1110-152">Wenn ein Client mehrere Anlagen in mehreren Nachrichten speichert, ruft er die **SaveChanges-Methode** für jede Anlage und jede Nachricht auf.</span><span class="sxs-lookup"><span data-stu-id="e1110-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="e1110-153">Häufig legen Clients MAPI_DEFERRED_ERRORS für jeden dieser Anrufe außer für den letzten Anruf ein.</span><span class="sxs-lookup"><span data-stu-id="e1110-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="e1110-154">Sie können Fehler entweder mit dem letzten Anruf oder mit früheren Aufrufen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e1110-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="e1110-155">Sie können sogar das Flag ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e1110-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="e1110-156">Wenn eine KEEP_OPEN_READWRITE oder KEEP_OPEN_READONLY zusammen mit MAPI_DEFERRED_ERRORS festgelegt ist, können Sie die Anforderung zur Fehlererhebung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e1110-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="e1110-157">Wenn MAPI_DEFERRED_ERRORS in  _ulFlags_ nicht festgelegt ist, kann einer der zuvor verzögerten Fehler für den **SaveChanges-Aufruf zurückgegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="e1110-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="e1110-158">Ob ein Remotetransportanbieter eine funktionale Implementierung dieser Methode bietet, ist optional und hängt von anderen Entwurfsentscheidungen in Ihrer Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="e1110-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="e1110-159">Wenn Sie diese Methode implementieren, tun Sie dies gemäß der hier gezeigten Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e1110-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="e1110-160">Da Ordnerobjekte und Statusobjekte nicht transaktiviert werden, muss die Implementierung von **SaveChanges** durch einen Remotetransportanbieter mindestens S_OK zurückgeben, ohne dass tatsächlich eine Arbeit vor sich geht.</span><span class="sxs-lookup"><span data-stu-id="e1110-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e1110-161">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e1110-161">Notes to callers</span></span>

<span data-ttu-id="e1110-162">Wenn ein Client KEEP_OPEN_READONLY, die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) aufruft und **dann SaveChanges** erneut aufruft, kann dieselbe Implementierung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e1110-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="e1110-163">Nachdem Sie MAPI_E_NO_ACCESS von einem Anruf empfangen haben, in dem Sie KEEP_OPEN_READWRITE festgelegt haben, verfügen Sie weiterhin über Lese-/Schreibberechtigung für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1110-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="e1110-164">Sie können **SaveChanges erneut** aufrufen, indem Sie entweder das KEEP_OPEN_READONLY oder keine Flags mit KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="e1110-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="e1110-165">Ob ein Anbieter das KEEP_OPEN_READWRITE unterstützt, hängt von der Implementierung des Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="e1110-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="e1110-166">Legen Sie keine Flags für den _ulFlags-Parameter_ fest, um anzugeben, dass der einzige Aufruf für das Objekt nach **SaveChanges** **IUnknown::Release** ist.</span><span class="sxs-lookup"><span data-stu-id="e1110-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e1110-167">Ein Fehler von **SaveChanges** gibt an, dass die ausstehenden Änderungen nicht dauerhaft vorgenommen werden konnten.</span><span class="sxs-lookup"><span data-stu-id="e1110-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="e1110-168">Unterschiedliche Anbieter behandeln das Fehlen von Kennzeichen für **den SaveChanges-Aufruf** unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="e1110-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="e1110-169">Einige Anbieter behandeln diesen Zustand wie KEEP_OPEN_READONLY; andere Anbieter interpretieren sie genauso wie KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="e1110-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="e1110-170">Andere Anbieter fahren das Objekt jedoch herunter, wenn sie keine Flags für den **SaveChanges-Aufruf** erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1110-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="e1110-171">Einige Eigenschaften, in der Regel berechnete Eigenschaften, können erst verarbeitet werden, wenn **Sie SaveChanges und** in einigen Fällen **Release aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="e1110-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="e1110-172">Wenn Sie Massenänderungen vornehmen, z. B. Anlagen in mehreren Nachrichten speichern, können Sie die Fehlerverarbeitung zurückschieben, indem Sie MAPI_DEFERRED_ERRORS in _ulFlags festlegen._</span><span class="sxs-lookup"><span data-stu-id="e1110-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="e1110-173">Wenn Sie mehrere Anlagen in mehreren Nachrichten speichern, nehmen Sie einen **SaveChanges-Aufruf** für jede Anlage und einen **SaveChanges-Aufruf** für jede Nachricht vor.</span><span class="sxs-lookup"><span data-stu-id="e1110-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="e1110-174">Legen Sie das MAPI_DEFERRED_ERRORS für jeden Anlagenaufruf und für alle Nachrichten außer dem letzten ein.</span><span class="sxs-lookup"><span data-stu-id="e1110-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="e1110-175">Wenn **SaveChanges** MAPI_E_OBJECT_CHANGED, überprüfen Sie, ob das ursprüngliche Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e1110-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="e1110-176">Wenn ja, warnen Sie den Benutzer, der entweder anfordern kann, dass die Änderungen die vorherigen Änderungen überschreiben oder das Objekt an anderer Stelle speichern.</span><span class="sxs-lookup"><span data-stu-id="e1110-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="e1110-177">Wenn das ursprüngliche Objekt gelöscht wurde, warnen Sie den Benutzer, ihm die Möglichkeit zu geben, das Objekt an einem anderen Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e1110-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="e1110-178">**SaveChanges kann nicht mit** dem FORCE_SAVE für ein gelöschtes geöffnetes Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e1110-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="e1110-179">Wenn **SaveChanges** einen Fehler zurückgibt, bleibt das Objekt, dessen Änderungen gespeichert werden sollten, geöffnet, unabhängig von den im _ulFlags-Parameter festgelegten Flags._</span><span class="sxs-lookup"><span data-stu-id="e1110-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e1110-180">Die  _ulFlags-NON_EMS_XP_SAVE_ und SPAMFILTER_ONSAVE sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe der folgenden Werte hinzufügen: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="e1110-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="e1110-181">Weitere Informationen finden Sie unter [Speichern von MAPI-Eigenschaften](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e1110-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1110-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1110-182">See also</span></span>



[<span data-ttu-id="e1110-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e1110-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="e1110-184">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e1110-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="e1110-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1110-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="e1110-186">Speichern von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1110-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)


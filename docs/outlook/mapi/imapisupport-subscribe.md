---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419926"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="98780-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="98780-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="98780-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98780-105">Registriert eine Ratensenke, um Benachrichtigungen über MAPI zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98780-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="98780-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98780-106">Parameters</span></span>

 <span data-ttu-id="98780-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="98780-107">_lpKey_</span></span>
  
> <span data-ttu-id="98780-108">[in] Ein Zeiger auf einen Benachrichtigungsschlüssel, der das advise-Quellobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="98780-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="98780-109">Der  _lpKey-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="98780-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="98780-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="98780-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="98780-111">[in] Eine Maske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, die der Anrufer interessiert und in die Registrierung einbezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="98780-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="98780-112">Die folgenden Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="98780-112">The following values are valid:</span></span>
    
 <span data-ttu-id="98780-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="98780-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="98780-114">Registriert für Benachrichtigungen über schwerwiegende Fehler, z. B. unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="98780-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="98780-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="98780-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="98780-116">Registriert für Benachrichtigungen über Ereignisse, die für den jeweiligen Adressbuch- oder Nachrichtenspeicheranbieter spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="98780-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="98780-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="98780-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="98780-118">Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="98780-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="98780-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="98780-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="98780-120">Registriert für Benachrichtigungen über die Erstellung eines neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="98780-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="98780-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="98780-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="98780-122">Registriert für Benachrichtigungen über ein objekt, das kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="98780-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="98780-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="98780-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="98780-124">Registriert für Benachrichtigungen über ein zu löschendes Objekt.</span><span class="sxs-lookup"><span data-stu-id="98780-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="98780-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="98780-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="98780-126">Registriert für Benachrichtigungen über ein zu änderndes Objekt.</span><span class="sxs-lookup"><span data-stu-id="98780-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="98780-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="98780-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="98780-128">Registriert für Benachrichtigungen über ein verschobenes Objekt.</span><span class="sxs-lookup"><span data-stu-id="98780-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="98780-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="98780-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="98780-130">Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="98780-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="98780-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98780-131">_ulFlags_</span></span>
  
> <span data-ttu-id="98780-132">[in] Eine Bitmaske mit Flags, die steuert, wie die Benachrichtigung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="98780-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="98780-133">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="98780-133">The following flag can be set:</span></span>
    
<span data-ttu-id="98780-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="98780-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="98780-135">Wenn der Aufrufer die [IMAPISupport::Notify-Methode](imapisupport-notify.md) aufruft, um Benachrichtigungen für diese Absenke zu generieren, sollte **Notify** alle erforderlichen Aufrufe zur Beratung von Senken vor der Rückgabe machen.</span><span class="sxs-lookup"><span data-stu-id="98780-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="98780-136">Wenn dieses Flag nicht festgelegt ist, ist die Benachrichtigung asynchron, und Rückrufe werden in die Warteschlange der Prozesse eingereiht, die abonniert und gestartet wurden, wenn diese Prozesse die Kontrolle über die CPU erlangen.</span><span class="sxs-lookup"><span data-stu-id="98780-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="98780-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="98780-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="98780-138">[in] Ein Zeiger auf ein Advise Sink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="98780-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="98780-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="98780-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="98780-140">[out] Ein Zeiger auf eine Verbindungsnummer ungleich Null, die die Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="98780-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98780-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98780-141">Return value</span></span>

<span data-ttu-id="98780-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="98780-142">S_OK</span></span> 
  
> <span data-ttu-id="98780-143">Die Benachrichtigungsregistrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="98780-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98780-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98780-144">Remarks</span></span>

<span data-ttu-id="98780-145">Die **IMAPISupport::Subscribe-Methode** ist für alle Dienstanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="98780-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="98780-146">Dienstanbieter rufen **Subscribe über** eine ihrer **Advise-Methoden** auf, damit MAPI die Benachrichtigungen verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="98780-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98780-147">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="98780-147">Notes to callers</span></span>

<span data-ttu-id="98780-148">Um die MAPI-Supportmethoden für die Benachrichtigung zu verwenden, erstellen Sie einen Schlüssel für die Quelle des Hinweises, über den Benachrichtigungen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98780-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="98780-149">Der Wert des Schlüssels muss eindeutig sein und sollte bei jeder Änderung des Objekts problemlos neu generiert werden.</span><span class="sxs-lookup"><span data-stu-id="98780-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="98780-150">MAPI verwendet den Benachrichtigungsschlüssel, um nach Rückruffunktionen zu suchen, die über die [HrAllocAdviseSink-Funktion](hrallocadvisesink.md) für die entsprechende Advise-Quelle registriert sind.</span><span class="sxs-lookup"><span data-stu-id="98780-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="98780-151">Übergeben Sie diesen Schlüssel **an IMAPISupport::Notify,** wenn Sie eine Benachrichtigung für die entsprechende Ratenquelle generieren müssen.</span><span class="sxs-lookup"><span data-stu-id="98780-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="98780-152">Das NOTIFY_SYNC wirkt sich auf den Betrieb nachfolgender Aufrufe von **Notify aus.**</span><span class="sxs-lookup"><span data-stu-id="98780-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="98780-153">Wenn Sie NOTIFY_SYNC, wird **Notify** erst dann angezeigt, wenn alle erforderlichen Benachrichtigungen gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="98780-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="98780-154">Wenn Sie keine NOTIFY_SYNC, wird **Notify** asynchron betrieben und möglicherweise vor dem Senden aller Benachrichtigungen zurückgeschickt.</span><span class="sxs-lookup"><span data-stu-id="98780-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98780-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98780-155">See also</span></span>



[<span data-ttu-id="98780-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="98780-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="98780-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="98780-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="98780-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="98780-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="98780-159">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="98780-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="98780-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="98780-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="98780-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="98780-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


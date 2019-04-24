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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328962"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="c0a9c-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="c0a9c-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="c0a9c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0a9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0a9c-105">Registriert eine Advise-Senke, um Benachrichtigungen über MAPI zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c0a9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0a9c-106">Parameters</span></span>

 <span data-ttu-id="c0a9c-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-107">_lpKey_</span></span>
  
> <span data-ttu-id="c0a9c-108">in Ein Zeiger auf einen Benachrichtigungs Schlüssel, der das Advise-Quellobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="c0a9c-109">Der _lpKey_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="c0a9c-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="c0a9c-111">in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist, und die in die Registrierung aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="c0a9c-112">Die folgenden Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c0a9c-112">The following values are valid:</span></span>
    
 <span data-ttu-id="c0a9c-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="c0a9c-114">Registriert Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise unzureichenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="c0a9c-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="c0a9c-116">Registriert Benachrichtigungen zu Ereignissen, die spezifisch für das jeweilige Adressbuch oder den Nachrichtenspeicher Anbieter sind.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="c0a9c-117">_Uleventmaskfnevnewmail_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="c0a9c-118">Registriert Benachrichtigungen über das Eintreffen neuer Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="c0a9c-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="c0a9c-120">Registriert Benachrichtigungen über die Erstellung eines neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="c0a9c-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="c0a9c-122">Registriert Benachrichtigungen zu einem kopierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="c0a9c-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="c0a9c-124">Registriert Benachrichtigungen zu einem Objekt, das gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="c0a9c-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="c0a9c-126">Registriert Benachrichtigungen zu einem Objekt, das geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="c0a9c-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="c0a9c-128">Registriert Benachrichtigungen zu einem Objekt, das verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="c0a9c-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="c0a9c-130">Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="c0a9c-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-131">_ulFlags_</span></span>
  
> <span data-ttu-id="c0a9c-132">in Eine Bitmaske von Flags, die die Art der Benachrichtigung steuert.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="c0a9c-133">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c0a9c-133">The following flag can be set:</span></span>
    
<span data-ttu-id="c0a9c-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="c0a9c-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="c0a9c-135">Wenn der Anrufer die [IMAPISupport:: notify](imapisupport-notify.md) -Methode zum Generieren von Benachrichtigungen für diese Advise-Senke aufruft, sollte notify alle erforderlichen Aufrufe für Advise-Empfänger durchführen, bevor **Sie** zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="c0a9c-136">Wenn dieses Flag nicht festgelegt ist, ist die Benachrichtigung asynchron, und die Rückrufe werden in die Warteschlange aufgenommen, wenn diese Prozesse die Steuerung der CPU erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="c0a9c-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="c0a9c-138">in Ein Zeiger auf ein Advise-Senke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="c0a9c-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="c0a9c-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="c0a9c-140">Out Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0a9c-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0a9c-141">Return value</span></span>

<span data-ttu-id="c0a9c-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0a9c-142">S_OK</span></span> 
  
> <span data-ttu-id="c0a9c-143">Die Benachrichtigungs Registrierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0a9c-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0a9c-144">Remarks</span></span>

<span data-ttu-id="c0a9c-145">Die **IMAPISupport:: subscribe** -Methode wird für alle Support Objekte des Dienstanbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="c0a9c-146">Dienstanbieter rufen **subscribe** aus einer Ihrer **Advise** -Methoden auf, damit MAPI die Benachrichtigungen verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0a9c-147">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c0a9c-147">Notes to callers</span></span>

<span data-ttu-id="c0a9c-148">Um die MAPI-Supportmethoden für die Benachrichtigung zu verwenden, erstellen Sie einen Schlüssel für die Advise-Quelle das Objekt, über das Benachrichtigungen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="c0a9c-149">Der Wert des Schlüssels muss eindeutig sein und bei jeder Änderung des Objekts leicht neu generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="c0a9c-150">MAPI verwendet den Benachrichtigungs Schlüssel, um nach beliebigen Rückruffunktionen zu suchen, die über die [HrAllocAdviseSink](hrallocadvisesink.md) -Funktion für die entsprechende Advise-Quelle registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="c0a9c-151">Geben Sie diesen Schlüssel an **IMAPISupport:: notify** , wenn Sie eine Benachrichtigung für die entsprechende Advise-Quelle generieren müssen.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="c0a9c-152">Das NOTIFY_SYNC-Flag wirkt sich auf den Vorgang der nachfolgenden Aufrufe von **Notify**aus.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="c0a9c-153">Wenn Sie NOTIFY_SYNC festlegen, wird **Notify** erst zurückgegeben, wenn alle erforderlichen Benachrichtigungen gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="c0a9c-154">Wenn Sie NOTIFY_SYNC nicht festlegen, wird **Notify** asynchron ausgeführt, und möglicherweise wird zurückgegeben, bevor alle Benachrichtigungen gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c0a9c-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0a9c-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0a9c-155">See also</span></span>



[<span data-ttu-id="c0a9c-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c0a9c-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="c0a9c-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c0a9c-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c0a9c-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="c0a9c-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="c0a9c-159">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c0a9c-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c0a9c-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="c0a9c-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="c0a9c-161">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0a9c-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


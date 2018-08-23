---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d427adde72c24d4ca879c7bd883af09c4ecad53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579970"
---
# <a name="notification"></a><span data-ttu-id="4a82d-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-103">NOTIFICATION</span></span>
 
<span data-ttu-id="4a82d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a82d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a82d-105">Enthält Informationen über ein Ereignis, das aufgetreten ist und die Daten, die das Ereignis betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="4a82d-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a82d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4a82d-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a82d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a82d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="4a82d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4a82d-108">Members</span></span>

<span data-ttu-id="4a82d-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="4a82d-109">**ulEventType**</span></span>
  
> <span data-ttu-id="4a82d-110">Typ der Benachrichtigungsereignis, das aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4a82d-110">Type of notification event that occurred.</span></span> <span data-ttu-id="4a82d-111">Der Wert des Elements **UlEventType** entspricht der Struktur, die in der Union **Info** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4a82d-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="4a82d-112">Das Element **UlEventType** kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4a82d-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="4a82d-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="4a82d-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="4a82d-114">Ein globaler Fehler ist aufgetreten, wie eine Sitzung Herunterfahren ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a82d-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="4a82d-115">Das **Info** -Element enthält eine [ERROR_NOTIFICATION](error_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4a82d-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="4a82d-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="4a82d-117">Ein internes Ereignis von einem bestimmten Dienstanbieter definierten ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4a82d-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="4a82d-118">Das **Info** -Element enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4a82d-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="4a82d-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="4a82d-120">Eine Nachricht übermittelt wurde, um den entsprechenden Ordner für die Nachrichtenklasse empfangen und wartet auf Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="4a82d-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="4a82d-121">Das **Info** -Element enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4a82d-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="4a82d-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="4a82d-123">Ein MAPI-Objekt wurde kopiert.</span><span class="sxs-lookup"><span data-stu-id="4a82d-123">A MAPI object has been copied.</span></span> <span data-ttu-id="4a82d-124">Das **Info** -Element enthält eine [OBJECT_NOTIFICATION](object_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4a82d-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="4a82d-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="4a82d-126">Ein MAPI-Objekt wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a82d-126">A MAPI object has been created.</span></span> <span data-ttu-id="4a82d-127">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4a82d-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="4a82d-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="4a82d-129">Ein MAPI-Objekt wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4a82d-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="4a82d-130">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4a82d-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="4a82d-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="4a82d-132">Ein MAPI-Objekt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a82d-132">A MAPI object has changed.</span></span> <span data-ttu-id="4a82d-133">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4a82d-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="4a82d-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="4a82d-135">Einen Nachrichtenspeicher oder Adresse Adressbuch-Objekt verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="4a82d-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="4a82d-136">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4a82d-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="4a82d-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="4a82d-138">Suchvorgang beendet wurde, und die Ergebnisse verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4a82d-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="4a82d-139">Das **Info** -Element enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4a82d-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="4a82d-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="4a82d-141">Die Informationen in einer Tabelle wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="4a82d-141">Information in a table has changed.</span></span> <span data-ttu-id="4a82d-142">Das **Info** -Element enthält eine [TABLE_NOTIFICATION](table_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a82d-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="4a82d-143">**Info**</span><span class="sxs-lookup"><span data-stu-id="4a82d-143">**info**</span></span>
  
> <span data-ttu-id="4a82d-144">Union der Benachrichtigung Strukturen zur Beschreibung der betreffenden Daten für einen bestimmten Typ des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="4a82d-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="4a82d-145">Die Struktur im **Info** -Member enthalten, hängt von den Wert des Elements **UlEventType** ab.</span><span class="sxs-lookup"><span data-stu-id="4a82d-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4a82d-146">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4a82d-146">Remarks</span></span>

<span data-ttu-id="4a82d-147">Ein oder mehrere **Benachrichtigung** Strukturen werden als Eingabeparameter mit jedem Aufruf einer registrierten Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="4a82d-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="4a82d-148">Die **Benachrichtigung** Strukturen enthalten Informationen zu den bestimmte Ereignisse, die aufgetreten sind, und der betroffene Objekte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4a82d-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="4a82d-149">Bevor Clients oder -Dienstanbieter erhalten eine Benachrichtigung die Struktur verwenden können Verarbeitung des Ereignisses, müssen sie den Ereignistyp überprüfen, wie im **UlEventType** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="4a82d-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="4a82d-150">Beispielsweise druckt das Codebeispiel, das hier gezeigte überprüft, ob das Eintreffen einer neuen Nachricht und beim Erkennen eines Ereignisses dieser Art, die Nachrichtenklasse der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4a82d-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="4a82d-151">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a82d-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="4a82d-152">**Thema**</span><span class="sxs-lookup"><span data-stu-id="4a82d-152">**Topic**</span></span>|<span data-ttu-id="4a82d-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a82d-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a82d-154">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="4a82d-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="4a82d-155">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="4a82d-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="4a82d-156">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="4a82d-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="4a82d-157">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a82d-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="4a82d-158">Unterstützen von Ereignisbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="4a82d-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="4a82d-159">Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="4a82d-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a82d-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a82d-160">See also</span></span>


- [<span data-ttu-id="4a82d-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="4a82d-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="4a82d-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="4a82d-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="4a82d-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="4a82d-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4a82d-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="4a82d-167">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4a82d-167">MAPI Structures</span></span>](mapi-structures.md)


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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280099"
---
# <a name="notification"></a><span data-ttu-id="4fbd4-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-103">NOTIFICATION</span></span>
 
<span data-ttu-id="4fbd4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fbd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fbd4-105">Enthält Informationen zu einem aufgetretenen Ereignis und den Daten, die vom Ereignis betroffen waren.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fbd4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4fbd4-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fbd4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4fbd4-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="4fbd4-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4fbd4-108">Members</span></span>

<span data-ttu-id="4fbd4-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-109">**ulEventType**</span></span>
  
> <span data-ttu-id="4fbd4-110">Typ des aufgetretenen Benachrichtigungsereignisses.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-110">Type of notification event that occurred.</span></span> <span data-ttu-id="4fbd4-111">Der Wert des **ulEventType** -Elements entspricht der Struktur, die in der **Info** -Union enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="4fbd4-112">Das **ulEventType** -Element kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4fbd4-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="4fbd4-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="4fbd4-114">Ein globaler Fehler ist aufgetreten, beispielsweise eine Sitzung wurde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="4fbd4-115">Der **Info** -Member enthält eine [ERROR_NOTIFICATION](error_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4fbd4-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="4fbd4-117">Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="4fbd4-118">Der **Info** -Member enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4fbd4-119">_Uleventmaskfnevnewmail_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="4fbd4-120">Eine Nachricht wurde an den entsprechenden Empfänger Ordner für die Nachrichtenklasse übermittelt und wartet auf die Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="4fbd4-121">Der **Info** -Member enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4fbd4-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="4fbd4-123">Ein MAPI-Objekt wurde kopiert.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-123">A MAPI object has been copied.</span></span> <span data-ttu-id="4fbd4-124">Der **Info** -Member enthält eine [OBJECT_NOTIFICATION](object_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="4fbd4-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="4fbd4-126">Es wurde ein MAPI-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-126">A MAPI object has been created.</span></span> <span data-ttu-id="4fbd4-127">Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4fbd4-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="4fbd4-129">Ein MAPI-Objekt wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="4fbd4-130">Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4fbd4-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="4fbd4-132">Ein MAPI-Objekt wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-132">A MAPI object has changed.</span></span> <span data-ttu-id="4fbd4-133">Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4fbd4-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="4fbd4-135">Ein Nachrichtenspeicher-oder Adressbuchobjekt wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="4fbd4-136">Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4fbd4-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="4fbd4-138">Ein Suchvorgang wurde abgeschlossen, und die Ergebnisse sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="4fbd4-139">Der **Info** -Member enthält eine **OBJECT_NOTIFICATION** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="4fbd4-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="4fbd4-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="4fbd4-141">Informationen in einer Tabelle wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-141">Information in a table has changed.</span></span> <span data-ttu-id="4fbd4-142">Der **Info** -Member enthält eine [TABLE_NOTIFICATION](table_notification.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="4fbd4-143">**info**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-143">**info**</span></span>
  
> <span data-ttu-id="4fbd4-144">Vereinigung von Benachrichtigungs Strukturen, die die betroffenen Daten für einen bestimmten Ereignistyp beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="4fbd4-145">Die im **Info** -Element enthaltene Struktur hängt vom Wert des **ulEventType** -Members ab.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4fbd4-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fbd4-146">Remarks</span></span>

<span data-ttu-id="4fbd4-147">Mindestens eine **Benachrichtigungs** Struktur wird bei jedem Aufruf der [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode einer registrierten Advise-Senke als Eingabeparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="4fbd4-148">Die **Benachrichtigungs** Strukturen enthalten Informationen zu den bestimmten Ereignissen, die aufgetreten sind, und beschreiben die betroffenen Objekte.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="4fbd4-149">Bevor Clients oder Dienstanbieter, die eine Benachrichtigung erhalten, die Struktur zum Verarbeiten des Ereignisses verwenden können, müssen Sie den Ereignistyp wie im **ulEventType** -Element angegeben überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="4fbd4-150">Das Codebeispiel, das hier gezeigt wird, prüft beispielsweise, ob eine neue Nachricht eingeht, und gibt die Nachrichtenklasse der Nachricht aus, wenn ein solches Ereignis ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="4fbd4-151">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="4fbd4-152">**Thema**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-152">**Topic**</span></span>|<span data-ttu-id="4fbd4-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fbd4-154">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="4fbd4-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="4fbd4-155">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="4fbd4-156">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="4fbd4-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="4fbd4-157">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="4fbd4-158">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="4fbd4-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="4fbd4-159">Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fbd4-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fbd4-160">See also</span></span>


- [<span data-ttu-id="4fbd4-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="4fbd4-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="4fbd4-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="4fbd4-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="4fbd4-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="4fbd4-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fbd4-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="4fbd4-167">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4fbd4-167">MAPI Structures</span></span>](mapi-structures.md)


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
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432877"
---
# <a name="notification"></a><span data-ttu-id="d2ba7-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-103">NOTIFICATION</span></span>
 
<span data-ttu-id="d2ba7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2ba7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2ba7-105">Enthält Informationen zu einem aufgetretenen Ereignis und zu den Daten, die von dem Ereignis betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2ba7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d2ba7-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2ba7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2ba7-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d2ba7-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="d2ba7-108">Members</span></span>

<span data-ttu-id="d2ba7-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="d2ba7-109">**ulEventType**</span></span>
  
> <span data-ttu-id="d2ba7-110">Typ des aufgetretenen Benachrichtigungsereigniss.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-110">Type of notification event that occurred.</span></span> <span data-ttu-id="d2ba7-111">Der Wert des **ulEventType-Members** entspricht der Struktur, die in der **Info-Union enthalten** ist.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="d2ba7-112">Das **ulEventType-Element** kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d2ba7-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="d2ba7-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="d2ba7-114">Es ist ein globaler Fehler aufgetreten, z. B. eine in Bearbeitung heruntergefahrene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="d2ba7-115">Das **Element info** enthält eine [ERROR_NOTIFICATION](error_notification.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2ba7-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="d2ba7-117">Ein internes Ereignis, das von einem bestimmten Dienstanbieter definiert wurde, ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="d2ba7-118">Das **Element info** enthält eine [EXTENDED_NOTIFICATION](extended_notification.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2ba7-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="d2ba7-120">Eine Nachricht wurde an den entsprechenden Empfangsordner für die Nachrichtenklasse übermittelt und wartet auf die Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="d2ba7-121">Das **Element info** enthält eine [NEWMAIL_NOTIFICATION](newmail_notification.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2ba7-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="d2ba7-123">Ein MAPI-Objekt wurde kopiert.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-123">A MAPI object has been copied.</span></span> <span data-ttu-id="d2ba7-124">Das **Element info** enthält eine [OBJECT_NOTIFICATION](object_notification.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2ba7-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="d2ba7-126">Ein MAPI-Objekt wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-126">A MAPI object has been created.</span></span> <span data-ttu-id="d2ba7-127">Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2ba7-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="d2ba7-129">Ein MAPI-Objekt wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="d2ba7-130">Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2ba7-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="d2ba7-132">Ein MAPI-Objekt wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-132">A MAPI object has changed.</span></span> <span data-ttu-id="d2ba7-133">Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2ba7-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="d2ba7-135">Ein Nachrichtenspeicher oder ein Adressbuchobjekt wurde verschoben.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="d2ba7-136">Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2ba7-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="d2ba7-138">Ein Suchvorgang ist abgeschlossen, und die Ergebnisse sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="d2ba7-139">Das **Element info** enthält eine **OBJECT_NOTIFICATION** Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2ba7-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="d2ba7-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="d2ba7-141">Die Informationen in einer Tabelle haben sich geändert.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-141">Information in a table has changed.</span></span> <span data-ttu-id="d2ba7-142">Das **Element info** enthält eine [TABLE_NOTIFICATION](table_notification.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="d2ba7-143">**info**</span><span class="sxs-lookup"><span data-stu-id="d2ba7-143">**info**</span></span>
  
> <span data-ttu-id="d2ba7-144">Union von Benachrichtigungsstrukturen, die die betroffenen Daten für einen bestimmten Ereignistyp beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="d2ba7-145">Die im Element **info** enthaltene Struktur hängt vom Wert des **ulEventType-Mitglieds** ab.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d2ba7-146">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2ba7-146">Remarks</span></span>

<span data-ttu-id="d2ba7-147">Mindestens eine **BENACHRICHTIGUNGsstruktur** wird bei jedem Aufruf der [IMAPIAdviseSink::OnNotify-Methode als Eingabeparameter an die IMAPIAdviseSink::OnNotify-Methode einer registrierten](imapiadvisesink-onnotify.md) Hinweissenke übergeben.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="d2ba7-148">Die **NOTIFICATION-Strukturen** enthalten Informationen zu den jeweiligen Ereignissen, die aufgetreten sind, und beschreiben die betroffenen Objekte.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="d2ba7-149">Bevor Clients oder Dienstanbieter, die eine Benachrichtigung erhalten, die Struktur zum Verarbeiten des Ereignisses verwenden können, müssen sie den Ereignistyp überprüfen, wie im **ulEventType-Element** angegeben.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="d2ba7-150">Das hier gezeigte Codebeispiel überprüft beispielsweise, ob eine neue Nachricht eintreffen kann, und gibt nach dem Erkennen eines solchen Ereignisses die Nachrichtenklasse der Nachricht aus.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="d2ba7-151">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d2ba7-152">**Thema**</span><span class="sxs-lookup"><span data-stu-id="d2ba7-152">**Topic**</span></span>|<span data-ttu-id="d2ba7-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2ba7-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2ba7-154">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="d2ba7-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d2ba7-155">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d2ba7-156">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d2ba7-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d2ba7-157">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d2ba7-158">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="d2ba7-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d2ba7-159">Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d2ba7-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2ba7-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2ba7-160">See also</span></span>


- [<span data-ttu-id="d2ba7-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="d2ba7-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="d2ba7-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="d2ba7-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="d2ba7-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="d2ba7-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2ba7-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="d2ba7-167">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d2ba7-167">MAPI Structures</span></span>](mapi-structures.md)


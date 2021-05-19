---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415719"
---
# <a name="extended_notification"></a><span data-ttu-id="557ae-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="557ae-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="557ae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="557ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="557ae-105">Beschreibt Informationen, die sich auf ein ereignis beziehen, das Dienstanbieterspezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="557ae-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="557ae-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="557ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="557ae-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="557ae-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="557ae-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="557ae-108">Members</span></span>

 <span data-ttu-id="557ae-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="557ae-109">**ulEvent**</span></span>
  
> <span data-ttu-id="557ae-110">Erweiterter Ereigniscode, der vom Anbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="557ae-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="557ae-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="557ae-111">**cb**</span></span>
  
> <span data-ttu-id="557ae-112">Anzahl der Bytes in den ereignisspezifischen Parametern, auf die von **pbEventParameters verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="557ae-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="557ae-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="557ae-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="557ae-114">Zeiger auf ereignisspezifische Parameter.</span><span class="sxs-lookup"><span data-stu-id="557ae-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="557ae-115">Der Typ der verwendeten Parameter hängt vom Wert des **ulEvent-Mitglieds** ab. Diese Parameter werden vom Anbieter dokumentiert, der das Ereignis ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="557ae-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="557ae-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="557ae-116">Remarks</span></span>

<span data-ttu-id="557ae-117">Die **EXTENDED_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist.</span><span class="sxs-lookup"><span data-stu-id="557ae-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="557ae-118">Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine EXTENDED_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf _fnevExtended festgelegt._</span><span class="sxs-lookup"><span data-stu-id="557ae-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="557ae-119">Das erweiterte Ereignis wird von einem Dienstanbieter definiert, um einen Änderungstyp zu repräsentieren, der von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="557ae-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="557ae-120">Nur Clients, die vor der Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="557ae-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="557ae-121">Clients können ohne erweiterte Kenntnisse nicht ermitteln, ob ein Dienstanbieter ein erweitertes Ereignis unterstützt.</span><span class="sxs-lookup"><span data-stu-id="557ae-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="557ae-122">Wenn ein Dienstanbieter ein erweitertes Ereignis unterstützt, wird gezeigt, wie ein solches Ereignis beim Empfangen behandeln wird.</span><span class="sxs-lookup"><span data-stu-id="557ae-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="557ae-123">Eine erweiterte Benachrichtigung wird von der Sitzung gesendet, wenn sich ein Client abmeldet.</span><span class="sxs-lookup"><span data-stu-id="557ae-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="557ae-124">Registrieren Sie sich für diese Benachrichtigung, indem [Sie IMAPISession::Advise](imapisession-advise.md) aufrufen, wenn  _der lpEntryID-Parameter_ auf NULL und  _der cbEntryID-Parameter_ auf Null festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="557ae-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="557ae-125">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="557ae-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="557ae-126">**Thema**</span><span class="sxs-lookup"><span data-stu-id="557ae-126">**Topic**</span></span>|<span data-ttu-id="557ae-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="557ae-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="557ae-128">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="557ae-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="557ae-129">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="557ae-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="557ae-130">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="557ae-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="557ae-131">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="557ae-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="557ae-132">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="557ae-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="557ae-133">Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methoden](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="557ae-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="557ae-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="557ae-134">See also</span></span>



[<span data-ttu-id="557ae-135">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="557ae-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="557ae-136">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="557ae-136">MAPI Structures</span></span>](mapi-structures.md)


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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341118"
---
# <a name="extendednotification"></a><span data-ttu-id="8fb9b-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8fb9b-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8fb9b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fb9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fb9b-105">Beschreibt Informationen, die sich auf ein Ereignis beziehen, das Dienstanbieter spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8fb9b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8fb9b-106">Header file:</span></span>  <br/> |<span data-ttu-id="8fb9b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8fb9b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="8fb9b-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="8fb9b-108">Members</span></span>

 <span data-ttu-id="8fb9b-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-109">**ulEvent**</span></span>
  
> <span data-ttu-id="8fb9b-110">Erweiterter Ereigniscode, der vom Anbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="8fb9b-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-111">**cb**</span></span>
  
> <span data-ttu-id="8fb9b-112">Die Anzahl der Bytes in den ereignisspezifischen Parametern, auf die von **pbEventParameters**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="8fb9b-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="8fb9b-114">Zeiger auf ereignisspezifische Parameter.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="8fb9b-115">Welcher Typ von Parametern verwendet wird, hängt vom Wert des **ulEvent** -Elements ab; Diese Parameter werden vom Anbieter dokumentiert, der das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8fb9b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fb9b-116">Remarks</span></span>

<span data-ttu-id="8fb9b-117">Die **EXTENDED_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8fb9b-118">Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **EXTENDED_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf _fnevExtended_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="8fb9b-119">Das Extended-Ereignis wird von einem Dienstanbieter definiert, der eine Art von Änderung darstellt, die von keinem der anderen vordefinierten Ereignisse abgedeckt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="8fb9b-120">Nur Clients, die vor Ihrer Registrierung wissen, dass ein Dienstanbieter ein erweitertes Ereignis unterstützt, können sich für dieses Ereignis registrieren.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="8fb9b-121">Es ist für Clients nicht möglich, ohne Erweitertes Wissen zu ermitteln, ob ein Dienstanbieter ein Extended-Ereignis unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="8fb9b-122">Wenn ein Dienstanbieter ein Extended-Ereignis unterstützt, wird gezeigt, wie ein solches Ereignis beim Empfang behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="8fb9b-123">Eine erweiterte Benachrichtigung wird von der Sitzung gesendet, wenn sich ein Client abmeldet.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="8fb9b-124">Registrieren Sie sich für diese Benachrichtigung, indem Sie [IMAPISession:: Advise](imapisession-advise.md) aufrufen, wobei der _lpEntryID_ -Parameter auf NULL festgelegt ist und der _cbEntryID_ -Parameter auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="8fb9b-125">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8fb9b-126">**Thema**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-126">**Topic**</span></span>|<span data-ttu-id="8fb9b-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8fb9b-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fb9b-128">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="8fb9b-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8fb9b-129">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8fb9b-130">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8fb9b-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8fb9b-131">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8fb9b-132">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8fb9b-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8fb9b-133">Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methoden zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fb9b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fb9b-134">See also</span></span>



[<span data-ttu-id="8fb9b-135">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8fb9b-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="8fb9b-136">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8fb9b-136">MAPI Structures</span></span>](mapi-structures.md)


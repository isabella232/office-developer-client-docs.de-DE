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
ms.openlocfilehash: 5e23d9b829a941e3add8b8d8e137c73052b08aa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791658"
---
# <a name="extendednotification"></a><span data-ttu-id="13256-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="13256-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="13256-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13256-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13256-105">Beschreibt die Informationen, die auf ein Ereignis bezieht, die anbieterspezifische-Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="13256-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13256-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="13256-106">Header file:</span></span>  <br/> |<span data-ttu-id="13256-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13256-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="13256-108">Members</span><span class="sxs-lookup"><span data-stu-id="13256-108">Members</span></span>

 <span data-ttu-id="13256-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="13256-109">**ulEvent**</span></span>
  
> <span data-ttu-id="13256-110">Erweiterte Ereigniscode, die vom Anbieter definiert ist.</span><span class="sxs-lookup"><span data-stu-id="13256-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="13256-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="13256-111">**cb**</span></span>
  
> <span data-ttu-id="13256-112">Anzahl der Bytes in der Ereignis-spezifischen Parametern auf **PbEventParameters**zeigt.</span><span class="sxs-lookup"><span data-stu-id="13256-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="13256-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="13256-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="13256-114">Zeiger auf Ereignis-spezifischen Parametern.</span><span class="sxs-lookup"><span data-stu-id="13256-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="13256-115">Der Typ von Parametern, die verwendet werden, hängt von den Wert des Elements **UlEvent** ab. Diese Parameter sind vom Anbieter dokumentiert, die das Ereignis ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="13256-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="13256-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13256-116">Remarks</span></span>

<span data-ttu-id="13256-117">Die **EXTENDED_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="13256-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="13256-118">Wenn **Info** Mitglied eine **Benachrichtigung** Struktur eine **EXTENDED_NOTIFICATION** -Struktur enthält, wird das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf _FnevExtended_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="13256-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="13256-119">Das erweiterte-Ereignis wird durch einen Dienstanbieter, eine Art der Änderung darstellen, die von keiner anderen vordefinierten Ereignisse behandelt werden kann nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="13256-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="13256-120">Für dieses Ereignis können nur Clients, die wissen, bevor sie registrieren, dass es sich bei ein Dienstanbieter ein erweiterte Ereignis unterstützt registrieren.</span><span class="sxs-lookup"><span data-stu-id="13256-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="13256-121">Es ist nicht möglich für Clients ohne guten Kenntnissen zu bestimmen, ob es sich bei ein Dienstanbieter ein erweiterte Ereignis unterstützt.</span><span class="sxs-lookup"><span data-stu-id="13256-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="13256-122">Wenn ein Dienstanbieter ein erweiterte Ereignis unterstützt, wird gezeigt, wie ein Ereignis beim Empfang zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="13256-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="13256-123">Wenn ein Client abmeldet eine erweiterte Benachrichtigung von der Sitzung gesendet.</span><span class="sxs-lookup"><span data-stu-id="13256-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="13256-124">Registrieren Sie für diese Benachrichtigung durch Aufrufen von [IMAPISession::Advise](imapisession-advise.md) mit der _LpEntryID_ -Parameter auf NULL und der _CbEntryID_ -Parameter auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="13256-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="13256-125">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="13256-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="13256-126">**Thema**</span><span class="sxs-lookup"><span data-stu-id="13256-126">**Topic**</span></span>|<span data-ttu-id="13256-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13256-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13256-128">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="13256-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="13256-129">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="13256-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="13256-130">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="13256-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="13256-131">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13256-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="13256-132">Benachrichtigung bei unterstützenden</span><span class="sxs-lookup"><span data-stu-id="13256-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="13256-133">Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methoden verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="13256-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13256-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13256-134">See also</span></span>



[<span data-ttu-id="13256-135">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="13256-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="13256-136">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="13256-136">MAPI Structures</span></span>](mapi-structures.md)


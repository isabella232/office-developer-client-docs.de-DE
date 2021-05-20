---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439856"
---
# <a name="newmail_notification"></a><span data-ttu-id="e89b1-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e89b1-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="e89b1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e89b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e89b1-105">Beschreibt Informationen, die sich auf das Eintreffen einer neuen Nachricht beziehen.</span><span class="sxs-lookup"><span data-stu-id="e89b1-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e89b1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e89b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="e89b1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e89b1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="e89b1-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e89b1-108">Members</span></span>

 <span data-ttu-id="e89b1-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="e89b1-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="e89b1-110">Anzahl der Bytes in der Eintrags-ID, auf die das **lpEntryID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="e89b1-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="e89b1-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="e89b1-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="e89b1-112">Zeiger auf die Eintrags-ID der neu eingetroffenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e89b1-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="e89b1-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="e89b1-113">**cbParentID**</span></span>
  
> <span data-ttu-id="e89b1-114">Anzahl der Bytes in der Eintrags-ID, auf die das **lpParentID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="e89b1-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="e89b1-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="e89b1-115">**lpParentID**</span></span>
  
> <span data-ttu-id="e89b1-116">Zeiger auf die Eintrags-ID des Empfangsordners für die neu eingetroffene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e89b1-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="e89b1-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e89b1-117">**ulFlags**</span></span>
  
> <span data-ttu-id="e89b1-118">Bitmaske von Flags, die verwendet werden, um das Format der Zeichenfolgeneigenschaften zu beschreiben, die in der Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e89b1-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="e89b1-119">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e89b1-119">The following flag can be set:</span></span>
    
<span data-ttu-id="e89b1-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e89b1-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e89b1-121">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e89b1-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e89b1-122">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e89b1-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e89b1-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="e89b1-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="e89b1-124">Zeiger auf die Nachrichtenklasse der neu eingetroffenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e89b1-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="e89b1-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="e89b1-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="e89b1-126">Bitmaske von Flags, die den aktuellen Status der neu eingetroffenen Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e89b1-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="e89b1-127">Das **ulMessageFlags-Element** ist eine Kopie der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e89b1-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e89b1-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e89b1-128">Remarks</span></span>

<span data-ttu-id="e89b1-129">Die **NEWMAIL_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist.</span><span class="sxs-lookup"><span data-stu-id="e89b1-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="e89b1-130">Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine NEWMAIL_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf  _fnevNewMail festgelegt._</span><span class="sxs-lookup"><span data-stu-id="e89b1-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="e89b1-131">MAPI verwendet die **NEWMAIL_NOTIFICATION** nur als Mitglied der **NOTIFICATION-Struktur,** die Informationen zu einem Benachrichtigungsereignis für die Hinweissenke enthält.</span><span class="sxs-lookup"><span data-stu-id="e89b1-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="e89b1-132">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="e89b1-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="e89b1-133">**Thema**</span><span class="sxs-lookup"><span data-stu-id="e89b1-133">**Topic**</span></span>|<span data-ttu-id="e89b1-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e89b1-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e89b1-135">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="e89b1-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="e89b1-136">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="e89b1-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="e89b1-137">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e89b1-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="e89b1-138">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="e89b1-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="e89b1-139">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="e89b1-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="e89b1-140">Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e89b1-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e89b1-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e89b1-141">See also</span></span>



[<span data-ttu-id="e89b1-142">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="e89b1-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e89b1-143">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e89b1-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="e89b1-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e89b1-144">MAPI Structures</span></span>](mapi-structures.md)


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
# <a name="newmailnotification"></a><span data-ttu-id="6f381-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6f381-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="6f381-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f381-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f381-105">Beschreibt Informationen, die sich auf das Eintreffen einer neuen Nachricht beziehen.</span><span class="sxs-lookup"><span data-stu-id="6f381-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f381-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6f381-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f381-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6f381-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="6f381-108">Members</span><span class="sxs-lookup"><span data-stu-id="6f381-108">Members</span></span>

 <span data-ttu-id="6f381-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="6f381-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="6f381-110">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpEntryID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6f381-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="6f381-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="6f381-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="6f381-112">Zeiger auf die Eintrags-ID der neu angekommenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6f381-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="6f381-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="6f381-113">**cbParentID**</span></span>
  
> <span data-ttu-id="6f381-114">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpParentID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6f381-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="6f381-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="6f381-115">**lpParentID**</span></span>
  
> <span data-ttu-id="6f381-116">Zeiger auf die Eintrags-ID des Empfangs Ordners für die neu eingetroffene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6f381-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="6f381-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6f381-117">**ulFlags**</span></span>
  
> <span data-ttu-id="6f381-118">Bitmaske von Flags zur Beschreibung des Formats der Zeichenfolgeneigenschaften, die in der Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6f381-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="6f381-119">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6f381-119">The following flag can be set:</span></span>
    
<span data-ttu-id="6f381-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f381-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6f381-121">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6f381-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6f381-122">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6f381-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6f381-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="6f381-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="6f381-124">Zeiger auf die Nachrichtenklasse der neu angekommenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6f381-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="6f381-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="6f381-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="6f381-126">Bitmaske von Flags, die den aktuellen Status der neu angekommenen Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6f381-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="6f381-127">Das **ulMessageFlags** -Element ist eine Kopie der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6f381-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f381-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f381-128">Remarks</span></span>

<span data-ttu-id="6f381-129">Die **NEWMAIL_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6f381-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="6f381-130">Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **NEWMAIL_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf uleventmaskfnevnewmail festgelegt _._</span><span class="sxs-lookup"><span data-stu-id="6f381-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="6f381-131">MAPI verwendet die **NEWMAIL_NOTIFICATION** -Struktur nur als Mitglied der **Benachrichtigungs** Struktur, die Informationen zu einem Benachrichtigungsereignis für die Advise-Senke enthält.</span><span class="sxs-lookup"><span data-stu-id="6f381-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="6f381-132">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="6f381-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="6f381-133">**Thema**</span><span class="sxs-lookup"><span data-stu-id="6f381-133">**Topic**</span></span>|<span data-ttu-id="6f381-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f381-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f381-135">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="6f381-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="6f381-136">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="6f381-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="6f381-137">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="6f381-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="6f381-138">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="6f381-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="6f381-139">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6f381-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="6f381-140">Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6f381-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f381-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f381-141">See also</span></span>



[<span data-ttu-id="6f381-142">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="6f381-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6f381-143">Kanonische PidTagMessageFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f381-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="6f381-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6f381-144">MAPI Structures</span></span>](mapi-structures.md)


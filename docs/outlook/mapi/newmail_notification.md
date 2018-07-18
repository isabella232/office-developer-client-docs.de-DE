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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793279"
---
# <a name="newmailnotification"></a><span data-ttu-id="66902-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="66902-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="66902-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66902-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66902-105">Beschreibt die Informationen, die über den Eingang einer neuen Nachricht beziehen.</span><span class="sxs-lookup"><span data-stu-id="66902-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66902-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="66902-106">Header file:</span></span>  <br/> |<span data-ttu-id="66902-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66902-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="66902-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="66902-108">Members</span></span>

 <span data-ttu-id="66902-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="66902-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="66902-110">Anzahl der Bytes in die Eintrags-ID auf den Member **LpEntryID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="66902-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="66902-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="66902-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="66902-112">Zeiger auf die Eintrags-ID der neu empfangene Meldung.</span><span class="sxs-lookup"><span data-stu-id="66902-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="66902-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="66902-113">**cbParentID**</span></span>
  
> <span data-ttu-id="66902-114">Anzahl der Bytes in die Eintrags-ID auf den Member **LpParentID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="66902-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="66902-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="66902-115">**lpParentID**</span></span>
  
> <span data-ttu-id="66902-116">Zeiger auf die Eintrags-ID des Ordners für die neu empfangene Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="66902-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="66902-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="66902-117">**ulFlags**</span></span>
  
> <span data-ttu-id="66902-118">Bitmaske aus Flags verwendet, um das Format der Zeichenfolgeneigenschaften der Nachricht enthaltene beschreiben.</span><span class="sxs-lookup"><span data-stu-id="66902-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="66902-119">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="66902-119">The following flag can be set:</span></span>
    
<span data-ttu-id="66902-120">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="66902-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="66902-121">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="66902-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="66902-122">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="66902-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="66902-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="66902-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="66902-124">Zeiger auf die Nachrichtenklasse der neu empfangene Meldung.</span><span class="sxs-lookup"><span data-stu-id="66902-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="66902-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="66902-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="66902-126">Bitmaske aus Flags, die den aktuellen Status der neu empfangene Nachricht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="66902-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="66902-127">Der **UlMessageFlags** -Member ist eine Kopie der Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="66902-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66902-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66902-128">Remarks</span></span>

<span data-ttu-id="66902-129">Die **NEWMAIL_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="66902-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="66902-130">Wenn das **Info** Mitglied einer **Benachrichtigung** Struktur eine **NEWMAIL_NOTIFICATION** Struktur enthält, das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf festgelegt ist _FnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="66902-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="66902-131">MAPI verwendet die **NEWMAIL_NOTIFICATION** -Struktur nur als Mitglied der **Benachrichtigung** -Struktur, die Informationen zu einem Benachrichtigungsereignis für die Advise-Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="66902-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="66902-132">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="66902-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="66902-133">**Thema**</span><span class="sxs-lookup"><span data-stu-id="66902-133">**Topic**</span></span>|<span data-ttu-id="66902-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66902-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66902-135">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="66902-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="66902-136">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="66902-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="66902-137">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="66902-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="66902-138">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="66902-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="66902-139">Unterstützen von Ereignisbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="66902-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="66902-140">Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="66902-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66902-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66902-141">See also</span></span>



[<span data-ttu-id="66902-142">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="66902-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="66902-143">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66902-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="66902-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="66902-144">MAPI Structures</span></span>](mapi-structures.md)


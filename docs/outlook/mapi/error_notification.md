---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425442"
---
# <a name="errornotification"></a><span data-ttu-id="8431d-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8431d-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8431d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8431d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8431d-105">Beschreibt Informationen zu einem wichtigen Fehler.</span><span class="sxs-lookup"><span data-stu-id="8431d-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="8431d-106">Dadurch wird eine Fehlerbenachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="8431d-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8431d-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8431d-107">Header file:</span></span>  <br/> |<span data-ttu-id="8431d-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8431d-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a><span data-ttu-id="8431d-109">Members</span><span class="sxs-lookup"><span data-stu-id="8431d-109">Members</span></span>

 <span data-ttu-id="8431d-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="8431d-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="8431d-111">Anzahl der Bytes in der Eintrags-ID, auf die von **lpEntryID**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8431d-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="8431d-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="8431d-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="8431d-113">Zeiger auf die Eintrags-ID des Objekts, das den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="8431d-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="8431d-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="8431d-114">**scode**</span></span>
  
> <span data-ttu-id="8431d-115">Fehlerwert für den kritischen Fehler.</span><span class="sxs-lookup"><span data-stu-id="8431d-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="8431d-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="8431d-116">**ulFlags**</span></span>
  
> <span data-ttu-id="8431d-117">Bitmaske der Flags, mit denen das Format des Texts festgelegt wird, der vom **lpszError** -Element in der Struktur verweist, auf die durch **lpMAPIError**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8431d-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="8431d-118">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8431d-118">The following flag can be set:</span></span>
    
<span data-ttu-id="8431d-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8431d-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8431d-120">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="8431d-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8431d-121">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="8431d-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8431d-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="8431d-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="8431d-123">Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8431d-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8431d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8431d-124">Remarks</span></span>

<span data-ttu-id="8431d-125">Die **ERROR_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8431d-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8431d-126">Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **ERROR_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf _fnevCriticalError_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8431d-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="8431d-127">Der Wert des **cbEntryID** -Elements und des **lpEntryID** -Members kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8431d-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="8431d-128">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="8431d-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8431d-129">**Thema**</span><span class="sxs-lookup"><span data-stu-id="8431d-129">**Topic**</span></span>|<span data-ttu-id="8431d-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8431d-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8431d-131">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="8431d-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8431d-132">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="8431d-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8431d-133">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8431d-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8431d-134">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="8431d-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8431d-135">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8431d-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8431d-136">Erläuterung, wie Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="8431d-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8431d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8431d-137">See also</span></span>



[<span data-ttu-id="8431d-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8431d-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8431d-139">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8431d-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="8431d-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8431d-140">MAPI Structures</span></span>](mapi-structures.md)


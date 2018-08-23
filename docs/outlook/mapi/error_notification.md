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
ms.openlocfilehash: 2405799fa59abf58583553f8e2d3718d68411a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574972"
---
# <a name="errornotification"></a><span data-ttu-id="e14a7-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e14a7-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="e14a7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e14a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e14a7-105">Beschreibt die Informationen, die auf ein schwerwiegender Fehler beziehen.</span><span class="sxs-lookup"><span data-stu-id="e14a7-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="e14a7-106">Daraufhin wird eine Benachrichtigung Fehler generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e14a7-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e14a7-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e14a7-107">Header file:</span></span>  <br/> |<span data-ttu-id="e14a7-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e14a7-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e14a7-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="e14a7-109">Members</span></span>

 <span data-ttu-id="e14a7-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="e14a7-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="e14a7-111">Anzahl der Bytes in die Eintrags-ID auf **LpEntryID**zeigt.</span><span class="sxs-lookup"><span data-stu-id="e14a7-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="e14a7-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="e14a7-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="e14a7-113">Zeiger auf die Eintrags-ID des Objekts, das den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="e14a7-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="e14a7-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="e14a7-114">**scode**</span></span>
  
> <span data-ttu-id="e14a7-115">Fehlerwert für den kritischen Fehler.</span><span class="sxs-lookup"><span data-stu-id="e14a7-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="e14a7-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e14a7-116">**ulFlags**</span></span>
  
> <span data-ttu-id="e14a7-117">Bitmaske aus Flags verwendet, um das Format des Texts festzulegen, auf dem **LpszError** -Element in der Struktur auf den **LpMAPIError**zeigt.</span><span class="sxs-lookup"><span data-stu-id="e14a7-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="e14a7-118">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e14a7-118">The following flag can be set:</span></span>
    
<span data-ttu-id="e14a7-119">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e14a7-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e14a7-120">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="e14a7-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e14a7-121">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="e14a7-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e14a7-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="e14a7-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="e14a7-123">Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e14a7-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e14a7-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e14a7-124">Remarks</span></span>

<span data-ttu-id="e14a7-125">Die **ERROR_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="e14a7-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="e14a7-126">Wenn **Info** Mitglied eine **Benachrichtigung** Struktur eine **ERROR_NOTIFICATION** -Struktur enthält, wird das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf _FnevCriticalError_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e14a7-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="e14a7-127">Der Wert des Members **CbEntryID** und der **LpEntryID** Member kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e14a7-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="e14a7-128">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e14a7-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="e14a7-129">**Thema**</span><span class="sxs-lookup"><span data-stu-id="e14a7-129">**Topic**</span></span>|<span data-ttu-id="e14a7-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e14a7-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e14a7-131">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="e14a7-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="e14a7-132">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="e14a7-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="e14a7-133">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e14a7-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="e14a7-134">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e14a7-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="e14a7-135">Unterstützen von Ereignisbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e14a7-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="e14a7-136">Erläuterung der wie-Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="e14a7-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e14a7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e14a7-137">See also</span></span>



[<span data-ttu-id="e14a7-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e14a7-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e14a7-139">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="e14a7-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="e14a7-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e14a7-140">MAPI Structures</span></span>](mapi-structures.md)


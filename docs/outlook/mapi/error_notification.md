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
# <a name="error_notification"></a><span data-ttu-id="c9a28-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9a28-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c9a28-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9a28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9a28-105">Beschreibt Informationen, die sich auf einen kritischen Fehler beziehen.</span><span class="sxs-lookup"><span data-stu-id="c9a28-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="c9a28-106">Dadurch wird eine Fehlerbenachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="c9a28-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9a28-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c9a28-107">Header file:</span></span>  <br/> |<span data-ttu-id="c9a28-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9a28-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c9a28-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="c9a28-109">Members</span></span>

 <span data-ttu-id="c9a28-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c9a28-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="c9a28-111">Anzahl der Bytes in der Eintrags-ID, auf die **von lpEntryID verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="c9a28-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="c9a28-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c9a28-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="c9a28-113">Zeiger auf den Eintragsbezeichner des Objekts, das den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="c9a28-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="c9a28-114">**scode**</span><span class="sxs-lookup"><span data-stu-id="c9a28-114">**scode**</span></span>
  
> <span data-ttu-id="c9a28-115">Fehlerwert für den kritischen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c9a28-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="c9a28-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c9a28-116">**ulFlags**</span></span>
  
> <span data-ttu-id="c9a28-117">Bitmaske von Flags, die verwendet werden, um das Format des Texts zu bestimmen, auf das das **lpszError-Element** in der Struktur verweist, auf das **lpMAPIError verweist.**</span><span class="sxs-lookup"><span data-stu-id="c9a28-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="c9a28-118">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c9a28-118">The following flag can be set:</span></span>
    
<span data-ttu-id="c9a28-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9a28-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c9a28-120">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c9a28-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c9a28-121">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c9a28-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c9a28-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="c9a28-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="c9a28-123">Zeiger auf eine [MAPIERROR-Struktur,](mapierror.md) die den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c9a28-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9a28-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9a28-124">Remarks</span></span>

<span data-ttu-id="c9a28-125">Die **ERROR_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist.</span><span class="sxs-lookup"><span data-stu-id="c9a28-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c9a28-126">Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine ERROR_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf _fnevCriticalError festgelegt._</span><span class="sxs-lookup"><span data-stu-id="c9a28-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="c9a28-127">Der Wert des **cbEntryID-Members** und des **lpEntryID-Members** kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c9a28-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="c9a28-128">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="c9a28-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c9a28-129">**Thema**</span><span class="sxs-lookup"><span data-stu-id="c9a28-129">**Topic**</span></span>|<span data-ttu-id="c9a28-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9a28-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9a28-131">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="c9a28-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c9a28-132">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="c9a28-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c9a28-133">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c9a28-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c9a28-134">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="c9a28-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c9a28-135">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c9a28-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c9a28-136">Hier erfahren Sie, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c9a28-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9a28-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9a28-137">See also</span></span>



[<span data-ttu-id="c9a28-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c9a28-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c9a28-139">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c9a28-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="c9a28-140">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c9a28-140">MAPI Structures</span></span>](mapi-structures.md)


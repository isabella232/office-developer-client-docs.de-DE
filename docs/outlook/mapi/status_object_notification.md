---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426268"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="c7582-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c7582-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c7582-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7582-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7582-105">Beschreibt ein Statusobjekt, das von einer Änderung betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="c7582-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7582-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c7582-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7582-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c7582-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="c7582-108">Members</span><span class="sxs-lookup"><span data-stu-id="c7582-108">Members</span></span>

 <span data-ttu-id="c7582-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c7582-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c7582-110">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpEntryID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c7582-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c7582-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c7582-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c7582-112">Zeiger auf die Eintrags-ID des geänderten Status Objekts.</span><span class="sxs-lookup"><span data-stu-id="c7582-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="c7582-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c7582-113">**cValues**</span></span>
  
> <span data-ttu-id="c7582-114">Die Anzahl der [SPropValue](spropvalue.md) -Strukturen im Array, auf die vom **lpPropVals** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c7582-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="c7582-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="c7582-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="c7582-116">Zeiger auf ein Array von **SPropValue** -Strukturen, die die Eigenschaften des geänderten Status-Objekts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c7582-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7582-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7582-117">Remarks</span></span>

<span data-ttu-id="c7582-118">Die **STATUS_OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c7582-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c7582-119">Die **STATUS_OBJECT_NOTIFICATION** -Struktur ist in einer Status Objekt Benachrichtigung für ein Ereignis vom Typ _fnevStatusObjectModified_enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7582-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="c7582-120">Status Objekt Benachrichtigung ist eine interne MAPI-Benachrichtigung; Clients und Dienstanbieter können sich nicht für IT registrieren, und Dienstanbieter können Sie nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="c7582-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="c7582-121">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="c7582-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c7582-122">**Thema**</span><span class="sxs-lookup"><span data-stu-id="c7582-122">**Topic**</span></span>|<span data-ttu-id="c7582-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7582-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7582-124">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="c7582-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c7582-125">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="c7582-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c7582-126">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c7582-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c7582-127">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="c7582-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c7582-128">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c7582-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c7582-129">Erläuterung, wie Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c7582-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7582-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7582-130">See also</span></span>



[<span data-ttu-id="c7582-131">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c7582-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c7582-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c7582-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c7582-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c7582-133">MAPI Structures</span></span>](mapi-structures.md)


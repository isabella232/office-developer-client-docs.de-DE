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
# <a name="status_object_notification"></a><span data-ttu-id="b7f3e-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b7f3e-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="b7f3e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7f3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7f3e-105">Beschreibt ein Statusobjekt, das von einer Änderung betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7f3e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b7f3e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7f3e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7f3e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="b7f3e-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="b7f3e-108">Members</span></span>

 <span data-ttu-id="b7f3e-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="b7f3e-110">Anzahl der Bytes in der Eintrags-ID, auf die das **lpEntryID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="b7f3e-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="b7f3e-112">Zeiger auf die Eintrags-ID des geänderten Statusobjekts.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="b7f3e-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-113">**cValues**</span></span>
  
> <span data-ttu-id="b7f3e-114">Anzahl der [SPropValue-Strukturen](spropvalue.md) im Array, auf das das **lpPropVals-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="b7f3e-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="b7f3e-116">Zeiger auf ein Array von **SPropValue-Strukturen,** die die Eigenschaften des geänderten Statusobjekts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b7f3e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7f3e-117">Remarks</span></span>

<span data-ttu-id="b7f3e-118">Die **STATUS_OBJECT_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b7f3e-119">Die **STATUS_OBJECT_NOTIFICATION** ist in einer Statusobjektbenachrichtigung für ein Ereignis vom Typ _fnevStatusObjectModified enthalten._</span><span class="sxs-lookup"><span data-stu-id="b7f3e-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="b7f3e-120">Status-Objektbenachrichtigung ist eine interne #A0 Clients und Dienstanbieter können sich nicht dafür registrieren, und Dienstanbieter können sie nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="b7f3e-121">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b7f3e-122">**Thema**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-122">**Topic**</span></span>|<span data-ttu-id="b7f3e-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7f3e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7f3e-124">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="b7f3e-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b7f3e-125">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b7f3e-126">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b7f3e-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b7f3e-127">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b7f3e-128">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b7f3e-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b7f3e-129">Hier erfahren Sie, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b7f3e-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7f3e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7f3e-130">See also</span></span>



[<span data-ttu-id="b7f3e-131">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b7f3e-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="b7f3e-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b7f3e-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b7f3e-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="b7f3e-133">MAPI Structures</span></span>](mapi-structures.md)


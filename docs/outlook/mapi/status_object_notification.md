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
ms.openlocfilehash: ba93cd0343121751ab12514fe3f09e5a480d5b23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582273"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="7ee3d-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7ee3d-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="7ee3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ee3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ee3d-105">Beschreibt ein Statusobjekt, das von einer Änderung betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ee3d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7ee3d-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ee3d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ee3d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="7ee3d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7ee3d-108">Members</span></span>

 <span data-ttu-id="7ee3d-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="7ee3d-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="7ee3d-110">Anzahl der Bytes in die Eintrags-ID auf den Member **LpEntryID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="7ee3d-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="7ee3d-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="7ee3d-112">Zeiger auf die Eintrags-ID des geänderten Status-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="7ee3d-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7ee3d-113">**cValues**</span></span>
  
> <span data-ttu-id="7ee3d-114">Anzahl der [SPropValue](spropvalue.md) Strukturen im Array auf der Member **LpPropVals** zeigt.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="7ee3d-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="7ee3d-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="7ee3d-116">Zeiger auf ein Array von **SPropValue** -Strukturen, die die Eigenschaften des geänderten Status-Objekts zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ee3d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ee3d-117">Remarks</span></span>

<span data-ttu-id="7ee3d-118">Die **STATUS_OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="7ee3d-119">Die Struktur **STATUS_OBJECT_NOTIFICATION** ist eine Benachrichtigung zum Status-Objekt für ein Ereignis des Typs _FnevStatusObjectModified_enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="7ee3d-120">Benachrichtigung über den-Objekt ist eine interne MAPI-Benachrichtigung an. Clients und -Dienstanbieter können nicht für sie registrieren und Dienstanbieter können es nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="7ee3d-121">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="7ee3d-122">**Thema**</span><span class="sxs-lookup"><span data-stu-id="7ee3d-122">**Topic**</span></span>|<span data-ttu-id="7ee3d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ee3d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ee3d-124">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="7ee3d-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="7ee3d-125">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="7ee3d-126">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7ee3d-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="7ee3d-127">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="7ee3d-128">Unterstützen von Ereignisbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7ee3d-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="7ee3d-129">Erläuterung der wie-Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7ee3d-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ee3d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ee3d-130">See also</span></span>



[<span data-ttu-id="7ee3d-131">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7ee3d-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7ee3d-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7ee3d-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7ee3d-133">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7ee3d-133">MAPI Structures</span></span>](mapi-structures.md)


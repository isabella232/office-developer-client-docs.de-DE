---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279886"
---
# <a name="objectnotification"></a><span data-ttu-id="1526b-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1526b-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="1526b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1526b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1526b-105">Enthält Informationen zu einem Objekt, das einer Änderung unterzogen wurde, beispielsweise kopiert oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1526b-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1526b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1526b-106">Header file:</span></span>  <br/> |<span data-ttu-id="1526b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1526b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="1526b-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="1526b-108">Members</span></span>

 <span data-ttu-id="1526b-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="1526b-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="1526b-110">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpEntryID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1526b-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="1526b-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="1526b-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="1526b-112">Zeiger auf die Eintrags-ID des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="1526b-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="1526b-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="1526b-113">**ulObjType**</span></span>
  
> <span data-ttu-id="1526b-114">Typ des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="1526b-114">Type of object affected.</span></span> <span data-ttu-id="1526b-115">Folgende Typen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="1526b-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="1526b-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="1526b-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="1526b-117">Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="1526b-117">Message store.</span></span> 
    
<span data-ttu-id="1526b-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="1526b-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="1526b-119">Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="1526b-119">Address book.</span></span> 
    
<span data-ttu-id="1526b-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="1526b-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="1526b-121">Ordner.</span><span class="sxs-lookup"><span data-stu-id="1526b-121">Folder.</span></span>
    
<span data-ttu-id="1526b-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="1526b-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="1526b-123">Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="1526b-123">Address book container.</span></span>
    
<span data-ttu-id="1526b-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="1526b-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="1526b-125">Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1526b-125">Message.</span></span>
    
<span data-ttu-id="1526b-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="1526b-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="1526b-127">Messaging Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1526b-127">Messaging user.</span></span>
    
<span data-ttu-id="1526b-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="1526b-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="1526b-129">Anlage.</span><span class="sxs-lookup"><span data-stu-id="1526b-129">Attachment.</span></span>
    
<span data-ttu-id="1526b-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="1526b-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="1526b-131">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="1526b-131">Distribution list.</span></span>
    
<span data-ttu-id="1526b-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="1526b-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="1526b-133">Profil Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="1526b-133">Profile section.</span></span>
    
<span data-ttu-id="1526b-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="1526b-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="1526b-135">Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1526b-135">Status object.</span></span>
    
<span data-ttu-id="1526b-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="1526b-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="1526b-137">Session-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1526b-137">Session object.</span></span>
    
 <span data-ttu-id="1526b-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="1526b-138">**cbParentID**</span></span>
  
> <span data-ttu-id="1526b-139">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpParentID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1526b-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="1526b-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="1526b-140">**lpParentID**</span></span>
  
> <span data-ttu-id="1526b-141">Zeiger auf die Eintrags-ID des übergeordneten Elements des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="1526b-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="1526b-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="1526b-142">**cbOldID**</span></span>
  
> <span data-ttu-id="1526b-143">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpOldID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1526b-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="1526b-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="1526b-144">**lpOldID**</span></span>
  
> <span data-ttu-id="1526b-145">Zeiger auf die Eintrags-ID des ursprünglichen Objekts.</span><span class="sxs-lookup"><span data-stu-id="1526b-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="1526b-146">Dieser Zeiger kann NULL sein, wenn das Ereignis kein Originalobjekt erfordert.</span><span class="sxs-lookup"><span data-stu-id="1526b-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="1526b-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="1526b-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="1526b-148">Die Anzahl der Bytes in der Eintrags-ID, auf die durch das **lpOldParentID** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1526b-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="1526b-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="1526b-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="1526b-150">Zeiger auf die Eintrags-ID des übergeordneten Elements des ursprünglichen Objekts.</span><span class="sxs-lookup"><span data-stu-id="1526b-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="1526b-151">Dieser Zeiger kann NULL sein, wenn das Ereignis kein Originalobjekt erfordert.</span><span class="sxs-lookup"><span data-stu-id="1526b-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="1526b-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="1526b-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="1526b-153">Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die die Eigenschaftstags enthält, die die vom Ereignis betroffenen Eigenschaften kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="1526b-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1526b-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1526b-154">Remarks</span></span>

<span data-ttu-id="1526b-155">Die **OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Vereinigung von Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1526b-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="1526b-156">Wenn der **Info** -Member einer **Benachrichtigungs** Struktur eine **OBJECT_NOTIFICATION** -Struktur enthält, wird das **ulEventType** -Element der **Benachrichtigungs** Struktur auf einen der folgenden Ereignistypen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="1526b-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="1526b-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="1526b-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="1526b-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="1526b-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="1526b-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="1526b-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="1526b-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="1526b-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="1526b-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="1526b-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="1526b-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="1526b-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="1526b-163">Das durch den fnevSearchComplete-Ereignistyp dargestellte vollständige Suchereignis gibt an, dass die erste Suche der Domäne für einen Suchordner abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="1526b-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="1526b-164">Die folgenden Member, die Informationen zum ursprünglichen Objekt enthalten, werden nur in Verschiebungs-und Kopier Ereignissen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1526b-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="1526b-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="1526b-165">**cbOldID**</span></span>
    
- <span data-ttu-id="1526b-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="1526b-166">**lpOldID**</span></span>
    
- <span data-ttu-id="1526b-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="1526b-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="1526b-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="1526b-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="1526b-169">Diese Elemente gelten nicht für die anderen Ereignistypen.</span><span class="sxs-lookup"><span data-stu-id="1526b-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="1526b-170">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="1526b-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="1526b-171">**Thema**</span><span class="sxs-lookup"><span data-stu-id="1526b-171">**Topic**</span></span>|<span data-ttu-id="1526b-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1526b-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1526b-173">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="1526b-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="1526b-174">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="1526b-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="1526b-175">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="1526b-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="1526b-176">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="1526b-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="1526b-177">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1526b-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="1526b-178">Erläuterung, wie Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1526b-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1526b-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1526b-179">See also</span></span>



[<span data-ttu-id="1526b-180">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1526b-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="1526b-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1526b-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="1526b-182">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1526b-182">MAPI Structures</span></span>](mapi-structures.md)


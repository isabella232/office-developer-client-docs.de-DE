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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430168"
---
# <a name="object_notification"></a><span data-ttu-id="c9a72-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c9a72-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c9a72-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9a72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9a72-105">Enthält Informationen zu einem Objekt, das einer Änderung unterzogen wurde, z. B. kopiert oder geändert.</span><span class="sxs-lookup"><span data-stu-id="c9a72-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9a72-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c9a72-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9a72-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9a72-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c9a72-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="c9a72-108">Members</span></span>

 <span data-ttu-id="c9a72-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c9a72-110">Anzahl der Bytes in der Eintrags-ID, auf die das **lpEntryID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c9a72-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c9a72-112">Zeiger auf den Eintragsbezeichner des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9a72-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="c9a72-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="c9a72-113">**ulObjType**</span></span>
  
> <span data-ttu-id="c9a72-114">Typ des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9a72-114">Type of object affected.</span></span> <span data-ttu-id="c9a72-115">Folgende Typen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="c9a72-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="c9a72-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="c9a72-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="c9a72-117">Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c9a72-117">Message store.</span></span> 
    
<span data-ttu-id="c9a72-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="c9a72-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="c9a72-119">Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="c9a72-119">Address book.</span></span> 
    
<span data-ttu-id="c9a72-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c9a72-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="c9a72-121">Folder.</span><span class="sxs-lookup"><span data-stu-id="c9a72-121">Folder.</span></span>
    
<span data-ttu-id="c9a72-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="c9a72-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="c9a72-123">Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="c9a72-123">Address book container.</span></span>
    
<span data-ttu-id="c9a72-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c9a72-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="c9a72-125">Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c9a72-125">Message.</span></span>
    
<span data-ttu-id="c9a72-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="c9a72-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="c9a72-127">Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="c9a72-127">Messaging user.</span></span>
    
<span data-ttu-id="c9a72-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="c9a72-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="c9a72-129">Anlage.</span><span class="sxs-lookup"><span data-stu-id="c9a72-129">Attachment.</span></span>
    
<span data-ttu-id="c9a72-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="c9a72-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="c9a72-131">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="c9a72-131">Distribution list.</span></span>
    
<span data-ttu-id="c9a72-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="c9a72-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="c9a72-133">Abschnitt "Profil".</span><span class="sxs-lookup"><span data-stu-id="c9a72-133">Profile section.</span></span>
    
<span data-ttu-id="c9a72-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="c9a72-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="c9a72-135">Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c9a72-135">Status object.</span></span>
    
<span data-ttu-id="c9a72-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="c9a72-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="c9a72-137">Session-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c9a72-137">Session object.</span></span>
    
 <span data-ttu-id="c9a72-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-138">**cbParentID**</span></span>
  
> <span data-ttu-id="c9a72-139">Anzahl der Bytes in der Eintrags-ID, auf die das **lpParentID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="c9a72-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-140">**lpParentID**</span></span>
  
> <span data-ttu-id="c9a72-141">Zeiger auf den Eintragsbezeichner des übergeordneten Objekts des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9a72-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="c9a72-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-142">**cbOldID**</span></span>
  
> <span data-ttu-id="c9a72-143">Anzahl der Bytes in der Eintrags-ID, auf die das **lpOldID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="c9a72-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-144">**lpOldID**</span></span>
  
> <span data-ttu-id="c9a72-145">Zeiger auf den Eintragsbezeichner des ursprünglichen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9a72-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="c9a72-146">Dieser Zeiger kann NULL sein, wenn für das Ereignis kein ursprüngliches Objekt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c9a72-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="c9a72-148">Anzahl der Bytes in der Eintrags-ID, auf die das **lpOldParentID-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="c9a72-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="c9a72-150">Zeiger auf den Eintragsbezeichner des übergeordneten Objekts des ursprünglichen Objekts.</span><span class="sxs-lookup"><span data-stu-id="c9a72-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="c9a72-151">Dieser Zeiger kann NULL sein, wenn für das Ereignis kein ursprüngliches Objekt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c9a72-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="c9a72-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="c9a72-153">Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die die Eigenschaftstags enthält, die eigenschaften identifizieren, die vom Ereignis betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="c9a72-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9a72-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9a72-154">Remarks</span></span>

<span data-ttu-id="c9a72-155">Die **OBJECT_NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **info-Element** der [NOTIFICATION-Struktur enthalten](notification.md) ist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c9a72-156">Wenn das **Infom** member einer **NOTIFICATION-Struktur** eine OBJECT_NOTIFICATION **enthält,** wird das **ulEventType-Element** der **NOTIFICATION-Struktur** auf einen der folgenden Ereignistypen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c9a72-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="c9a72-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="c9a72-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="c9a72-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="c9a72-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="c9a72-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="c9a72-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="c9a72-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="c9a72-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="c9a72-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="c9a72-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="c9a72-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="c9a72-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="c9a72-163">Das vollständige Suchereignis, dargestellt durch den fnevSearchComplete-Ereignistyp, gibt an, dass die anfängliche Suche der Domäne nach einem Suchordner abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c9a72-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="c9a72-164">Die folgenden Elemente, die Informationen zum ursprünglichen Objekt enthalten, werden nur in Move- und Copy-Ereignissen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9a72-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="c9a72-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-165">**cbOldID**</span></span>
    
- <span data-ttu-id="c9a72-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-166">**lpOldID**</span></span>
    
- <span data-ttu-id="c9a72-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="c9a72-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c9a72-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="c9a72-169">Diese Elemente gelten nicht für die anderen Ereignistypen.</span><span class="sxs-lookup"><span data-stu-id="c9a72-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="c9a72-170">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="c9a72-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c9a72-171">**Thema**</span><span class="sxs-lookup"><span data-stu-id="c9a72-171">**Topic**</span></span>|<span data-ttu-id="c9a72-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9a72-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9a72-173">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="c9a72-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c9a72-174">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="c9a72-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c9a72-175">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c9a72-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c9a72-176">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="c9a72-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c9a72-177">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c9a72-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c9a72-178">Hier erfahren Sie, wie Dienstanbieter die [IMAPISupport-Methode](imapisupportiunknown.md) zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c9a72-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9a72-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9a72-179">See also</span></span>



[<span data-ttu-id="c9a72-180">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c9a72-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c9a72-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c9a72-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="c9a72-182">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c9a72-182">MAPI Structures</span></span>](mapi-structures.md)


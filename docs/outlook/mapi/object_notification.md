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
ms.openlocfilehash: 1593152786a3345827089e5f6702454896944b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793299"
---
# <a name="objectnotification"></a><span data-ttu-id="c69fd-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c69fd-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c69fd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c69fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c69fd-105">Enthält Informationen zu einem Objekt, die eine Änderung unterzogen, z. B. wird kopiert oder geändert.</span><span class="sxs-lookup"><span data-stu-id="c69fd-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c69fd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c69fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="c69fd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c69fd-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c69fd-108">Members</span><span class="sxs-lookup"><span data-stu-id="c69fd-108">Members</span></span>

 <span data-ttu-id="c69fd-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c69fd-110">Anzahl der Bytes in die Eintrags-ID auf den Member **LpEntryID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c69fd-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c69fd-112">Zeiger auf die Eintrags-ID des betroffenen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c69fd-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="c69fd-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="c69fd-113">**ulObjType**</span></span>
  
> <span data-ttu-id="c69fd-114">Typ des Objekts betroffen.</span><span class="sxs-lookup"><span data-stu-id="c69fd-114">Type of object affected.</span></span> <span data-ttu-id="c69fd-115">Verfügbare Typen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c69fd-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="c69fd-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="c69fd-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="c69fd-117">Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c69fd-117">Message store.</span></span> 
    
<span data-ttu-id="c69fd-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="c69fd-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="c69fd-119">Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="c69fd-119">Address book.</span></span> 
    
<span data-ttu-id="c69fd-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c69fd-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="c69fd-121">Ordner.</span><span class="sxs-lookup"><span data-stu-id="c69fd-121">Folder.</span></span>
    
<span data-ttu-id="c69fd-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="c69fd-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="c69fd-123">Adressbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="c69fd-123">Address book container.</span></span>
    
<span data-ttu-id="c69fd-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c69fd-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="c69fd-125">Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c69fd-125">Message.</span></span>
    
<span data-ttu-id="c69fd-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="c69fd-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="c69fd-127">Messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c69fd-127">Messaging user.</span></span>
    
<span data-ttu-id="c69fd-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="c69fd-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="c69fd-129">Attachment-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-129">Attachment.</span></span>
    
<span data-ttu-id="c69fd-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="c69fd-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="c69fd-131">Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="c69fd-131">Distribution list.</span></span>
    
<span data-ttu-id="c69fd-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="c69fd-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="c69fd-133">Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-133">Profile section.</span></span>
    
<span data-ttu-id="c69fd-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="c69fd-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="c69fd-135">Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-135">Status object.</span></span>
    
<span data-ttu-id="c69fd-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="c69fd-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="c69fd-137">Session-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-137">Session object.</span></span>
    
 <span data-ttu-id="c69fd-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-138">**cbParentID**</span></span>
  
> <span data-ttu-id="c69fd-139">Anzahl der Bytes in die Eintrags-ID auf den Member **LpParentID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="c69fd-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-140">**lpParentID**</span></span>
  
> <span data-ttu-id="c69fd-141">Zeiger auf die Eintrags-ID des übergeordneten Elements des betroffenen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c69fd-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="c69fd-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-142">**cbOldID**</span></span>
  
> <span data-ttu-id="c69fd-143">Anzahl der Bytes in die Eintrags-ID auf den Member **LpOldID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="c69fd-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-144">**lpOldID**</span></span>
  
> <span data-ttu-id="c69fd-145">Zeiger auf die Eintrags-ID des ursprünglichen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c69fd-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="c69fd-146">Wenn das Ereignis ursprüngliche-Objekt nicht erforderlich sind, kann dieser Zeiger NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c69fd-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c69fd-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="c69fd-148">Anzahl der Bytes in die Eintrags-ID auf den Member **LpOldParentID** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c69fd-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="c69fd-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="c69fd-150">Zeiger auf die Eintrags-ID des übergeordneten Elements des ursprünglichen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c69fd-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="c69fd-151">Wenn das Ereignis ursprüngliche-Objekt nicht erforderlich sind, kann dieser Zeiger NULL sein.</span><span class="sxs-lookup"><span data-stu-id="c69fd-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c69fd-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="c69fd-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="c69fd-153">Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die die Eigenschaft enthält tags identifizierende Eigenschaften, die von dem Ereignis betroffen.</span><span class="sxs-lookup"><span data-stu-id="c69fd-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c69fd-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c69fd-154">Remarks</span></span>

<span data-ttu-id="c69fd-155">Die **OBJECT_NOTIFICATION** -Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c69fd-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c69fd-156">Wenn der Member **Info** eine **Benachrichtigung** Struktur eine **OBJECT_NOTIFICATION** -Struktur enthält, wird das **UlEventType** Mitglied der **Benachrichtigung** Struktur auf eine der folgenden Arten von Ereignissen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c69fd-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="c69fd-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="c69fd-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="c69fd-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="c69fd-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="c69fd-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="c69fd-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="c69fd-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="c69fd-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="c69fd-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="c69fd-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="c69fd-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="c69fd-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="c69fd-163">Das Search-complete-Ereignis, dargestellt durch den Ereignistyp FnevSearchComplete gibt an, dass die erste Suche der Domäne für ein Suchordner abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c69fd-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="c69fd-164">Die folgenden Elemente, die Informationen zum ursprünglichen-Objekt enthalten sind nur in verschieben und kopieren Ereignisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="c69fd-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="c69fd-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-165">**cbOldID**</span></span>
    
- <span data-ttu-id="c69fd-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-166">**lpOldID**</span></span>
    
- <span data-ttu-id="c69fd-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="c69fd-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c69fd-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="c69fd-169">Dieser Member gelten nicht für andere Arten von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c69fd-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="c69fd-170">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c69fd-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c69fd-171">**Thema**</span><span class="sxs-lookup"><span data-stu-id="c69fd-171">**Topic**</span></span>|<span data-ttu-id="c69fd-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c69fd-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c69fd-173">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="c69fd-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c69fd-174">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="c69fd-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c69fd-175">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c69fd-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c69fd-176">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c69fd-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c69fd-177">Benachrichtigung bei unterstützenden</span><span class="sxs-lookup"><span data-stu-id="c69fd-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c69fd-178">Erläuterung der wie-Dienstanbieter die [IMAPISupport](imapisupportiunknown.md) -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c69fd-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c69fd-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c69fd-179">See also</span></span>



[<span data-ttu-id="c69fd-180">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c69fd-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c69fd-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c69fd-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="c69fd-182">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c69fd-182">MAPI Structures</span></span>](mapi-structures.md)


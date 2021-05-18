---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422327"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="bf91e-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bf91e-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="bf91e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf91e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf91e-105">Bietet Zugriff auf Nachrichtenspeicherinformationen sowie auf Nachrichten und Ordner.</span><span class="sxs-lookup"><span data-stu-id="bf91e-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf91e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bf91e-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf91e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf91e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bf91e-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="bf91e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bf91e-109">Message store-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf91e-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="bf91e-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="bf91e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bf91e-111">Anbieter von Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="bf91e-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="bf91e-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="bf91e-112">Called by:</span></span>  <br/> |<span data-ttu-id="bf91e-113">Clientanwendungen, mapi-Spooler und MAPI</span><span class="sxs-lookup"><span data-stu-id="bf91e-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="bf91e-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="bf91e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bf91e-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="bf91e-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="bf91e-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="bf91e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bf91e-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="bf91e-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="bf91e-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="bf91e-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="bf91e-119">Nichttransaktioniert</span><span class="sxs-lookup"><span data-stu-id="bf91e-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bf91e-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="bf91e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bf91e-121">Raten</span><span class="sxs-lookup"><span data-stu-id="bf91e-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="bf91e-122">Registriert, um Benachrichtigungen über angegebene Ereignisse zu erhalten, die sich auf den Nachrichtenspeicher auswirken.</span><span class="sxs-lookup"><span data-stu-id="bf91e-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="bf91e-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="bf91e-124">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMsgStore::Advise-Methode eingerichtet** wurden.</span><span class="sxs-lookup"><span data-stu-id="bf91e-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="bf91e-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="bf91e-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf denselben Eintrag in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="bf91e-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="bf91e-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="bf91e-128">Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="bf91e-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="bf91e-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="bf91e-130">Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.</span><span class="sxs-lookup"><span data-stu-id="bf91e-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="bf91e-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="bf91e-132">Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als Standard-Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf91e-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="bf91e-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="bf91e-134">Bietet Zugriff auf die Tabelle "Empfangsordner", eine Tabelle mit Informationen zu allen Empfangsordnern für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="bf91e-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="bf91e-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="bf91e-136">Aktiviert die geordnete Abmeldung des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="bf91e-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="bf91e-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="bf91e-138">Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bf91e-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="bf91e-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="bf91e-140">Bietet Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="bf91e-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="bf91e-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="bf91e-142">Sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bf91e-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="bf91e-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="bf91e-144">Ermöglicht dem Nachrichtenspeicheranbieter die Verarbeitung einer gesendeten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bf91e-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="bf91e-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="bf91e-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="bf91e-146">Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="bf91e-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="bf91e-147">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="bf91e-147">**Required properties**</span></span>|<span data-ttu-id="bf91e-148">**Zugriffsebene**</span><span class="sxs-lookup"><span data-stu-id="bf91e-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf91e-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bf91e-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="bf91e-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="bf91e-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="bf91e-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="bf91e-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="bf91e-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="bf91e-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-162">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="bf91e-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bf91e-164">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf91e-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="bf91e-165">Die folgenden Eigenschaften sind für Zwischenperson Message (IPM)-Nachrichtenspeicher:</span><span class="sxs-lookup"><span data-stu-id="bf91e-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="bf91e-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bf91e-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bf91e-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bf91e-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bf91e-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bf91e-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="bf91e-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="bf91e-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="bf91e-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf91e-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf91e-172">See also</span></span>



[<span data-ttu-id="bf91e-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf91e-173">MAPI Properties</span></span>](mapi-properties.md)


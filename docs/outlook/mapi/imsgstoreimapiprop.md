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
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="972d2-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="972d2-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="972d2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="972d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="972d2-105">Ermöglicht den Zugriff auf Nachrichtenspeicher Informationen und für Nachrichten und Ordner.</span><span class="sxs-lookup"><span data-stu-id="972d2-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="972d2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="972d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="972d2-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="972d2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="972d2-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="972d2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="972d2-109">Nachrichtenspeicherobjekt</span><span class="sxs-lookup"><span data-stu-id="972d2-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="972d2-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="972d2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="972d2-111">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="972d2-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="972d2-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="972d2-112">Called by:</span></span>  <br/> |<span data-ttu-id="972d2-113">Client Anwendungen, MAPI-Spooler und MAPI</span><span class="sxs-lookup"><span data-stu-id="972d2-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="972d2-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="972d2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="972d2-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="972d2-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="972d2-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="972d2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="972d2-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="972d2-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="972d2-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="972d2-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="972d2-119">Nicht durchgeführten</span><span class="sxs-lookup"><span data-stu-id="972d2-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="972d2-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="972d2-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="972d2-121">Beraten</span><span class="sxs-lookup"><span data-stu-id="972d2-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="972d2-122">Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf den Nachrichtenspeicher auswirken.</span><span class="sxs-lookup"><span data-stu-id="972d2-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="972d2-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="972d2-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="972d2-124">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMsgStore:: Advise** -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="972d2-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="972d2-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="972d2-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="972d2-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf den gleichen Eintrag in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="972d2-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="972d2-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="972d2-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="972d2-128">Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="972d2-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="972d2-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="972d2-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="972d2-130">Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.</span><span class="sxs-lookup"><span data-stu-id="972d2-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="972d2-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="972d2-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="972d2-132">Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als standardmäßiger Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="972d2-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="972d2-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="972d2-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="972d2-134">Ermöglicht den Zugriff auf die Tabelle Receive Folder, eine Tabelle mit Informationen zu allen Empfangs Ordnern für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="972d2-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="972d2-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="972d2-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="972d2-136">Aktiviert die ordnungsgemäße Abmeldung des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="972d2-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="972d2-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="972d2-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="972d2-138">Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="972d2-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="972d2-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="972d2-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="972d2-140">Ermöglicht den Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="972d2-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="972d2-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="972d2-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="972d2-142">Sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="972d2-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="972d2-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="972d2-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="972d2-144">Ermöglicht dem Nachrichtenspeicher Anbieter das Ausführen der Verarbeitung für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="972d2-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="972d2-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="972d2-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="972d2-146">Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="972d2-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="972d2-147">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="972d2-147">**Required properties**</span></span>|<span data-ttu-id="972d2-148">**Zugriffsebene**</span><span class="sxs-lookup"><span data-stu-id="972d2-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="972d2-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="972d2-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="972d2-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="972d2-153">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="972d2-155">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="972d2-157">**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="972d2-159">**PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="972d2-161">**PR_MDB_PROVIDER** ([Pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-162">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="972d2-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="972d2-164">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="972d2-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="972d2-165">Die folgenden Eigenschaften sind für Nachrichtenspeicher zwischen Personen Nachrichten (IPM):</span><span class="sxs-lookup"><span data-stu-id="972d2-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="972d2-166">**PR_IPM_OUTBOX_ENTRYID** ([Pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="972d2-167">**PR_IPM_SENTMAIL_ENTRYID** ([Pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="972d2-168">**PR_IPM_SUBTREE_ENTRYID** ([Pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="972d2-169">**PR_IPM_WASTEBASKET_ENTRYID** ([Pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="972d2-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="972d2-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="972d2-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="972d2-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="972d2-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="972d2-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="972d2-172">See also</span></span>



[<span data-ttu-id="972d2-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="972d2-173">MAPI Properties</span></span>](mapi-properties.md)


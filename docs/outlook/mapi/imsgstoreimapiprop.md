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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348720"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="8b695-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8b695-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="8b695-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b695-105">Ermöglicht den Zugriff auf Nachrichtenspeicher Informationen und für Nachrichten und Ordner.</span><span class="sxs-lookup"><span data-stu-id="8b695-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b695-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8b695-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b695-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8b695-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8b695-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="8b695-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8b695-109">Nachrichtenspeicherobjekt</span><span class="sxs-lookup"><span data-stu-id="8b695-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="8b695-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8b695-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8b695-111">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b695-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="8b695-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8b695-112">Called by:</span></span>  <br/> |<span data-ttu-id="8b695-113">Client Anwendungen, MAPI-Spooler und MAPI</span><span class="sxs-lookup"><span data-stu-id="8b695-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="8b695-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8b695-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8b695-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="8b695-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="8b695-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="8b695-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8b695-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="8b695-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="8b695-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="8b695-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="8b695-119">Nicht durchgeführten</span><span class="sxs-lookup"><span data-stu-id="8b695-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8b695-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="8b695-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8b695-121">Beraten</span><span class="sxs-lookup"><span data-stu-id="8b695-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="8b695-122">Registriert die Benachrichtigung über angegebene Ereignisse, die sich auf den Nachrichtenspeicher auswirken.</span><span class="sxs-lookup"><span data-stu-id="8b695-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="8b695-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="8b695-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="8b695-124">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **IMsgStore:: Advise** -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="8b695-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="8b695-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8b695-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="8b695-126">Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf den gleichen Eintrag in einem Nachrichtenspeicher verweisen.</span><span class="sxs-lookup"><span data-stu-id="8b695-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="8b695-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8b695-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="8b695-128">Öffnet einen Ordner oder eine Nachricht und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="8b695-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="8b695-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="8b695-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="8b695-130">Richtet einen Ordner als Ziel für eingehende Nachrichten einer bestimmten Nachrichtenklasse ein.</span><span class="sxs-lookup"><span data-stu-id="8b695-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="8b695-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="8b695-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="8b695-132">Ruft den Ordner ab, der als Ziel für eingehende Nachrichten einer angegebenen Nachrichtenklasse oder als standardmäßiger Empfangsordner für den Nachrichtenspeicher eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="8b695-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="8b695-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="8b695-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="8b695-134">Ermöglicht den Zugriff auf die Tabelle Receive Folder, eine Tabelle mit Informationen zu allen Empfangs Ordnern für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8b695-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="8b695-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="8b695-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="8b695-136">Aktiviert die ordnungsgemäße Abmeldung des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="8b695-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="8b695-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="8b695-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="8b695-138">Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8b695-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="8b695-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="8b695-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="8b695-140">Ermöglicht den Zugriff auf die Tabelle für ausgehende Warteschlangen, eine Tabelle mit Informationen zu allen Nachrichten in der ausgehenden Warteschlange des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="8b695-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="8b695-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="8b695-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="8b695-142">Sperrt oder entsperrt eine Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8b695-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="8b695-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="8b695-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="8b695-144">Ermöglicht dem Nachrichtenspeicher Anbieter das Ausführen der Verarbeitung für eine gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8b695-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="8b695-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="8b695-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="8b695-146">Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="8b695-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="8b695-147">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="8b695-147">**Required properties**</span></span>|<span data-ttu-id="8b695-148">**Zugriffsebene**</span><span class="sxs-lookup"><span data-stu-id="8b695-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b695-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b695-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="8b695-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="8b695-153">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="8b695-155">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="8b695-157">**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="8b695-159">**PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="8b695-161">**PR_MDB_PROVIDER** ([Pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-162">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="8b695-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8b695-164">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b695-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="8b695-165">Die folgenden Eigenschaften sind für Nachrichtenspeicher zwischen Personen Nachrichten (IPM):</span><span class="sxs-lookup"><span data-stu-id="8b695-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="8b695-166">**PR_IPM_OUTBOX_ENTRYID** ([Pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="8b695-167">**PR_IPM_SENTMAIL_ENTRYID** ([Pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="8b695-168">**PR_IPM_SUBTREE_ENTRYID** ([Pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="8b695-169">**PR_IPM_WASTEBASKET_ENTRYID** ([Pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8b695-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="8b695-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="8b695-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="8b695-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="8b695-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b695-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b695-172">See also</span></span>



[<span data-ttu-id="8b695-173">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b695-173">MAPI Properties</span></span>](mapi-properties.md)


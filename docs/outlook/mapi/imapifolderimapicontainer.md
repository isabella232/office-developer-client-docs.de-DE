---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1886987515f3cafe38418960baa4b6fd89e3b6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590799"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="0bd41-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0bd41-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="0bd41-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bd41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bd41-105">Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="0bd41-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bd41-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0bd41-106">Header file:</span></span>  <br/> |<span data-ttu-id="0bd41-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bd41-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0bd41-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="0bd41-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0bd41-109">Folder-Objekten</span><span class="sxs-lookup"><span data-stu-id="0bd41-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="0bd41-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0bd41-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0bd41-111">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="0bd41-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="0bd41-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0bd41-112">Called by:</span></span>  <br/> |<span data-ttu-id="0bd41-113">Clientanwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="0bd41-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="0bd41-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="0bd41-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0bd41-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="0bd41-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="0bd41-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="0bd41-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0bd41-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="0bd41-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="0bd41-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="0bd41-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="0bd41-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="0bd41-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0bd41-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="0bd41-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0bd41-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="0bd41-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="0bd41-122">Erstellt eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="0bd41-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="0bd41-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="0bd41-124">Kopiert oder verschiebt eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="0bd41-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="0bd41-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="0bd41-126">Löscht eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="0bd41-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="0bd41-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="0bd41-128">Erstellt einen neuen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="0bd41-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0bd41-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="0bd41-130">Kopiert oder Verschiebt einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="0bd41-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="0bd41-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="0bd41-132">Löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="0bd41-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="0bd41-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="0bd41-134">Legt fest oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) von einem oder mehreren der Nachrichten, die den Ordner und das Senden von lesen Berichte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0bd41-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0bd41-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="0bd41-136">Ruft den Status einer Nachricht in einem bestimmten Ordner an.</span><span class="sxs-lookup"><span data-stu-id="0bd41-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0bd41-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="0bd41-138">Setzt den Status einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0bd41-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="0bd41-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="0bd41-140">Legt die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle fest.</span><span class="sxs-lookup"><span data-stu-id="0bd41-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="0bd41-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="0bd41-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="0bd41-142">Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst löschen.</span><span class="sxs-lookup"><span data-stu-id="0bd41-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="0bd41-143">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="0bd41-143">**Required properties**</span></span>|<span data-ttu-id="0bd41-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="0bd41-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0bd41-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-146">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="0bd41-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="0bd41-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-148">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bd41-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="0bd41-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-150">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="0bd41-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="0bd41-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-152">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bd41-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="0bd41-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-154">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bd41-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="0bd41-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-156">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bd41-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="0bd41-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-158">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bd41-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="0bd41-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0bd41-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0bd41-160">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bd41-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bd41-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bd41-161">See also</span></span>



[<span data-ttu-id="0bd41-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0bd41-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


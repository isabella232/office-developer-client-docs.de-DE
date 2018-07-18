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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792131"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="6d9b3-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6d9b3-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="6d9b3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d9b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d9b3-105">Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d9b3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6d9b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="6d9b3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d9b3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6d9b3-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="6d9b3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6d9b3-109">Folder-Objekten</span><span class="sxs-lookup"><span data-stu-id="6d9b3-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="6d9b3-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6d9b3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6d9b3-111">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6d9b3-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="6d9b3-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6d9b3-112">Called by:</span></span>  <br/> |<span data-ttu-id="6d9b3-113">Clientanwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="6d9b3-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="6d9b3-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6d9b3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6d9b3-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="6d9b3-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="6d9b3-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="6d9b3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6d9b3-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="6d9b3-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="6d9b3-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="6d9b3-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="6d9b3-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="6d9b3-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6d9b3-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6d9b3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6d9b3-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="6d9b3-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="6d9b3-122">Erstellt eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="6d9b3-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="6d9b3-124">Kopiert oder verschiebt eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="6d9b3-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="6d9b3-126">Löscht eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="6d9b3-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="6d9b3-128">Erstellt einen neuen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="6d9b3-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="6d9b3-130">Kopiert oder Verschiebt einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="6d9b3-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="6d9b3-132">Löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="6d9b3-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="6d9b3-134">Legt fest oder löscht das Flag MSGFLAG_READ in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) von einem oder mehreren der Nachrichten, die den Ordner und das Senden von lesen Berichte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="6d9b3-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="6d9b3-136">Ruft den Status einer Nachricht in einem bestimmten Ordner an.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="6d9b3-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="6d9b3-138">Setzt den Status einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="6d9b3-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="6d9b3-140">Legt die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle fest.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="6d9b3-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="6d9b3-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="6d9b3-142">Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst löschen.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="6d9b3-143">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="6d9b3-143">**Required properties**</span></span>|<span data-ttu-id="6d9b3-144">**Zugriff**</span><span class="sxs-lookup"><span data-stu-id="6d9b3-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d9b3-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-146">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="6d9b3-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="6d9b3-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-148">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="6d9b3-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-150">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="6d9b3-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="6d9b3-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-152">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="6d9b3-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-154">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="6d9b3-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-156">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="6d9b3-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-158">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="6d9b3-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d9b3-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d9b3-160">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d9b3-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d9b3-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d9b3-161">See also</span></span>



[<span data-ttu-id="6d9b3-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6d9b3-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


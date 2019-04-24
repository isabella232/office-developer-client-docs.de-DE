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
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329491"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="f86b2-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f86b2-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="f86b2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f86b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f86b2-105">Führt Vorgänge für die Nachrichten und Unterordner in einem Ordner aus.</span><span class="sxs-lookup"><span data-stu-id="f86b2-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f86b2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f86b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="f86b2-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f86b2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f86b2-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="f86b2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f86b2-109">Folder-Objekte</span><span class="sxs-lookup"><span data-stu-id="f86b2-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="f86b2-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f86b2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f86b2-111">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="f86b2-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="f86b2-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f86b2-112">Called by:</span></span>  <br/> |<span data-ttu-id="f86b2-113">Client Anwendungen und MAPI</span><span class="sxs-lookup"><span data-stu-id="f86b2-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="f86b2-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="f86b2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f86b2-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="f86b2-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="f86b2-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="f86b2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f86b2-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="f86b2-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="f86b2-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="f86b2-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="f86b2-119">Nicht durchgeführten</span><span class="sxs-lookup"><span data-stu-id="f86b2-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f86b2-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="f86b2-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f86b2-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="f86b2-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="f86b2-122">Erstellt eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f86b2-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f86b2-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="f86b2-124">Kopiert oder verschiebt eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f86b2-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="f86b2-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="f86b2-126">Löscht eine oder mehrere Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f86b2-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="f86b2-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="f86b2-128">Erstellt einen neuen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="f86b2-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f86b2-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="f86b2-130">Kopiert oder verschiebt einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="f86b2-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="f86b2-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="f86b2-132">Löscht einen Unterordner.</span><span class="sxs-lookup"><span data-stu-id="f86b2-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="f86b2-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="f86b2-134">Legt das MSGFLAG_READ-flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft einer oder mehrerer der Nachrichten des Ordners fest oder löscht das Senden von Lese Berichten.</span><span class="sxs-lookup"><span data-stu-id="f86b2-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="f86b2-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="f86b2-136">Ruft den Status ab, der einer Nachricht in einem bestimmten Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f86b2-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="f86b2-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="f86b2-138">Legt den Status fest, der einer Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f86b2-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="f86b2-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="f86b2-140">Legt die Standardsortierreihenfolge für die Inhaltstabelle eines Ordners fest.</span><span class="sxs-lookup"><span data-stu-id="f86b2-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="f86b2-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="f86b2-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="f86b2-142">Löscht alle Nachrichten und Unterordner aus einem Ordner, ohne den Ordner selbst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f86b2-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="f86b2-143">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="f86b2-143">**Required properties**</span></span>|<span data-ttu-id="f86b2-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="f86b2-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f86b2-145">**PR_DISPLAY_NAME** ([Pidtagdisplaynameprefix (](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f86b2-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="f86b2-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86b2-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="f86b2-149">**PR_FOLDER_TYPE** ([Pidtagfoldertype (](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-150">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f86b2-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="f86b2-151">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86b2-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="f86b2-153">**PR_PARENT_ENTRYID** ([Pidtagparententryid (](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-154">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86b2-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="f86b2-155">**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86b2-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="f86b2-157">**PR_STORE_ENTRYID** ([Pidtagstoreentryid (](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86b2-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="f86b2-159">**PR_STORE_RECORD_KEY** ([Pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f86b2-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f86b2-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f86b2-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f86b2-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f86b2-161">See also</span></span>



[<span data-ttu-id="f86b2-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f86b2-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


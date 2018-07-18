---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bac363183c15a2d53c15b46724266b6cb5744075
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792113"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="87040-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="87040-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="87040-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87040-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87040-105">Ruft den Status einer Nachricht in einem bestimmten Ordner zugeordnet, (z. B., ob die Nachricht zum Löschen markiert ist).</span><span class="sxs-lookup"><span data-stu-id="87040-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="87040-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87040-106">Parameters</span></span>

 <span data-ttu-id="87040-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="87040-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="87040-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="87040-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="87040-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="87040-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="87040-110">[in] Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="87040-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="87040-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87040-111">_ulFlags_</span></span>
  
> <span data-ttu-id="87040-112">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="87040-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="87040-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="87040-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="87040-114">[out] Ein Zeiger auf einen Zeiger auf eine Bitmaske aus Flags, die die Nachricht Status angeben.</span><span class="sxs-lookup"><span data-stu-id="87040-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="87040-115">Bits 0 bis 15 sind reserviert und müssen null sein. 16 bis 31 Bits sind für die Verwendung von implementierungsspezifischen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="87040-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="87040-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="87040-116">The following flags can be set:</span></span>
    
<span data-ttu-id="87040-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="87040-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="87040-118">Die Nachricht wurde zum Löschen markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="87040-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="87040-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="87040-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="87040-120">Die Nachricht wird nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="87040-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="87040-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="87040-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="87040-122">Die Nachricht anzuzeigen ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="87040-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="87040-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="87040-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="87040-124">Die Nachricht wurde zum Löschen auf die entfernten Nachrichtenspeicher markiert, ohne dass auf dem lokalen Client heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="87040-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="87040-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="87040-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="87040-126">Die Nachricht wurde für das Herunterladen aus dem remote Nachrichtenspeicher auf dem lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="87040-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="87040-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="87040-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="87040-128">Für einen Client definierten Zweck hat die Nachricht markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="87040-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87040-129">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="87040-129">Return value</span></span>

<span data-ttu-id="87040-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="87040-130">S_OK</span></span> 
  
> <span data-ttu-id="87040-131">Die Nachricht den Status wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="87040-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87040-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87040-132">Remarks</span></span>

<span data-ttu-id="87040-133">Die **IMAPIFolder::GetMessageStatus** -Methode gibt den Status einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="87040-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="87040-134">Nachrichtenstatus wird in der Nachricht **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87040-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="87040-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="87040-135">Notes to implementers</span></span>

<span data-ttu-id="87040-136">Wie die Nachricht Statusbits festgelegt, gelöscht und verwendet werden, hängt vollständig die Implementierung mit der Ausnahme, dass Bits 0 bis 15 reserviert sind und müssen null sein.</span><span class="sxs-lookup"><span data-stu-id="87040-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="87040-137">Wenn Sie Nachrichten in der IPM-Unterstruktur speichern, reserviert MAPI Bits 16 bis 31 für die Verwendung durch Clients IPM.</span><span class="sxs-lookup"><span data-stu-id="87040-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="87040-138">Wenn Sie Nachrichten in anderen Unterstrukturen speichern, können Sie Bits 16 bis 31 für eigene Zwecke.</span><span class="sxs-lookup"><span data-stu-id="87040-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87040-139">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="87040-139">MFCMAPI reference</span></span>

<span data-ttu-id="87040-140">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="87040-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87040-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="87040-141">**File**</span></span>|<span data-ttu-id="87040-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="87040-142">**Function**</span></span>|<span data-ttu-id="87040-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="87040-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87040-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="87040-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="87040-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="87040-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="87040-146">MFCMAPI (engl.) verwendet die **IMAPIFolder::GetMessageStatus** -Methode, um den Status der nächsten Nachricht anzuzeigende abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87040-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="87040-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="87040-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="87040-148">OpenMessageNonModal und OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="87040-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="87040-149">MFCMAPI (engl.) verwendet die **IMAPIFolder::GetMessageStatus** -Methode zum Abrufen des Status der Nachricht angezeigt werden, für den Betrachter Formular zu übergeben, CMyMAPIFormViewer oder [IMAPISession::ShowForm](imapisession-showform.md)ist.</span><span class="sxs-lookup"><span data-stu-id="87040-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87040-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87040-150">See also</span></span>



[<span data-ttu-id="87040-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="87040-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="87040-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="87040-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="87040-153">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="87040-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="87040-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="87040-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="87040-155">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="87040-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


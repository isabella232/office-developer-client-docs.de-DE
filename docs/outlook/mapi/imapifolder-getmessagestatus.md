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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418638"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="cdebb-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="cdebb-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="cdebb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdebb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdebb-105">Ruft den Status ab, der einer Nachricht in einem bestimmten Ordner zugeordnet ist (beispielsweise, ob diese Nachricht zum Löschen markiert ist).</span><span class="sxs-lookup"><span data-stu-id="cdebb-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="cdebb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdebb-106">Parameters</span></span>

 <span data-ttu-id="cdebb-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="cdebb-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="cdebb-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cdebb-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="cdebb-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="cdebb-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="cdebb-110">in Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cdebb-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="cdebb-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cdebb-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cdebb-112">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="cdebb-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cdebb-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="cdebb-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="cdebb-114">Out Ein Zeiger auf einen Zeiger auf eine Bitmaske von Flags, die den Status der Nachricht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cdebb-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="cdebb-115">Die Bits 0 bis 15 sind reserviert und müssen NULL sein; Bits 16 bis 31 sind für die implementierungsspezifische Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cdebb-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="cdebb-116">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cdebb-116">The following flags can be set:</span></span>
    
<span data-ttu-id="cdebb-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="cdebb-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="cdebb-118">Die Nachricht wurde zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="cdebb-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="cdebb-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="cdebb-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="cdebb-120">Die Nachricht soll nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cdebb-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="cdebb-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="cdebb-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="cdebb-122">Die Nachricht wird hervorgehoben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdebb-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="cdebb-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="cdebb-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="cdebb-124">Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher markiert, ohne Sie auf den lokalen Client herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="cdebb-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="cdebb-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="cdebb-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="cdebb-126">Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="cdebb-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="cdebb-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="cdebb-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="cdebb-128">Die Nachricht wurde für einen Client definierten Zweck markiert.</span><span class="sxs-lookup"><span data-stu-id="cdebb-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cdebb-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdebb-129">Return value</span></span>

<span data-ttu-id="cdebb-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdebb-130">S_OK</span></span> 
  
> <span data-ttu-id="cdebb-131">Der Nachrichtenstatus wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cdebb-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cdebb-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdebb-132">Remarks</span></span>

<span data-ttu-id="cdebb-133">Die **IMAPIFolder:: GetMessageStatus** -Methode gibt den Status einer Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="cdebb-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="cdebb-134">Der Nachrichtenstatus wird in der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cdebb-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cdebb-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="cdebb-135">Notes to implementers</span></span>

<span data-ttu-id="cdebb-136">Wie die Nachrichtenstatus-Bits festgelegt, gelöscht und verwendet werden, hängt vollständig von der Implementierung ab, mit der Ausnahme, dass die Bits 0 bis 15 reserviert sind und 0 (null) sein müssen.</span><span class="sxs-lookup"><span data-stu-id="cdebb-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="cdebb-137">Wenn Sie Nachrichten in der IPM-Unterstruktur speichern, werden die Bits 16 bis 31 für die Verwendung durch IPM-Clients reserviert.</span><span class="sxs-lookup"><span data-stu-id="cdebb-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="cdebb-138">Wenn Sie Nachrichten in anderen unter Strukturen speichern, können Sie die Bits 16 bis 31 für eigene Zwecke verwenden.</span><span class="sxs-lookup"><span data-stu-id="cdebb-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cdebb-139">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="cdebb-139">MFCMAPI reference</span></span>

<span data-ttu-id="cdebb-140">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cdebb-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cdebb-141">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cdebb-141">**File**</span></span>|<span data-ttu-id="cdebb-142">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="cdebb-142">**Function**</span></span>|<span data-ttu-id="cdebb-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cdebb-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cdebb-144">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="cdebb-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="cdebb-145">CMyMAPIFormViewer:: GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="cdebb-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="cdebb-146">MFCMAPI verwendet die **IMAPIFolder:: GetMessageStatus** -Methode, um den Status der nächsten Nachricht abzurufen, die angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cdebb-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="cdebb-147">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="cdebb-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cdebb-148">OpenMessageNonModal und OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="cdebb-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="cdebb-149">MFCMAPI verwendet die **IMAPIFolder:: GetMessageStatus** -Methode, um den Status der Meldung anzuzeigen, die an den Formular Betrachter weitergegeben werden soll, der entweder CMyMAPIFormViewer oder [IMAPISession:: ShowForm](imapisession-showform.md)ist.</span><span class="sxs-lookup"><span data-stu-id="cdebb-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdebb-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdebb-150">See also</span></span>



[<span data-ttu-id="cdebb-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="cdebb-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="cdebb-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="cdebb-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="cdebb-153">Kanonische Pidtagmessagestatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cdebb-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="cdebb-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="cdebb-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="cdebb-155">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="cdebb-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


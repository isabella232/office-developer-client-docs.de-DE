---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792630"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="a56c4-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="a56c4-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="a56c4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a56c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a56c4-105">Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a56c4-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a56c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a56c4-106">Parameters</span></span>

 <span data-ttu-id="a56c4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a56c4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a56c4-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a56c4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a56c4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a56c4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a56c4-110">[in] Ein Zeiger auf die Eintrags-ID der Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a56c4-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="a56c4-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a56c4-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a56c4-112">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="a56c4-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a56c4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a56c4-113">Return value</span></span>

<span data-ttu-id="a56c4-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a56c4-114">S_OK</span></span> 
  
> <span data-ttu-id="a56c4-115">Die Nachricht wurde aus der ausgehenden Warteschlange erfolgreich entfernt.</span><span class="sxs-lookup"><span data-stu-id="a56c4-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="a56c4-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="a56c4-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="a56c4-117">Die Nachricht vom _LpEntryID_ ist nicht mehr in der Nachrichtenspeicher ausgehenden Warteschlange, in der Regel, da es bereits gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a56c4-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="a56c4-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="a56c4-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="a56c4-119">Die Nachricht vom _LpEntryID_ gesperrt ist, durch die MAPI-Warteschlange, und der Vorgang kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="a56c4-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a56c4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a56c4-120">Remarks</span></span>

<span data-ttu-id="a56c4-121">Die **IMsgStore::AbortSubmit** -Methode versucht, eine gesendete Nachricht aus dem Nachrichtenspeicher ausgehende Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a56c4-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a56c4-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a56c4-122">Notes to callers</span></span>

<span data-ttu-id="a56c4-123">Nachdem eine Nachricht gesendet wird, ist das Abbrechen der Übermittlung durch Aufrufen von **AbortSubmit** die einzige Aktion, die für die Nachricht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a56c4-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="a56c4-124">Davon ausgehen, dass **AbortSubmit** immer erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a56c4-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="a56c4-125">Je nachdem, wie das zugrunde liegende messaging-System implementiert wird möglicherweise es nicht möglich, das Senden der Nachricht abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="a56c4-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a56c4-126">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="a56c4-126">MFCMAPI reference</span></span>

<span data-ttu-id="a56c4-127">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a56c4-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a56c4-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a56c4-128">**File**</span></span>|<span data-ttu-id="a56c4-129">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a56c4-129">**Function**</span></span>|<span data-ttu-id="a56c4-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a56c4-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a56c4-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a56c4-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="a56c4-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="a56c4-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="a56c4-133">MFCMAPI (engl.) verwendet die **IMsgStore::AbortSubmit** -Methode, um der Übermittlung der ausgewählten Nachricht abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="a56c4-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a56c4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a56c4-134">See also</span></span>



[<span data-ttu-id="a56c4-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a56c4-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="a56c4-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a56c4-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="a56c4-137">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a56c4-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


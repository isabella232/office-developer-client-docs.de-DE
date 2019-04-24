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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348818"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="8a209-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="8a209-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="8a209-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a209-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a209-105">Versucht, eine Nachricht aus der ausgehenden Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8a209-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8a209-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a209-106">Parameters</span></span>

 <span data-ttu-id="8a209-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8a209-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8a209-108">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8a209-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8a209-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8a209-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8a209-110">in Ein Zeiger auf die Eintrags-ID der Nachricht, die aus der ausgehenden Warteschlange entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a209-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="8a209-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a209-111">_ulFlags_</span></span>
  
> <span data-ttu-id="8a209-112">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="8a209-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a209-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a209-113">Return value</span></span>

<span data-ttu-id="8a209-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a209-114">S_OK</span></span> 
  
> <span data-ttu-id="8a209-115">Die Nachricht wurde erfolgreich aus der ausgehenden Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="8a209-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="8a209-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="8a209-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="8a209-117">Die von _lpEntryID_ angegebene Nachricht befindet sich nicht mehr in der ausgehenden Warteschlange des Nachrichtenspeichers, in der Regel, weil Sie bereits gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8a209-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="8a209-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="8a209-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="8a209-119">Die von _lpEntryID_ angegebene Nachricht wird vom MAPI-Spooler gesperrt, und der Vorgang kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="8a209-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8a209-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a209-120">Remarks</span></span>

<span data-ttu-id="8a209-121">Die **IMsgStore:: AbortSubmit** -Methode versucht, eine übermittelte Nachricht aus der ausgehenden Warteschlange des Nachrichtenspeichers zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8a209-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8a209-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8a209-122">Notes to callers</span></span>

<span data-ttu-id="8a209-123">Nachdem eine Nachricht übermittelt wurde, wird die Übermittlung durch Aufrufen von **AbortSubmit** abgebrochen und ist die einzige Aktion, die für die Nachricht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a209-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="8a209-124">Erwarten Sie nicht, dass **AbortSubmit** immer erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8a209-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="8a209-125">Je nachdem, wie das zugrunde liegende Messagingsystem implementiert wird, kann das Senden der Nachricht möglicherweise nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="8a209-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8a209-126">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8a209-126">MFCMAPI reference</span></span>

<span data-ttu-id="8a209-127">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8a209-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8a209-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8a209-128">**File**</span></span>|<span data-ttu-id="8a209-129">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8a209-129">**Function**</span></span>|<span data-ttu-id="8a209-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8a209-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a209-131">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="8a209-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="8a209-132">CFolderDlg:: OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="8a209-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="8a209-133">MFCMAPI verwendet die **IMsgStore:: AbortSubmit** -Methode, um die Übermittlung der ausgewählten Nachricht abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="8a209-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a209-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a209-134">See also</span></span>



[<span data-ttu-id="8a209-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="8a209-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="8a209-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a209-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="8a209-137">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8a209-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


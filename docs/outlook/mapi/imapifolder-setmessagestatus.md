---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fcca6a7e8fa70a2df9042e8b3c2b28825cee9a7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792124"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="1a1b5-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1a1b5-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="1a1b5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a1b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a1b5-105">Setzt den Status einer Nachricht zugeordneten (z. B., ob die Nachricht zum Löschen markiert ist).</span><span class="sxs-lookup"><span data-stu-id="1a1b5-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="1a1b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a1b5-106">Parameters</span></span>

 <span data-ttu-id="1a1b5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1a1b5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="1a1b5-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1a1b5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1a1b5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="1a1b5-110">[in] Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="1a1b5-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="1a1b5-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="1a1b5-112">[in] Der neue Status zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="1a1b5-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="1a1b5-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="1a1b5-114">[in] Eine Bitmaske aus Flags, die auf den neuen Status angewendet wird und der zu protokollierenden festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="1a1b5-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1a1b5-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1a1b5-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="1a1b5-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="1a1b5-117">Die Nachricht wurde zum Löschen markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="1a1b5-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="1a1b5-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="1a1b5-119">Die Nachricht wird nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="1a1b5-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="1a1b5-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="1a1b5-121">Die Nachricht anzuzeigen ist hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="1a1b5-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="1a1b5-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="1a1b5-123">Die Nachricht wurde zum Löschen auf die entfernten Nachrichtenspeicher markiert, ohne dass auf dem lokalen Client heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="1a1b5-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1a1b5-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1a1b5-125">Die Nachricht wurde für das Herunterladen aus dem remote Nachrichtenspeicher auf dem lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="1a1b5-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="1a1b5-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="1a1b5-127">Für einen Client definierten Zweck hat die Nachricht markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="1a1b5-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="1a1b5-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="1a1b5-129">[out] Ein Zeiger auf den vorherigen Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a1b5-130">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1a1b5-130">Return value</span></span>

<span data-ttu-id="1a1b5-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a1b5-131">S_OK</span></span> 
  
> <span data-ttu-id="1a1b5-132">Der Nachrichtenstatus wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a1b5-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a1b5-133">Remarks</span></span>

<span data-ttu-id="1a1b5-134">Die **IMAPIFolder::SetMessageStatus** -Methode wird die Nachricht den Status auf den Wert, der in dessen **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1a1b5-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="1a1b5-135">Notes to implementers</span></span>

<span data-ttu-id="1a1b5-136">Wie die Nachricht Statusbits festgelegt, gelöscht und verwendet werden, hängt vollständig die Implementierung mit der Ausnahme, dass Bits 0 bis 15 reserviert sind und müssen null sein.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="1a1b5-137">Eine remote Adressbuchhierarchie Implementierung dieser Methode muss der hier beschriebenen Semantik folgen.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="1a1b5-138">Es gibt keine besondere Aspekte.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-138">There are no special considerations.</span></span> <span data-ttu-id="1a1b5-139">Clients mit dieser Methode können Sie legen die Bits MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE, um anzugeben, dass eine bestimmte Nachricht wird heruntergeladen oder vom remote Nachrichtenspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="1a1b5-140">Eine remote Adressbuchhierarchie hat keinen implementieren die verwandte [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="1a1b5-141">Clients müssen Suchen in den Ordner Inhaltstabelle zum Bestimmen des Status einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a1b5-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1a1b5-142">Notes to callers</span></span>

<span data-ttu-id="1a1b5-143">Die **PR_MSG_STATUS** -Eigenschaft einer Nachricht können Sie einen Nachricht Sperrung Vorgang mit anderen Clients aushandeln.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="1a1b5-144">Etwas als die Sperrung Bit bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="1a1b5-145">Um zu bestimmen, ob das Sperrung Bit festgelegt wurde, untersuchen Sie den vorherigen Wert für Nachrichtenstatus im _LpulOldStatus_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="1a1b5-146">Verwenden Sie die anderen Bits im _UlNewStatus_ -Parameter Nachrichtenstatus verfolgen, ohne eine Störung der Sperrung Bit.</span><span class="sxs-lookup"><span data-stu-id="1a1b5-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a1b5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a1b5-147">See also</span></span>



[<span data-ttu-id="1a1b5-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1a1b5-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="1a1b5-149">Kanonische PidTagMessageStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a1b5-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="1a1b5-150">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="1a1b5-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


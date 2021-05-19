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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417273"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="72427-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="72427-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="72427-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72427-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72427-105">Legt den Status fest, der einer Nachricht zugeordnet ist (z. B. ob diese Nachricht zum Löschen markiert ist).</span><span class="sxs-lookup"><span data-stu-id="72427-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="72427-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72427-106">Parameters</span></span>

 <span data-ttu-id="72427-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="72427-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="72427-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="72427-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="72427-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="72427-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="72427-110">[in] Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="72427-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="72427-111">_ulNewStatus_</span><span class="sxs-lookup"><span data-stu-id="72427-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="72427-112">[in] Der neue Status, der zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="72427-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="72427-113">_ulNewStatusMask_</span><span class="sxs-lookup"><span data-stu-id="72427-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="72427-114">[in] Eine Bitmaske mit Flags, die auf den neuen Status angewendet wird und die festgelegten Flags angibt.</span><span class="sxs-lookup"><span data-stu-id="72427-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="72427-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="72427-115">The following flags can be set:</span></span>
    
<span data-ttu-id="72427-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="72427-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="72427-117">Die Nachricht wurde zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="72427-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="72427-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="72427-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="72427-119">Die Nachricht soll nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="72427-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="72427-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="72427-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="72427-121">Die Nachricht soll hervorgehoben angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="72427-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="72427-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="72427-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="72427-123">Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher ohne Download auf den lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="72427-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="72427-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="72427-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="72427-125">Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert.</span><span class="sxs-lookup"><span data-stu-id="72427-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="72427-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="72427-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="72427-127">Die Nachricht wurde für einen clientdefinierten Zweck markiert.</span><span class="sxs-lookup"><span data-stu-id="72427-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="72427-128">_lpulOldStatus_</span><span class="sxs-lookup"><span data-stu-id="72427-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="72427-129">[out] Ein Zeiger auf den vorherigen Status der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="72427-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72427-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72427-130">Return value</span></span>

<span data-ttu-id="72427-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="72427-131">S_OK</span></span> 
  
> <span data-ttu-id="72427-132">Der Nachrichtenstatus wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72427-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72427-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72427-133">Remarks</span></span>

<span data-ttu-id="72427-134">Die **IMAPIFolder::SetMessageStatus-Methode** legt den Nachrichtenstatus auf den Wert fest, der in der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) **-Eigenschaft** gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="72427-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="72427-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="72427-135">Notes to implementers</span></span>

<span data-ttu-id="72427-136">Wie die Nachrichtenstatusbits festgelegt, geräumt und verwendet werden, hängt vollständig von Ihrer Implementierung ab, mit der Ausnahme, dass bits 0 bis 15 reserviert sind und null sein müssen.</span><span class="sxs-lookup"><span data-stu-id="72427-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="72427-137">Die Implementierung dieser Methode durch einen Remotetransportanbieter muss der hier beschriebenen Semantik folgen.</span><span class="sxs-lookup"><span data-stu-id="72427-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="72427-138">Es gibt keine besonderen Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="72427-138">There are no special considerations.</span></span> <span data-ttu-id="72427-139">Clients verwenden diese Methode, um die bits MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE anzugeben, dass eine bestimmte Nachricht heruntergeladen oder aus dem Remotenachrichtenspeicher gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="72427-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="72427-140">Ein Remotetransportanbieter muss die zugehörige [IMAPIFolder::GetMessageStatus-Methode](imapifolder-getmessagestatus.md) nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="72427-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="72427-141">Clients müssen in der Inhaltstabelle des Ordners suchen, um den Status einer Nachricht zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="72427-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="72427-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="72427-142">Notes to callers</span></span>

<span data-ttu-id="72427-143">Sie können die **PR_MSG_STATUS** einer Nachricht verwenden, um einen Nachrichtensperrungsvorgang mit anderen Clients auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="72427-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="72427-144">Geben Sie ein Bit als Sperrbit an.</span><span class="sxs-lookup"><span data-stu-id="72427-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="72427-145">Um zu ermitteln, ob das Sperrbit festgelegt wurde, untersuchen Sie den vorherigen Wert für den Nachrichtenstatus im _lpulOldStatus-Parameter._</span><span class="sxs-lookup"><span data-stu-id="72427-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="72427-146">Verwenden Sie die anderen Bits im  _ulNewStatus-Parameter,_ um den Nachrichtenstatus nachverfolgt zu haben, ohne das Sperrbit zu stören.</span><span class="sxs-lookup"><span data-stu-id="72427-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72427-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72427-147">See also</span></span>



[<span data-ttu-id="72427-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="72427-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="72427-149">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="72427-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="72427-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="72427-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


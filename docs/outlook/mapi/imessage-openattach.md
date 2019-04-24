---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349252"
---
# <a name="imessageopenattach"></a><span data-ttu-id="8695e-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="8695e-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="8695e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8695e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8695e-105">Öffnet eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="8695e-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="8695e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8695e-106">Parameters</span></span>

 <span data-ttu-id="8695e-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="8695e-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="8695e-108">in Index Nummer der zu öffnenden Anlage, wie in der **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8695e-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="8695e-109">Diese Indexnummer identifiziert die Anlage in der Nachricht eindeutig und ist nur im Kontext der Nachricht gültig.</span><span class="sxs-lookup"><span data-stu-id="8695e-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="8695e-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8695e-110">_lpInterface_</span></span>
  
> <span data-ttu-id="8695e-111">in Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf die Anlage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8695e-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="8695e-112">Das übergeben von NULL-Ergebnissen in der Standardschnittstelle oder **IAttach**, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8695e-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="8695e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8695e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="8695e-114">in Bitmaske von Flags, die Steuern, wie die Anlage geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8695e-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="8695e-115">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8695e-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="8695e-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8695e-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="8695e-117">Fordert, dass die Anlage mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Zugriff auf Clientanwendungen geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8695e-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="8695e-118">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, muss die Anlage mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützten Zugriff hat, sollte die Anlage mit Lesezugriff geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="8695e-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="8695e-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8695e-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8695e-120">Ermöglicht \*\*\*\* das erfolgreiche zurückgeben von openattach, möglicherweise vor der vollständigen Verfügbarkeit der Anlage für den aufrufenden Client.</span><span class="sxs-lookup"><span data-stu-id="8695e-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="8695e-121">Wenn die Anlage nicht verfügbar ist, kann durch einen nachfolgenden Aufruf eine Fehlermeldung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="8695e-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="8695e-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8695e-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8695e-123">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="8695e-123">Requests read/write permission.</span></span> <span data-ttu-id="8695e-124">Anlagen werden standardmäßig mit schreibgeschütztem Zugriff geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="8695e-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="8695e-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="8695e-125">_lppAttach_</span></span>
  
> <span data-ttu-id="8695e-126">Out Zeiger auf einen Zeiger auf die offene Anlage.</span><span class="sxs-lookup"><span data-stu-id="8695e-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8695e-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8695e-127">Return value</span></span>

<span data-ttu-id="8695e-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="8695e-128">S_OK</span></span> 
  
> <span data-ttu-id="8695e-129">Die Anlage wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8695e-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8695e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8695e-130">Remarks</span></span>

<span data-ttu-id="8695e-131">Die **IMessage:: openattach** -Methode öffnet die Anlage einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8695e-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8695e-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8695e-132">Notes to callers</span></span>

<span data-ttu-id="8695e-133">Zum Öffnen einer Anlage benötigen Sie Zugriff auf die Anlagennummer oder die **PR_ATTACH_NUM** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8695e-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="8695e-134">Rufen Sie [IMessage::](imessage-getattachmenttable.md) getattachmentable auf, um die Attachment-Tabelle der Nachricht abzurufen und die Zeile zu suchen, die die zu öffnende Anlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="8695e-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="8695e-135">Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="8695e-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="8695e-136">Versuchen Sie nicht, eine Anlage mehrmals zu öffnen. die Ergebnisse sind nicht definiert und vom Nachrichtenspeicher Anbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="8695e-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="8695e-137">Anstelle des Standard schreibgeschützten Modus können Sie anfordern, dass die Anlage im Lese-/Schreibzugriff-Modus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8695e-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="8695e-138">Ob die Anlage tatsächlich im Lese-/Schreibzugriff-Modus geöffnet wird, liegt jedoch beim Nachrichtenspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="8695e-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="8695e-139">Sie können entweder versuchen, die Anlage zu ändern, die Behandlung möglicher Ausfälle vorzubereiten oder die Zugriffsebene zu überprüfen, die durch Abrufen der **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft der Anlage gewährt wurde, falls diese verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8695e-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8695e-140">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8695e-140">MFCMAPI reference</span></span>

<span data-ttu-id="8695e-141">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8695e-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8695e-142">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8695e-142">**File**</span></span>|<span data-ttu-id="8695e-143">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8695e-143">**Function**</span></span>|<span data-ttu-id="8695e-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8695e-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8695e-145">AttachmentsDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="8695e-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="8695e-146">CAttachmentsDlg:: OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="8695e-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="8695e-147">MFCMAPI verwendet die **IMessage:: openattach** -Methode zum Öffnen von Attachment-Objekten,</span><span class="sxs-lookup"><span data-stu-id="8695e-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8695e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8695e-148">See also</span></span>



[<span data-ttu-id="8695e-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8695e-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="8695e-150">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8695e-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


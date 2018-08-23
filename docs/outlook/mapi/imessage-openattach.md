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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 48df5362106e849f061b0797736fad82fafa6584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588713"
---
# <a name="imessageopenattach"></a><span data-ttu-id="f556e-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="f556e-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="f556e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f556e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f556e-105">Öffnet eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="f556e-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="f556e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f556e-106">Parameters</span></span>

 <span data-ttu-id="f556e-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="f556e-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="f556e-108">[in] Die Indexnummer der Anlage für das Öffnen, wie in der Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f556e-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="f556e-109">Diese Indexnummer eindeutig identifiziert die Anlage in der Nachricht und ist nur im Kontext der Nachricht gültig.</span><span class="sxs-lookup"><span data-stu-id="f556e-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="f556e-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f556e-110">_lpInterface_</span></span>
  
> <span data-ttu-id="f556e-111">[in] Zeiger auf die Schnittstelle-ID (IID), das die Schnittstelle für den Zugriff auf die Anlage verwendet werden darstellt.</span><span class="sxs-lookup"><span data-stu-id="f556e-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="f556e-112">Bei Übergabe von NULL führt der Anlage Standardschnittstelle oder **IAttach**, zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f556e-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="f556e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f556e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="f556e-114">[in] Bitmaske aus Flags, die steuert, wie die Anlage geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f556e-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="f556e-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f556e-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="f556e-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f556e-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="f556e-117">Fordert an, dass die Anlage mit den maximale Netzwerkberechtigungen für den Benutzer und die maximale Anwendung Clientzugriff zulässig geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f556e-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="f556e-118">Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Attachment-Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client schreibgeschützten Zugriff hat, sollte die Anlage mit schreibgeschützten Zugriff geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f556e-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="f556e-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f556e-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f556e-120">Ermöglicht **OpenAttach** erfolgreich, möglicherweise beendet, bevor die Anlage vollständig an den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f556e-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="f556e-121">Wenn die Anlage nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f556e-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="f556e-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f556e-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f556e-123">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="f556e-123">Requests read/write permission.</span></span> <span data-ttu-id="f556e-124">Standardmäßig werden Anlagen mit schreibgeschützten Zugriff geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="f556e-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="f556e-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="f556e-125">_lppAttach_</span></span>
  
> <span data-ttu-id="f556e-126">[out] Zeiger auf einen Zeiger auf die Anlage öffnen.</span><span class="sxs-lookup"><span data-stu-id="f556e-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f556e-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f556e-127">Return value</span></span>

<span data-ttu-id="f556e-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="f556e-128">S_OK</span></span> 
  
> <span data-ttu-id="f556e-129">Die Anlage wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f556e-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f556e-130">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f556e-130">Remarks</span></span>

<span data-ttu-id="f556e-131">Die **IMessage::OpenAttach** -Methode wird ein e-Mail-Anlage geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f556e-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f556e-132">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f556e-132">Notes to callers</span></span>

<span data-ttu-id="f556e-133">Um eine Anlage zu öffnen, benötigen Sie Zugriff auf die Anlage Nummer oder **PR_ATTACH_NUM** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f556e-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="f556e-134">Rufen Sie [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) zum Abrufen der Nachricht Anlagentabelle, und suchen Sie die Zeile, die die Anlage geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f556e-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="f556e-135">Weitere Informationen finden Sie unter [Öffnen einer Anlage](opening-an-attachment.md) .</span><span class="sxs-lookup"><span data-stu-id="f556e-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="f556e-136">Versuchen Sie nicht, öffnen Sie eine Anlage mehrmals; die Ergebnisse sind nicht definiert und die Nachricht Speicheranbieter abhängig.</span><span class="sxs-lookup"><span data-stu-id="f556e-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="f556e-137">Sie können anfordern, dass die Anlage im Lese-/Schreibmodus anstelle der Standardmodus schreibgeschützt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f556e-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="f556e-138">Bis zu der Nachricht Informationsdienst jedoch ist, ob die Anlage tatsächlich im Lese-/Schreibmodus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f556e-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="f556e-139">Sie können entweder Versuch, ändern die Anlage Vorbereitung auf mögliche Ausfälle behandeln oder Überprüfen Sie die Zugriffsebene, die durch die Anlage **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft, abrufen, falls verfügbar erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="f556e-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f556e-140">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="f556e-140">MFCMAPI reference</span></span>

<span data-ttu-id="f556e-141">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f556e-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f556e-142">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f556e-142">**File**</span></span>|<span data-ttu-id="f556e-143">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f556e-143">**Function**</span></span>|<span data-ttu-id="f556e-144">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f556e-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f556e-145">AttachmentsDlg.cpp verwendet, um</span><span class="sxs-lookup"><span data-stu-id="f556e-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="f556e-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="f556e-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="f556e-147">MFCMAPI (engl.) wird die **IMessage::OpenAttach** -Methode verwendet, um Attachment-Objekte zu öffnen,</span><span class="sxs-lookup"><span data-stu-id="f556e-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f556e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f556e-148">See also</span></span>



[<span data-ttu-id="f556e-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f556e-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="f556e-150">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f556e-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


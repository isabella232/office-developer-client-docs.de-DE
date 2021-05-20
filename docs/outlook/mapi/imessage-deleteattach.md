---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430707"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="a810a-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="a810a-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="a810a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a810a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a810a-105">Löscht eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="a810a-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a810a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a810a-106">Parameters</span></span>

 <span data-ttu-id="a810a-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="a810a-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="a810a-108">[in] Indexnummer der zu löschende Anlage.</span><span class="sxs-lookup"><span data-stu-id="a810a-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="a810a-109">Dies ist der Wert für die **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft der Anlage.</span><span class="sxs-lookup"><span data-stu-id="a810a-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="a810a-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a810a-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="a810a-111">[in] Behandeln Sie das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a810a-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="a810a-112">Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das ATTACH_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a810a-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a810a-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a810a-113">_lpProgress_</span></span>
  
> <span data-ttu-id="a810a-114">[in] Zeiger auf ein Statusobjekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a810a-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a810a-115">Wenn NULL in  _lpProgress übergeben_ wird, zeigt der Nachrichtenspeicheranbieter mithilfe der MAPI-Fortschrittsobjektimplementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="a810a-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="a810a-116">Der _lpProgress-Parameter_ wird ignoriert, es sei denn, ATTACH_DIALOG in _ulFlags festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="a810a-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a810a-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a810a-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a810a-118">[in] Bitmaske von Flags, die die Anzeige einer Benutzeroberfläche steuert.</span><span class="sxs-lookup"><span data-stu-id="a810a-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="a810a-119">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a810a-119">The following flag can be set:</span></span>
    
<span data-ttu-id="a810a-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a810a-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="a810a-121">Fordert die Anzeige eines Statusindikators an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a810a-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a810a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a810a-122">Return value</span></span>

<span data-ttu-id="a810a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a810a-123">S_OK</span></span> 
  
> <span data-ttu-id="a810a-124">Die Anlage wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a810a-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a810a-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a810a-125">Remarks</span></span>

<span data-ttu-id="a810a-126">Die **IMessage::D eleteAttach-Methode** löscht eine Anlage innerhalb einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a810a-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="a810a-127">Eine gelöschte Anlage wird erst endgültig gelöscht, wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a810a-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a810a-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a810a-128">Notes to callers</span></span>

<span data-ttu-id="a810a-129">Rufen Sie **vor dem Aufrufen von DeleteAttach** die **IUnknown::Release-Methode** für die Anlage und jeden ihrer Datenströme auf.</span><span class="sxs-lookup"><span data-stu-id="a810a-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="a810a-130">Da das Löschen einer Anlage ein langwieriger Prozess sein kann, bietet **DeleteAttach** den Mechanismus, der eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a810a-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="a810a-131">Sie können die Anzeige eines Statusindikators anfordern, indem Sie einen Zeiger an Ihre [IMAPIProgress : IUnknown-Implementierung](imapiprogressiunknown.md) oder NULL übergeben, wenn Sie über keine Implementierung verfügen.</span><span class="sxs-lookup"><span data-stu-id="a810a-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="a810a-132">Sie müssen auch ein Fensterhandle im  _ulUIParam-Parameter_ und das ATTACH_DIALOG im  _ulFlags-Parameter_ angeben.</span><span class="sxs-lookup"><span data-stu-id="a810a-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a810a-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a810a-133">MFCMAPI reference</span></span>

<span data-ttu-id="a810a-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a810a-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a810a-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a810a-135">**File**</span></span>|<span data-ttu-id="a810a-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a810a-136">**Function**</span></span>|<span data-ttu-id="a810a-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a810a-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a810a-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a810a-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="a810a-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a810a-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a810a-140">MFCMAPI verwendet die **IMessage::D eleteAttach-Methode,** um die ausgewählte Anlage zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a810a-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a810a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a810a-141">See also</span></span>



[<span data-ttu-id="a810a-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a810a-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a810a-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a810a-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="a810a-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a810a-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


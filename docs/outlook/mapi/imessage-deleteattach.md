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
ms.openlocfilehash: de5c98272c08c469acf23b0ecae7eac0a2d1bfe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592514"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="a88c6-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="a88c6-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="a88c6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a88c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a88c6-105">Löscht eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="a88c6-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a88c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a88c6-106">Parameters</span></span>

 <span data-ttu-id="a88c6-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="a88c6-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="a88c6-108">[in] Die Indexnummer der Anlage zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a88c6-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="a88c6-109">Dies ist der Wert für die Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a88c6-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="a88c6-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a88c6-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="a88c6-111">[in] Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, den, die diese Methode zeigt.</span><span class="sxs-lookup"><span data-stu-id="a88c6-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="a88c6-112">Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag ATTACH_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a88c6-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a88c6-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a88c6-113">_lpProgress_</span></span>
  
> <span data-ttu-id="a88c6-114">[in] Zeiger auf ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a88c6-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a88c6-115">Wenn NULL _LpProgress_übergeben wird, wird der Nachricht Speicheranbieter mithilfe der MAPI-Fortschritt objektimplementierung wird die Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a88c6-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="a88c6-116">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag ATTACH_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a88c6-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a88c6-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a88c6-117">_ulFlags_</span></span>
  
> <span data-ttu-id="a88c6-118">[in] Bitmaske aus Flags, die die Anzeige einer Benutzeroberfläche steuert.</span><span class="sxs-lookup"><span data-stu-id="a88c6-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="a88c6-119">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a88c6-119">The following flag can be set:</span></span>
    
<span data-ttu-id="a88c6-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a88c6-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="a88c6-121">Fordert die Anzeige einer Statusanzeige an, wie der-Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a88c6-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a88c6-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a88c6-122">Return value</span></span>

<span data-ttu-id="a88c6-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a88c6-123">S_OK</span></span> 
  
> <span data-ttu-id="a88c6-124">Die Anlage wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a88c6-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a88c6-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a88c6-125">Remarks</span></span>

<span data-ttu-id="a88c6-126">Die **IMessage::DeleteAttach** -Methode löscht eine Anlage in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a88c6-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="a88c6-127">Eine gelöschte Anlage wird nicht endgültig gelöscht werden, bis die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a88c6-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a88c6-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a88c6-128">Notes to callers</span></span>

<span data-ttu-id="a88c6-129">Vor dem Aufruf von **DeleteAttach**, rufen Sie die **IUnknown** -Methode für die Anlage und die einzelnen seine Datenströme.</span><span class="sxs-lookup"><span data-stu-id="a88c6-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="a88c6-130">Da eine Anlage löschen Anspruch sein kann, bietet **DeleteAttach** den Mechanismus, der eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a88c6-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="a88c6-131">Sie können die Anzeige einer Statusanzeige anfordern, übergeben Sie einen Zeiger auf Ihre [IMAPIProgress: IUnknown](imapiprogressiunknown.md) Implementierung oder NULL, wenn Sie nicht über eine Implementierung verfügen.</span><span class="sxs-lookup"><span data-stu-id="a88c6-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="a88c6-132">Sie müssen auch ein Fensterhandle in der _UlUIParam_ -Parameter und das Flag ATTACH_DIALOG im _UlFlags_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a88c6-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a88c6-133">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="a88c6-133">MFCMAPI reference</span></span>

<span data-ttu-id="a88c6-134">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a88c6-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a88c6-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a88c6-135">**File**</span></span>|<span data-ttu-id="a88c6-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a88c6-136">**Function**</span></span>|<span data-ttu-id="a88c6-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a88c6-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a88c6-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a88c6-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="a88c6-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a88c6-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a88c6-140">MFCMAPI (engl.) verwendet die **IMessage::DeleteAttach** -Methode, um die ausgewählte Anlage zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a88c6-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a88c6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a88c6-141">See also</span></span>



[<span data-ttu-id="a88c6-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a88c6-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a88c6-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a88c6-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="a88c6-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a88c6-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351079"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="9c863-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="9c863-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="9c863-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c863-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c863-105">Löscht eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="9c863-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9c863-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c863-106">Parameters</span></span>

 <span data-ttu-id="9c863-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="9c863-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="9c863-108">in Index Nummer der zu löschenden Anlage.</span><span class="sxs-lookup"><span data-stu-id="9c863-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="9c863-109">Dies ist der Wert für die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage.</span><span class="sxs-lookup"><span data-stu-id="9c863-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="9c863-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9c863-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="9c863-111">in Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9c863-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="9c863-112">Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das ATTACH_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c863-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9c863-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9c863-113">_lpProgress_</span></span>
  
> <span data-ttu-id="9c863-114">in Zeiger auf ein Progress-Objekt, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9c863-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9c863-115">Wenn NULL in _lpProgress_übergeben wird, zeigt der Nachrichtenspeicher Anbieter mithilfe der MAPI-Progress-Objekt Implementierung eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="9c863-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="9c863-116">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das ATTACH_DIALOG-Flag wird in _ulFlags_festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c863-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9c863-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c863-117">_ulFlags_</span></span>
  
> <span data-ttu-id="9c863-118">in Bitmaske von Flags, die die Anzeige einer Benutzeroberfläche steuert.</span><span class="sxs-lookup"><span data-stu-id="9c863-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="9c863-119">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9c863-119">The following flag can be set:</span></span>
    
<span data-ttu-id="9c863-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9c863-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="9c863-121">Fordert die Anzeige einer Statusanzeige an, während der Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9c863-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c863-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c863-122">Return value</span></span>

<span data-ttu-id="9c863-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c863-123">S_OK</span></span> 
  
> <span data-ttu-id="9c863-124">Die Anlage wurde erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9c863-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c863-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c863-125">Remarks</span></span>

<span data-ttu-id="9c863-126">Die **IMessage::D eleteattach** -Methode löscht eine Anlage aus einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9c863-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="9c863-127">Eine gelöschte Anlage wird erst dann endgültig gelöscht, wenn die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9c863-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9c863-128">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9c863-128">Notes to callers</span></span>

<span data-ttu-id="9c863-129">Rufen Sie vor dem Aufrufen von **DeleteAttach**die **IUnknown:: Release** -Methode für die Anlage und alle zugehörigen Streams auf.</span><span class="sxs-lookup"><span data-stu-id="9c863-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="9c863-130">Da das Löschen einer Anlage ein langwieriger Prozess sein kann, stellt **DeleteAttach** den Mechanismus bereit, mit dem eine Statusanzeige angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9c863-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="9c863-131">Sie können die Anzeige einer Statusanzeige anfordern, indem Sie einen Zeiger an Ihre [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Implementierung oder NULL übergeben, wenn Sie keine Implementierung haben.</span><span class="sxs-lookup"><span data-stu-id="9c863-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="9c863-132">Sie müssen auch ein Fensterhandle im Parameter _ulUIParam_ und das ATTACH_DIALOG-Flag im _ulFlags_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9c863-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9c863-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="9c863-133">MFCMAPI reference</span></span>

<span data-ttu-id="9c863-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9c863-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9c863-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9c863-135">**File**</span></span>|<span data-ttu-id="9c863-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9c863-136">**Function**</span></span>|<span data-ttu-id="9c863-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9c863-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c863-138">AttachmentsDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="9c863-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="9c863-139">CAttachmentsDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="9c863-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="9c863-140">MFCMAPI verwendet die **IMessage::D eleteattach** -Methode, um die ausgewählte Anlage zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9c863-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c863-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c863-141">See also</span></span>



[<span data-ttu-id="9c863-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9c863-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9c863-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9c863-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="9c863-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="9c863-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792748"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="20536-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="20536-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="20536-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20536-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20536-105">Das Formular benachrichtigt, einen Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="20536-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="20536-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20536-106">Parameters</span></span>

<span data-ttu-id="20536-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="20536-107">_pMessage_</span></span>
  
> <span data-ttu-id="20536-108">[in] Ein Zeiger auf die neu gespeicherte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="20536-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20536-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="20536-109">Return value</span></span>

<span data-ttu-id="20536-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="20536-110">S_OK</span></span> 
  
> <span data-ttu-id="20536-111">Die Benachrichtigung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="20536-111">The notification was successful.</span></span>
    
<span data-ttu-id="20536-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="20536-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="20536-113">Der Parameter _pMessage_ ist NULL, und das Formular ist entweder im Zustand [HandsOffFromNormal](handsofffromnormal-state.md) oder [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="20536-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="20536-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="20536-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="20536-115">Das Formular ist nicht in einem der folgenden Zustände:</span><span class="sxs-lookup"><span data-stu-id="20536-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="20536-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="20536-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="20536-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="20536-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="20536-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="20536-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="20536-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20536-119">Remarks</span></span>

<span data-ttu-id="20536-120">Die **IPersistMessage::SaveCompleted** -Methode wird aufgerufen, von einem Formular-Viewer, um das Formular zu benachrichtigen, das alle ausstehende Änderungen gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="20536-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="20536-121">**SaveCompleted** sollte aufgerufen werden, nur, wenn das Formular in einem der folgenden Zustände befindet:</span><span class="sxs-lookup"><span data-stu-id="20536-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="20536-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="20536-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="20536-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="20536-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="20536-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="20536-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="20536-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="20536-125">Notes to implementers</span></span>

<span data-ttu-id="20536-126">Es gibt mehrere mögliche Aktionen, die die **SaveCompleted** -Methode ausführen können, je nach der Botschaft Zeigerparameter enthält und welche Zustand die Nachricht befindet.</span><span class="sxs-lookup"><span data-stu-id="20536-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="20536-127">Jedoch bei eine Aktion erfolgreich ist, immer speichern Sie dem aktuellen Status der Nachricht, die auf der _pMessage_ -Parameter verweist und Übergang das Formular in den [normalen](normal-state.md) Zustand.</span><span class="sxs-lookup"><span data-stu-id="20536-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="20536-128">In der folgenden Tabelle werden die Bedingungen, die die Aktionen betreffen, die Sie, in der Implementierung der **SaveCompleted ergreifen sollten**beschrieben.</span><span class="sxs-lookup"><span data-stu-id="20536-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="20536-129">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="20536-129">**Condition**</span></span>|<span data-ttu-id="20536-130">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="20536-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20536-131">Der Parameter _pMessage_ ist NULL und der _fSameAsLoad_ -Parameter der [IPersistMessage::Save](ipersistmessage-save.md) -Methode auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20536-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="20536-132">Rufen Sie die [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) -Methode des alle registrierten Viewer, markieren Sie das Formular als clean und return S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="20536-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="20536-133">Der Parameter _pMessage_ ist NULL und der _fSameAsLoad_ -Parameter der **IPersistMessage::Save** -Methode auf FALSE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20536-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="20536-134">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="20536-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="20536-135">Das Formular befindet sich im HandsOffFromNormal Zustand.</span><span class="sxs-lookup"><span data-stu-id="20536-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="20536-136">Freigeben Sie die aktuelle Nachricht, und Ersetzen Sie ihn mit der Meldung über den Parameter _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="20536-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="20536-137">Rufen Sie die Ersatznachricht [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="20536-137">Call the replacement message's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="20536-138">Das Formular befindet sich im HandsOffAfterSave Zustand.</span><span class="sxs-lookup"><span data-stu-id="20536-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="20536-139">Rufen Sie die **IMAPIViewAdviseSink::OnSaved** -Methode des alle registrierten Viewer, markieren Sie das Formular als clean und return S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="20536-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="20536-140">Das Formular befindet sich im [NoScribble](noscribble-state.md) Zustand.</span><span class="sxs-lookup"><span data-stu-id="20536-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="20536-141">Freigeben Sie die aktuelle Nachricht, und Ersetzen Sie ihn mit der Meldung von _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="20536-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="20536-142">Rufen Sie die Ersatznachricht **IUnknown:: AddRef** -Methode.</span><span class="sxs-lookup"><span data-stu-id="20536-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="20536-143">Rufen Sie die **IMAPIViewAdviseSink::OnSaved** -Methode des alle registrierten Viewer, markieren Sie das Formular als clean und return S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="20536-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="20536-144">Das Formular befindet sich in einem der Zustände HandsOff und der _pMessage_ -Parameter auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20536-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="20536-145">E_INVALIDARG zurück.</span><span class="sxs-lookup"><span data-stu-id="20536-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="20536-146">Das Formular befindet sich in eine andere als die HandsOff Zustände oder der NoScribble Zustand.</span><span class="sxs-lookup"><span data-stu-id="20536-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="20536-147">E_UNEXPECTED zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="20536-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="20536-148">Weitere Informationen zum Speichern von Speicherobjekte finden Sie unter Dokumentation für die [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) oder [:: SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="20536-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) or [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20536-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20536-149">See also</span></span>



[<span data-ttu-id="20536-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20536-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="20536-151">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="20536-151">Form States</span></span>](form-states.md)


[<span data-ttu-id="20536-152">IPersistStorage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="20536-152">IPersistStorage::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[<span data-ttu-id="20536-153">:: SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="20536-153">IPersistFile::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)


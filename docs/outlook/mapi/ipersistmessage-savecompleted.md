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
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317136"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="43912-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="43912-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="43912-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43912-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43912-105">Benachrichtigt das Formular, dass ein Speichervorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="43912-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="43912-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43912-106">Parameters</span></span>

<span data-ttu-id="43912-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="43912-107">_pMessage_</span></span>
  
> <span data-ttu-id="43912-108">in Ein Zeiger auf die neu gespeicherte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="43912-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43912-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43912-109">Return value</span></span>

<span data-ttu-id="43912-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="43912-110">S_OK</span></span> 
  
> <span data-ttu-id="43912-111">Die Benachrichtigung wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43912-111">The notification was successful.</span></span>
    
<span data-ttu-id="43912-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="43912-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="43912-113">Der _pMessage_ -Parameter ist NULL, und das Formular befindet sich im [Status "handsofffromnormal](handsofffromnormal-state.md) -oder [HandsOffAfterSave](handsoffaftersave-state.md) -Zustand.</span><span class="sxs-lookup"><span data-stu-id="43912-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="43912-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="43912-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="43912-115">Das Formular befindet sich nicht in einem der folgenden Status:</span><span class="sxs-lookup"><span data-stu-id="43912-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="43912-116">Status "handsofffromnormal</span><span class="sxs-lookup"><span data-stu-id="43912-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="43912-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="43912-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="43912-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="43912-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="43912-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43912-119">Remarks</span></span>

<span data-ttu-id="43912-120">Die **IPersistMessage:: SaveCompleted** -Methode wird von einem Formular Betrachter aufgerufen, um das Formular zu benachrichtigen, dass alle ausstehenden Änderungen gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="43912-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="43912-121">**SaveCompleted** sollte nur aufgerufen werden, wenn sich das Formular in einem der folgenden Zustände befindet:</span><span class="sxs-lookup"><span data-stu-id="43912-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="43912-122">Status "handsofffromnormal</span><span class="sxs-lookup"><span data-stu-id="43912-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="43912-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="43912-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="43912-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="43912-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="43912-125">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="43912-125">Notes to implementers</span></span>

<span data-ttu-id="43912-126">Es gibt verschiedene mögliche Aktionen, die von der **SaveCompleted** -Methode ausgeführt werden können, je nachdem, was der Nachrichten Zeigerparameter enthält und in welchem Zustand sich die Nachricht befindet.</span><span class="sxs-lookup"><span data-stu-id="43912-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="43912-127">Wenn eine Aktion jedoch erfolgreich ist, speichern Sie immer den aktuellen Status der Nachricht, auf die der _pMessage_ -Parameter zeigt, und wechseln Sie in den [normalen](normal-state.md) Status des Formulars.</span><span class="sxs-lookup"><span data-stu-id="43912-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="43912-128">In der folgenden Tabelle werden die Bedingungen beschrieben, die sich auf die Aktionen auswirken, die Sie bei der Implementierung von **SaveCompleted**ausführen sollten.</span><span class="sxs-lookup"><span data-stu-id="43912-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="43912-129">**Bedingung**</span><span class="sxs-lookup"><span data-stu-id="43912-129">**Condition**</span></span>|<span data-ttu-id="43912-130">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="43912-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43912-131">Der _pMessage_ -Parameter ist NULL, und der _fSameAsLoad_ -Parameter der [IPersistMessage:: Save](ipersistmessage-save.md) -Methode ist auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43912-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="43912-132">Rufen Sie die [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved-Methode aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="43912-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="43912-133">Der _pMessage_ -Parameter ist NULL, und der _fSameAsLoad_ -Parameter der **IPersistMessage:: Save** -Methode ist auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43912-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="43912-134">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="43912-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="43912-135">Das Formular befindet sich im Status "handsofffromnormal-Zustand.</span><span class="sxs-lookup"><span data-stu-id="43912-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="43912-136">Geben Sie die aktuelle Nachricht frei, und ersetzen Sie Sie durch die Nachricht, auf die durch den _pMessage_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="43912-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="43912-137">Rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode der Ersatznachricht auf, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="43912-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="43912-138">Das Formular befindet sich im HandsOffAfterSave-Zustand.</span><span class="sxs-lookup"><span data-stu-id="43912-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="43912-139">Rufen Sie die **IMAPIViewAdviseSink::** onsaved-Methode aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="43912-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="43912-140">Das Formular befindet sich im [noscribble](noscribble-state.md) -Zustand.</span><span class="sxs-lookup"><span data-stu-id="43912-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="43912-141">Geben Sie die aktuelle Nachricht frei, und ersetzen Sie Sie durch die Nachricht, auf die von _pMessage_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="43912-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="43912-142">Rufen Sie die **IUnknown:: AddRef** -Methode der Ersatznachricht auf.</span><span class="sxs-lookup"><span data-stu-id="43912-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="43912-143">Rufen Sie die **IMAPIViewAdviseSink::** onsaved-Methode aller registrierten Viewer auf, markieren Sie das Formular als sauber, und geben Sie S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="43912-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="43912-144">Das Formular befindet sich in einem der HandsOff-Zustände, und der _pMessage_ -Parameter ist auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43912-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="43912-145">E_INVALIDARG zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="43912-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="43912-146">Das Formular befindet sich in einem anderen Status als einem der HandsOff-Zustände oder im noScribble-Zustand.</span><span class="sxs-lookup"><span data-stu-id="43912-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="43912-147">E_UNEXPECTED zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="43912-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="43912-148">Weitere Informationen zum Speichern von Speicherobjekten finden Sie in der Dokumentation zu den [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) -oder [IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="43912-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43912-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43912-149">See also</span></span>

- [<span data-ttu-id="43912-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43912-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="43912-151">Formular Status</span><span class="sxs-lookup"><span data-stu-id="43912-151">Form States</span></span>](form-states.md)

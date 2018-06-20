---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792128"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="64203-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="64203-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="64203-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64203-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64203-105">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="64203-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="64203-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64203-106">Parameters</span></span>

 <span data-ttu-id="64203-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="64203-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="64203-108">[in] Ein Wert, der steuert, wie und ob Daten im Formular gespeichert werden, bevor das Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="64203-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="64203-109">Eine der folgenden Werte kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="64203-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="64203-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="64203-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="64203-111">Formulardaten sollten nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="64203-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="64203-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="64203-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="64203-113">Der Benutzer sollte auf beliebige geänderten Daten im Formular zu speichern aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="64203-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="64203-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="64203-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="64203-115">Formulardaten sollte gespeichert werden, wenn es seit die letzten Speichern geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="64203-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="64203-116">Wenn keine Benutzeroberfläche angezeigt wird, kann das Formular optional wechseln Sie zur Verwendung der Funktionen für die Option SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="64203-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="64203-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="64203-117">Return value</span></span>

<span data-ttu-id="64203-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="64203-118">S_OK</span></span> 
  
> <span data-ttu-id="64203-119">Das Formular geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="64203-119">The form was closed.</span></span>
    
<span data-ttu-id="64203-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="64203-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="64203-121">Das Formular wurde bereits von einem vorherigen Aufruf von **ShutdownForm**geschlossen.</span><span class="sxs-lookup"><span data-stu-id="64203-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64203-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64203-122">Remarks</span></span>

<span data-ttu-id="64203-123">Formular Viewer rufen Sie die **IMAPIForm::ShutdownForm** -Methode, um ein Formular zu schließen.</span><span class="sxs-lookup"><span data-stu-id="64203-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="64203-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="64203-124">Notes to implementers</span></span>

<span data-ttu-id="64203-125">Führen Sie die folgenden Aufgaben in der Implementierung der **ShutdownForm**:</span><span class="sxs-lookup"><span data-stu-id="64203-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="64203-126">Überprüfen Sie, dass ein Viewer nicht bereits **ShutdownForm**aufgerufen wurde, und zurückgeben Sie E_UNEXPECTED, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="64203-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="64203-127">Obgleich dies unwahrscheinlich ist, sollten Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64203-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="64203-128">Rufen Sie das Formular [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) -Methode, sodass Speicher für das Formular und alle internen Datenstrukturen verfügbar bleiben, bis die Verarbeitung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="64203-128">Call your form's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="64203-129">Überprüfen Sie, ob alle nicht gespeicherten Änderungen an die Daten des Formulars.</span><span class="sxs-lookup"><span data-stu-id="64203-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="64203-130">Speichern Sie nicht gespeicherte Daten entsprechend wie der Parameter _UlSaveOptions_ durch Aufrufen des Viewers [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) -Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="64203-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="64203-131">Zerstören Sie Fenster auf der Benutzeroberfläche des Formulars.</span><span class="sxs-lookup"><span data-stu-id="64203-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="64203-132">Freigeben des Formulars Nachricht und Standortobjekten Nachricht durch ihre [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64203-132">Release your form's message and message site objects by calling their [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="64203-133">Benachrichtigt werden alle registrierte Leser von Berichten für die ausstehende beenden, indem Sie ihre [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) -Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64203-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="64203-134">Rufen Sie die [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode, um die Registrierung für Benachrichtigung des Formulars abbrechen, indem Sie der Advise-Empfängerzeiger auf **einen Nullwert fest**.</span><span class="sxs-lookup"><span data-stu-id="64203-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="64203-135">Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um den Speicherplatz für die Eigenschaften des Formulars freizugeben.</span><span class="sxs-lookup"><span data-stu-id="64203-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="64203-136">Vergleich des in Schritt 2 **AddRef** -Aufrufs des Formulars **IUnknown** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64203-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="64203-137">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="64203-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="64203-138">Nachdem diese Aktionen abgeschlossen wurden, umfassen die einzige gültigen Methoden für das Form-Objekt, das aufgerufen werden kann, die die [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64203-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="64203-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="64203-139">Notes to callers</span></span>

<span data-ttu-id="64203-140">Wenn **ShutdownForm** zurückgibt, unabhängig davon, ob ein Fehler zurückgegeben, lassen Sie das Formular durch Aufrufen seiner **IUnknown** -Methode.</span><span class="sxs-lookup"><span data-stu-id="64203-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="64203-141">Sie können von **ShutdownForm**zurückgegebenen Fehler ignorieren.</span><span class="sxs-lookup"><span data-stu-id="64203-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="64203-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64203-142">See also</span></span>



[<span data-ttu-id="64203-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="64203-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="64203-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="64203-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="64203-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="64203-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="64203-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="64203-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="64203-147">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="64203-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


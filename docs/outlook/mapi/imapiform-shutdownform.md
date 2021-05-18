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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329477"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="528af-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="528af-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="528af-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="528af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="528af-105">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="528af-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="528af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="528af-106">Parameters</span></span>

 <span data-ttu-id="528af-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="528af-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="528af-108">[in] Ein Wert, der steuert, wie oder ob Daten im Formular gespeichert werden, bevor das Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="528af-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="528af-109">Eine der folgenden Werte kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="528af-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="528af-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="528af-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="528af-111">Formulardaten sollten nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="528af-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="528af-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="528af-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="528af-113">Der Benutzer sollte aufgefordert werden, alle geänderten Daten im Formular zu speichern.</span><span class="sxs-lookup"><span data-stu-id="528af-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="528af-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="528af-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="528af-115">Formulardaten sollten gespeichert werden, wenn sie seit dem letzten Speichern geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="528af-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="528af-116">Wenn keine Benutzeroberfläche angezeigt wird, kann das Formular optional zur Verwendung der Funktionalität für die option SAVEOPTS_NOSAVE wechseln.</span><span class="sxs-lookup"><span data-stu-id="528af-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="528af-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="528af-117">Return value</span></span>

<span data-ttu-id="528af-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="528af-118">S_OK</span></span> 
  
> <span data-ttu-id="528af-119">Das Formular wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="528af-119">The form was closed.</span></span>
    
<span data-ttu-id="528af-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="528af-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="528af-121">Das Formular wurde bereits durch einen vorherigen Aufruf von **ShutdownForm geschlossen.**</span><span class="sxs-lookup"><span data-stu-id="528af-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="528af-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="528af-122">Remarks</span></span>

<span data-ttu-id="528af-123">Formularbetrachter rufen die **IMAPIForm::ShutdownForm-Methode** auf, um ein Formular zu schließen.</span><span class="sxs-lookup"><span data-stu-id="528af-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="528af-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="528af-124">Notes to implementers</span></span>

<span data-ttu-id="528af-125">Führen Sie die folgenden Aufgaben in Ihrer Implementierung von **ShutdownForm aus:**</span><span class="sxs-lookup"><span data-stu-id="528af-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="528af-126">Überprüfen Sie, ob ein Viewer **shutdownForm** noch nicht aufgerufen hat, und geben E_UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="528af-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="528af-127">Obwohl dies unwahrscheinlich ist, sollten Sie dies überprüfen.</span><span class="sxs-lookup"><span data-stu-id="528af-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="528af-128">Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) Ihres Formulars auf, damit der Speicher für das Formular und alle internen Datenstrukturen verfügbar bleiben, bis die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="528af-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="528af-129">Bestimmen Sie, ob nicht gespeicherte Änderungen an den Daten des Formulars vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="528af-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="528af-130">Speichern Sie nicht gespeicherte Daten entsprechend der Einstellung des  _ulSaveOptions-Parameters,_ indem Sie die [IMAPIMessageSite::SaveMessage-Methode](imapimessagesite-savemessage.md) ihres Viewers aufrufen.</span><span class="sxs-lookup"><span data-stu-id="528af-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="528af-131">Zerstören Sie das Benutzeroberflächenfenster Ihres Formulars.</span><span class="sxs-lookup"><span data-stu-id="528af-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="528af-132">Geben Sie die Nachrichten- und Nachrichtenwebsiteobjekte Ihres Formulars frei, indem Sie ihre [IUnknown::Release-Methoden](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="528af-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="528af-133">Benachrichtigen Sie alle registrierten Viewer über das ausstehende Herunterfahren, indem Sie ihre [IMAPIViewAdviseSink::OnShutdown-Methoden](imapiviewadvisesink-onshutdown.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="528af-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="528af-134">Rufen Sie [die IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) auf, um die Registrierung Ihres Formulars zur Benachrichtigung **abbricht,** indem Sie den Hinweissenkenzeiger auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="528af-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="528af-135">Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den Arbeitsspeicher für die Eigenschaften Ihres Formulars frei zu machen.</span><span class="sxs-lookup"><span data-stu-id="528af-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="528af-136">Rufen Sie die **IUnknown::Release-Methode** Ihres Formulars auf, die mit dem **AddRef-Aufruf** in Schritt 2 übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="528af-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="528af-137">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="528af-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="528af-138">Nachdem diese Aktionen abgeschlossen wurden, sind die einzigen gültigen Methoden für das Formularobjekt, die aufgerufen werden können, die methoden von der [IUnknown-Schnittstelle.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="528af-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="528af-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="528af-139">Notes to callers</span></span>

<span data-ttu-id="528af-140">Wenn **ShutdownForm** zurückgibt, unabhängig davon, ob ein Fehler zurückgegeben wird, geben Sie das Formular frei, indem Sie die **IUnknown::Release-Methode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="528af-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="528af-141">Sie können alle von ShutdownForm zurückgegebenen Fehler **ignorieren.**</span><span class="sxs-lookup"><span data-stu-id="528af-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="528af-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="528af-142">See also</span></span>



[<span data-ttu-id="528af-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="528af-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="528af-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="528af-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="528af-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="528af-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="528af-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="528af-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="528af-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="528af-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


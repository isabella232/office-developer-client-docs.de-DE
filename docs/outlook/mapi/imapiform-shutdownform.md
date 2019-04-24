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
# <a name="imapiformshutdownform"></a><span data-ttu-id="3ebf8-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="3ebf8-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="3ebf8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ebf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ebf8-105">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="3ebf8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ebf8-106">Parameters</span></span>

 <span data-ttu-id="3ebf8-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="3ebf8-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="3ebf8-108">in Ein Wert, der steuert, ob Daten im Formular gespeichert werden, bevor das Formular geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="3ebf8-109">Eine der folgenden Werte kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3ebf8-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="3ebf8-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="3ebf8-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="3ebf8-111">Formulardaten sollten nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="3ebf8-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="3ebf8-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="3ebf8-113">Der Benutzer sollte aufgefordert werden, geänderte Daten im Formular zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="3ebf8-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="3ebf8-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="3ebf8-115">Formulardaten sollten gespeichert werden, wenn Sie seit dem letzten Speichern geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="3ebf8-116">Wenn keine Benutzeroberfläche angezeigt wird, kann das Formular optional zur Verwendung der Funktionen für die SAVEOPTS_NOSAVE-Option wechseln.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ebf8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ebf8-117">Return value</span></span>

<span data-ttu-id="3ebf8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ebf8-118">S_OK</span></span> 
  
> <span data-ttu-id="3ebf8-119">Das Formular wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-119">The form was closed.</span></span>
    
<span data-ttu-id="3ebf8-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="3ebf8-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="3ebf8-121">Das Formular wurde bereits durch einen vorherigen Aufruf von **ShutdownForm**geschlossen.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ebf8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ebf8-122">Remarks</span></span>

<span data-ttu-id="3ebf8-123">Formular Betrachter rufen die **IMAPIForm:: ShutdownForm** -Methode auf, um ein Formular zu beenden.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ebf8-124">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="3ebf8-124">Notes to implementers</span></span>

<span data-ttu-id="3ebf8-125">Führen Sie die folgenden Aufgaben in der Implementierung von **ShutdownForm**aus:</span><span class="sxs-lookup"><span data-stu-id="3ebf8-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="3ebf8-126">Überprüfen Sie, ob ein Viewer **ShutdownForm**nicht bereits aufgerufen hat, und geben Sie E_UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="3ebf8-127">Obwohl dies unwahrscheinlich ist, sollten Sie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="3ebf8-128">Rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode des Formulars auf, sodass der Speicher für das Formular und alle internen Datenstrukturen verfügbar bleiben, bis die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="3ebf8-129">Bestimmen Sie, ob ungespeicherte Änderungen an den Formulardaten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="3ebf8-130">Speichern Sie nicht gespeicherte Daten gemäß der Festlegung des _ulSaveOptions_ -Parameters, indem Sie die [IMAPIMessageSite:: SaveMessage](imapimessagesite-savemessage.md) -Methode des Viewers aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="3ebf8-131">Zerstören Sie das Benutzeroberflächenfenster des Formulars.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="3ebf8-132">Geben Sie die Nachrichten-und Nachrichtenwebsite Objekte Ihres Formulars durch Aufrufen der [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methoden frei.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="3ebf8-133">Informieren Sie alle registrierten Betrachter des ausstehenden Herunterfahren durch Aufrufen der [IMAPIViewAdviseSink:: OnShutdown](imapiviewadvisesink-onshutdown.md) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="3ebf8-134">Rufen Sie die [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode auf, um die Registrierung Ihres Formulars für die Benachrichtigung abzubrechen, indem Sie den Advise-Senke-Zeiger auf **null**festlegen.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="3ebf8-135">Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um den Arbeitsspeicher für die Eigenschaften Ihres Formulars freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="3ebf8-136">Rufen Sie die **IUnknown:: Release** -Methode des Formulars auf, die dem in Schritt 2 **AddRef** -Aufruf entspricht.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="3ebf8-137">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3ebf8-138">Nachdem diese Aktionen abgeschlossen wurden, sind die einzigen gültigen Methoden für das Form-Objekt, die aufgerufen werden können, die von der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ebf8-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3ebf8-139">Notes to callers</span></span>

<span data-ttu-id="3ebf8-140">Wenn **ShutdownForm** zurückgegeben wird, unabhängig davon, ob ein Fehler zurückgegeben wird, lassen Sie das Formular durch Aufrufen seiner **IUnknown:: Release** -Methode los.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="3ebf8-141">Fehler, die von **ShutdownForm**zurückgegeben werden, können ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="3ebf8-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ebf8-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ebf8-142">See also</span></span>



[<span data-ttu-id="3ebf8-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="3ebf8-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="3ebf8-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="3ebf8-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="3ebf8-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3ebf8-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="3ebf8-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3ebf8-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3ebf8-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ebf8-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


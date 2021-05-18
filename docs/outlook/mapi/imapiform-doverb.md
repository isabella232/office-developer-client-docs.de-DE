---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329460"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="7365f-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="7365f-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="7365f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7365f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7365f-105">Fordert an, dass das Formular alle Aufgaben ausführen soll, die es einem bestimmten Verb zurrent.</span><span class="sxs-lookup"><span data-stu-id="7365f-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="7365f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7365f-106">Parameters</span></span>

 <span data-ttu-id="7365f-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="7365f-107">_iVerb_</span></span>
  
> <span data-ttu-id="7365f-108">[in] Die Zahl, die einem der Verben des Formulars zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7365f-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="7365f-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="7365f-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="7365f-110">[in] Ein Zeiger auf ein Ansichtskontextobjekt.</span><span class="sxs-lookup"><span data-stu-id="7365f-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="7365f-111">Der _lpViewContext-Parameter_ kann **null sein.**</span><span class="sxs-lookup"><span data-stu-id="7365f-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="7365f-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="7365f-112">_hwndParent_</span></span>
  
> <span data-ttu-id="7365f-113">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="7365f-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="7365f-114">Der  _hwndParent-Parameter_ sollte **null sein,** wenn das Dialogfeld oder Fenster nicht modal ist.</span><span class="sxs-lookup"><span data-stu-id="7365f-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="7365f-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="7365f-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="7365f-116">[in] Ein Zeiger auf eine Win32 [RECT-Struktur,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) die die Größe und Position des Formularfensters enthält.</span><span class="sxs-lookup"><span data-stu-id="7365f-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7365f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7365f-117">Return value</span></span>

<span data-ttu-id="7365f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7365f-118">S_OK</span></span> 
  
> <span data-ttu-id="7365f-119">Das Verb wurde erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7365f-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="7365f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="7365f-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="7365f-121">Das verb, das durch den  _iVerb-Parameter_ dargestellt wird, ist gültig, aber das Formular kann die derzeit zugeordneten Vorgänge nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="7365f-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7365f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7365f-122">Remarks</span></span>

<span data-ttu-id="7365f-123">Formularbetrachter rufen die **IMAPIForm::D oVerb-Methode** auf, um anzusinnen, dass das Formular die Aufgaben ausführen soll, die es mit jedem verb verknüpft, das das Formular unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7365f-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="7365f-124">Jedes der unterstützten Verben wird durch einen numerischen Wert identifiziert, der im **iVerb-Parameter** an  _DoVerb übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="7365f-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="7365f-125">Typische Implementierungen von **DoVerb** enthalten eine **switch-Anweisung,** die die Werte testet, die für den  _iVerb-Parameter_ für das Formular gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7365f-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7365f-126">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7365f-126">Notes to implementers</span></span>

<span data-ttu-id="7365f-127">Wenn der Formularanzeiger einen Ansichtskontext im  _lpViewContext-Parameter_ angibt, verwenden Sie ihn in Der **DoVerb-Implementierung** anstelle des Ansichtskontexts, der in einem früheren Aufruf der [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7365f-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="7365f-128">Nehmen Sie alle änderungen vor, die an Ihren internen Datenstrukturen erforderlich sind, und speichern Sie den Ansichtskontext nicht.</span><span class="sxs-lookup"><span data-stu-id="7365f-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="7365f-129">Führen Sie die folgenden Aufgaben in Ihrer **DoVerb-Implementierung** aus:</span><span class="sxs-lookup"><span data-stu-id="7365f-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="7365f-130">Führen Sie den code aus, der für das bestimmte Verb erforderlich ist, das dem  _iVerb-Parameter zugeordnet_ ist.</span><span class="sxs-lookup"><span data-stu-id="7365f-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="7365f-131">Stellen Sie bei Bedarf den ursprünglichen Ansichtskontext wieder auf.</span><span class="sxs-lookup"><span data-stu-id="7365f-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="7365f-132">Wenn eine unbekannte Verbnummer übergeben wurde, geben Sie MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="7365f-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="7365f-133">Andernfalls geben Sie ein Ergebnis basierend auf dem Erfolg oder Fehler des Verbs zurück, das ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7365f-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="7365f-134">Schließen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="7365f-134">Close the form.</span></span> <span data-ttu-id="7365f-135">Es liegt immer in Ihrer Verantwortung, das Formular nach Abschluss eines **DoVerb-Anrufs** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="7365f-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="7365f-136">Einige Verben, z. B. Print, sollten im Hinblick auf den **DoVerb-Aufruf** modal sein, d. h. der angegebene Vorgang muss abgeschlossen sein, bevor der **DoVerb-Aufruf** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7365f-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="7365f-137">Rufen Sie die [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf, um die vom Formularfenster verwendete **RECT-Struktur** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7365f-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="7365f-138">Speichern Sie das Handle nicht im  _hwndParent-Parameter,_ da es zwar in der Regel bis zum Abschluss von **DoVerb** gültig bleibt, es aber sofort nach der Rückgabe des Anrufs zerstört werden kann.</span><span class="sxs-lookup"><span data-stu-id="7365f-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7365f-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7365f-139">Notes to callers</span></span>

<span data-ttu-id="7365f-140">Sie können nicht modale Verben als modale Verben verwenden, indem Sie  _lpViewContext_ auf eine Ansichtskontextimplementierung verweisen, die das VCSTATUS_MODAL-Flag aus der [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7365f-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="7365f-141">Weitere Informationen zu Verben in MAPI finden Sie unter [Form Verbs](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="7365f-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="7365f-142">Weitere Informationen zum Umgang mit Verben in OLE finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7365f-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7365f-143">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7365f-143">MFCMAPI reference</span></span>

<span data-ttu-id="7365f-144">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7365f-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7365f-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7365f-145">**File**</span></span>|<span data-ttu-id="7365f-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7365f-146">**Function**</span></span>|<span data-ttu-id="7365f-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7365f-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7365f-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7365f-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7365f-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="7365f-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="7365f-150">MFCMAPI verwendet die **IMAPIForm::D oVerb-Methode** zum Aufrufen eines Verbs in einem Formular.</span><span class="sxs-lookup"><span data-stu-id="7365f-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7365f-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7365f-151">See also</span></span>



[<span data-ttu-id="7365f-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="7365f-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="7365f-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="7365f-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="7365f-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7365f-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="7365f-155">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7365f-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7365f-156">Formularverben</span><span class="sxs-lookup"><span data-stu-id="7365f-156">Form Verbs</span></span>](form-verbs.md)


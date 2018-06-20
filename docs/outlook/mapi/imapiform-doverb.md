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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9ea44c9ba75390f06ff12ddeed0c7b652538e07d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792161"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="c2731-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="c2731-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="c2731-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2731-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2731-105">Fordert, dass das Formular ausführen, was es Aufgaben ein bestimmtes Verb zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c2731-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="c2731-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2731-106">Parameters</span></span>

 <span data-ttu-id="c2731-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="c2731-107">_iVerb_</span></span>
  
> <span data-ttu-id="c2731-108">[in] Die Anzahl eines Verben für das Formular zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c2731-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="c2731-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="c2731-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="c2731-110">[in] Ein Zeiger auf eine Ansicht Context-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2731-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="c2731-111">Der Parameter _LpViewContext_ kann **null**sein.</span><span class="sxs-lookup"><span data-stu-id="c2731-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="c2731-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="c2731-112">_hwndParent_</span></span>
  
> <span data-ttu-id="c2731-113">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="c2731-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="c2731-114">Der Parameter _HwndParent_ muss **null** sein, wenn das Dialogfeld oder Fenster nicht modalen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="c2731-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="c2731-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="c2731-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="c2731-116">[in] Ein Zeiger auf eine Win32- [Rechteck](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) -Struktur, die die Größe und Position des Fenster des Formulars enthält.</span><span class="sxs-lookup"><span data-stu-id="c2731-116">[in] A pointer to a Win32 [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2731-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c2731-117">Return value</span></span>

<span data-ttu-id="c2731-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2731-118">S_OK</span></span> 
  
> <span data-ttu-id="c2731-119">Das Verb wurde erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c2731-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="c2731-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="c2731-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="c2731-121">Das Verb, dargestellt durch den Parameter _iVerb_ ist gültig, aber das Formular kann nicht ausgeführt werden die Vorgänge, die derzeit zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c2731-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c2731-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2731-122">Remarks</span></span>

<span data-ttu-id="c2731-123">Formular Viewer rufen Sie die **IMAPIForm::DoVerb** -Methode, um anzufordern, dass das Formular der Aufgaben, bei denen es jedes Verb zugeordnet, die das Formular unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2731-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="c2731-124">Jeder der unterstützten Verben wird durch einen numerischen Wert, der im Parameter _iVerb_ **DoVerb** übergeben identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c2731-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="c2731-125">Typische Implementierungen von **DoVerb** enthalten eine **switch** -Anweisung, die die Werte getestet, die für den Parameter _iVerb_ für das Formular gültig sind.</span><span class="sxs-lookup"><span data-stu-id="c2731-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c2731-126">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c2731-126">Notes to implementers</span></span>

<span data-ttu-id="c2731-127">Verwenden sie der Formular-Viewer ein Ansichtskontext im _LpViewContext_ -Parameter gibt an, in der Implementierung **DoVerb** anstelle der Ansichtskontext einen früheren Aufruf der [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="c2731-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="c2731-128">Stellen Sie alle Änderungen sind erforderlich, um Ihre internen Datenstrukturen und den Ansichtskontext nicht speichern.</span><span class="sxs-lookup"><span data-stu-id="c2731-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="c2731-129">Führen Sie die folgenden Aufgaben in der Implementierung **DoVerb** :</span><span class="sxs-lookup"><span data-stu-id="c2731-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="c2731-130">Führen Sie den Code für das jeweilige Verb erforderlich ist, mit dem Parameter _iVerb_ verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c2731-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="c2731-131">Bei Bedarf wiederherstellen Sie den ursprünglichen Ansichtskontext.</span><span class="sxs-lookup"><span data-stu-id="c2731-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="c2731-132">Wenn eine unbekannte Verbanzahl übergeben wurde, geben Sie MAPI_E_NO_SUPPORT zurück.</span><span class="sxs-lookup"><span data-stu-id="c2731-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="c2731-133">Anderenfalls zurückgeben Sie basierend auf den Erfolg oder Misserfolg des jegliches Verb ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c2731-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="c2731-134">Schließen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="c2731-134">Close the form.</span></span> <span data-ttu-id="c2731-135">Es ist immer sicherstellen, dass Sie das Formular nach Abschluss einer **DoVerb** -Aufrufs zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c2731-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="c2731-136">Einige Verben, wie beispielsweise drucken, sollte im Hinblick auf den Anruf **DoVerb** modal sein – d. h., die angegebene Operation muss gestartet werden, bevor der Aufruf **DoVerb** beendet.</span><span class="sxs-lookup"><span data-stu-id="c2731-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="c2731-137">Rufen Sie die [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2731-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="c2731-138">Speichern Sie das Handle nicht im Parameter _HwndParent_ , da es in der Regel gültig bis zum Abschluss des **DoVerb**bleibt, es sofort bei der Rückgabe des Aufrufs gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2731-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c2731-139">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c2731-139">Notes to callers</span></span>

<span data-ttu-id="c2731-140">Sie können festlegen, dass nicht gebundenes Verben fungieren als modales Verben zeigen Sie _LpViewContext_ an die Implementierung einer Ansicht Kontext, die die Kennzeichen VCSTATUS_MODAL von der [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c2731-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="c2731-141">Weitere Informationen zu Verben in MAPI finden Sie unter [Formular Verben](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="c2731-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="c2731-142">Weitere Informationen dazu, wie Verben in OLE behandelt werden finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2731-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c2731-143">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c2731-143">MFCMAPI reference</span></span>

<span data-ttu-id="c2731-144">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c2731-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c2731-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c2731-145">**File**</span></span>|<span data-ttu-id="c2731-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c2731-146">**Function**</span></span>|<span data-ttu-id="c2731-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c2731-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c2731-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c2731-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c2731-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="c2731-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="c2731-150">MFCMAPI (engl.) verwendet die **IMAPIForm::DoVerb** -Methode zum Aufrufen eines Verbs in einem Formular.</span><span class="sxs-lookup"><span data-stu-id="c2731-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2731-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2731-151">See also</span></span>



[<span data-ttu-id="c2731-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="c2731-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="c2731-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="c2731-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="c2731-154">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2731-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="c2731-155">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c2731-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="c2731-156">Formular Verben</span><span class="sxs-lookup"><span data-stu-id="c2731-156">Form Verbs</span></span>](form-verbs.md)


---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c1ba49ba1b4deacb684da1411d86ebd4dd19e63f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792136"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="e536b-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="e536b-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="e536b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e536b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e536b-105">Stellt ein Ansichtskontext für das Formular her.</span><span class="sxs-lookup"><span data-stu-id="e536b-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="e536b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e536b-106">Parameters</span></span>

 <span data-ttu-id="e536b-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="e536b-107">_pViewContext_</span></span>
  
> <span data-ttu-id="e536b-108">[in] Ein Zeiger auf den neuen Ansichtskontext für das Formular.</span><span class="sxs-lookup"><span data-stu-id="e536b-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e536b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e536b-109">Return value</span></span>

<span data-ttu-id="e536b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e536b-110">S_OK</span></span> 
  
> <span data-ttu-id="e536b-111">Der Ansichtskontext wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e536b-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e536b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e536b-112">Remarks</span></span>

<span data-ttu-id="e536b-113">Formular Viewer rufen Sie die **IMAPIForm::SetViewContext** -Methode, um ein bestimmtes Formular Ansichtskontext als aktuelle einzurichten.</span><span class="sxs-lookup"><span data-stu-id="e536b-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="e536b-114">Ein Formular kann jeweils nur ein Ansichtskontext haben.</span><span class="sxs-lookup"><span data-stu-id="e536b-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e536b-115">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e536b-115">Notes to implementers</span></span>

<span data-ttu-id="e536b-116">Die meisten Formular Server implementieren **SetViewContext** mithilfe des folgenden Algorithmus:</span><span class="sxs-lookup"><span data-stu-id="e536b-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="e536b-117">Wenn ein Ansichtskontext für das Formular bereits vorhanden ist, brechen Sie Registrierung für das Formular durch Aufrufen der [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) -Methode mit **null** im Parameter _Pmnvs ab_ , und rufen Sie dann dem Ansichtskontext [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methode, um die verringert den Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="e536b-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="e536b-118">Wenn der neue Ansichtskontext ungleich **null**ist, Anruf **IMAPIViewContext::SetAdviseSink** mithilfe des _pViewContext_ -Parameters So richten Sie eine neue Ansicht ein advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="e536b-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="e536b-119">Wenn der neue Ansichtskontext ungleich **null**ist, rufen Sie die [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode, um zu bestimmen, welche Status-Flags festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="e536b-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="e536b-120">Wenn der neue Ansichtskontext ungleich **null**ist, speichern Sie sie, und rufen Sie dessen [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) -Methode, um den Referenzzähler erhöhen.</span><span class="sxs-lookup"><span data-stu-id="e536b-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="e536b-121">Aktualisieren Sie alle Elemente der Benutzeroberfläche, die von dem Ansichtskontext abhängen.</span><span class="sxs-lookup"><span data-stu-id="e536b-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="e536b-122">**SetViewContext** können auch andere Aktionen durchführen, je nach den Statusflags für von **IMAPIViewContext::GetViewStatus**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e536b-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="e536b-123">Wenn die Flags VCSTATUS_NEXT und VCSTATUS_PREV zurückgegeben werden, können beispielsweise **SetViewContext** die **nächsten** oder **vorherigen** Schaltflächen für die neue Ansichtskontext aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e536b-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e536b-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="e536b-124">MFCMAPI reference</span></span>

<span data-ttu-id="e536b-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e536b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e536b-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e536b-126">**File**</span></span>|<span data-ttu-id="e536b-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e536b-127">**Function**</span></span>|<span data-ttu-id="e536b-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e536b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e536b-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e536b-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e536b-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="e536b-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="e536b-131">MFCMAPI (engl.) mithilfe die **IMAPIForm::SetViewContext** -Methode Ansichtskontext MFCMAPI des (engl.) auf dem Formular festgelegt werden, bevor das Formular angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e536b-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e536b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e536b-132">See also</span></span>



[<span data-ttu-id="e536b-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="e536b-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="e536b-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e536b-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="e536b-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e536b-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="e536b-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e536b-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


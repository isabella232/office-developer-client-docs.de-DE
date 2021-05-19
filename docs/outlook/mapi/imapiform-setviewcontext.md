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
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350946"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="03b12-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="03b12-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="03b12-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03b12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03b12-105">Richtet einen Ansichtskontext für das Formular ein.</span><span class="sxs-lookup"><span data-stu-id="03b12-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="03b12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03b12-106">Parameters</span></span>

 <span data-ttu-id="03b12-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="03b12-107">_pViewContext_</span></span>
  
> <span data-ttu-id="03b12-108">[in] Ein Zeiger auf den neuen Ansichtskontext für das Formular.</span><span class="sxs-lookup"><span data-stu-id="03b12-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03b12-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03b12-109">Return value</span></span>

<span data-ttu-id="03b12-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="03b12-110">S_OK</span></span> 
  
> <span data-ttu-id="03b12-111">Der Ansichtskontext wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="03b12-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03b12-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03b12-112">Remarks</span></span>

<span data-ttu-id="03b12-113">Formularbetrachter rufen die **IMAPIForm::SetViewContext-Methode** auf, um einen bestimmten Formularansichtskontext als aktuell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03b12-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="03b12-114">Ein Formular kann immer nur einen Ansichtskontext haben.</span><span class="sxs-lookup"><span data-stu-id="03b12-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="03b12-115">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="03b12-115">Notes to implementers</span></span>

<span data-ttu-id="03b12-116">Die meisten Formularserver implementieren **SetViewContext** mithilfe des folgenden Algorithmus:</span><span class="sxs-lookup"><span data-stu-id="03b12-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="03b12-117">Wenn bereits ein Ansichtskontext für das Formular vorhanden ist, brechen Sie die Registrierung des Formulars ab, indem Sie die [IMAPIViewContext::SetAdviseSink-Methode](imapiviewcontext-setadvisesink.md) mit **Null** im  _pmnvs-Parameter_ aufrufen und dann die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Ansichtskontexts aufrufen, um die Referenzanzahl zu dekrementieren.</span><span class="sxs-lookup"><span data-stu-id="03b12-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="03b12-118">Wenn der neue Ansichtskontext nicht **null** ist, rufen Sie **IMAPIViewContext::SetAdviseSink** auf, indem Sie den  _pViewContext-Parameter_ verwenden, um eine neue Ansichtssenke zu einrichten.</span><span class="sxs-lookup"><span data-stu-id="03b12-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="03b12-119">Wenn der neue Ansichtskontext nicht **null** ist, rufen Sie die [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) auf, um zu bestimmen, welche Statusflags festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="03b12-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="03b12-120">Wenn der neue Ansichtskontext nicht **null** ist, speichern Sie ihn, und rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) auf, um die Referenzanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="03b12-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="03b12-121">Aktualisieren Sie alle Benutzeroberflächenelemente, die vom Ansichtskontext abhängen.</span><span class="sxs-lookup"><span data-stu-id="03b12-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="03b12-122">Abhängig von den status flags, die von **IMAPIViewContext::GetViewStatus** zurückgegeben werden, **kann SetViewContext** auch andere Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="03b12-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="03b12-123">Wenn beispielsweise die VCSTATUS_NEXT und VCSTATUS_PREV zurückgegeben werden, kann **SetViewContext** die Schaltflächen **Next** und **Previous** für den neuen Ansichtskontext aktivieren.</span><span class="sxs-lookup"><span data-stu-id="03b12-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="03b12-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="03b12-124">MFCMAPI reference</span></span>

<span data-ttu-id="03b12-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="03b12-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="03b12-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="03b12-126">**File**</span></span>|<span data-ttu-id="03b12-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="03b12-127">**Function**</span></span>|<span data-ttu-id="03b12-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="03b12-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03b12-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="03b12-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="03b12-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="03b12-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="03b12-131">MFCMAPI verwendet die **IMAPIForm::SetViewContext-Methode,** um den Ansichtskontext von MFCMAPI auf dem Formular vor dem Anzeigen des Formulars zu setzen.</span><span class="sxs-lookup"><span data-stu-id="03b12-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03b12-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03b12-132">See also</span></span>



[<span data-ttu-id="03b12-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="03b12-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="03b12-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="03b12-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="03b12-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03b12-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="03b12-136">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="03b12-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


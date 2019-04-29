---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430903"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="2709a-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="2709a-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="2709a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2709a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2709a-105">Gibt den aktuellen Ansichtskontext für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="2709a-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="2709a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2709a-106">Parameters</span></span>

 <span data-ttu-id="2709a-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="2709a-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="2709a-108">Out Ein Zeiger auf einen Zeiger auf den Ansichtskontext des Formulars.</span><span class="sxs-lookup"><span data-stu-id="2709a-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2709a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2709a-109">Return value</span></span>

<span data-ttu-id="2709a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2709a-110">S_OK</span></span> 
  
> <span data-ttu-id="2709a-111">Der aktuelle Ansichtskontext des Formulars wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2709a-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="2709a-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2709a-112">S_FALSE</span></span> 
  
> <span data-ttu-id="2709a-113">Es gibt keinen Ansichtskontext für das Formular.</span><span class="sxs-lookup"><span data-stu-id="2709a-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2709a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2709a-114">Remarks</span></span>

<span data-ttu-id="2709a-115">Formular Betrachter rufen \*\*\*\* getviewcontext auf, um einen Zeiger auf den Ansichtskontext abzurufen, der in einem vorherigen Aufruf von [IMAPIForm::](imapiform-setviewcontext.md)setviewcontext festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="2709a-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="2709a-116">Wenn kein vorheriger Aufruf an setViewcontext vorgenommen wurde, \*\*\*\* wird _ppViewContext_ auf NULL festgelegt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2709a-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2709a-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="2709a-117">Notes to implementers</span></span>

<span data-ttu-id="2709a-118">Kopieren Sie den Ansichtskontext des Formulars in den Zeiger, der vom aufrufenden Formular Betrachter im _ppViewContext_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2709a-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="2709a-119">Wenn das Formular keinen Ansichtskontext hat, legen Sie _ppViewContext_ auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="2709a-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2709a-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="2709a-120">MFCMAPI reference</span></span>

<span data-ttu-id="2709a-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2709a-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2709a-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2709a-122">**File**</span></span>|<span data-ttu-id="2709a-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="2709a-123">**Function**</span></span>|<span data-ttu-id="2709a-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2709a-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2709a-125">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="2709a-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2709a-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="2709a-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2709a-127">MFCMAPI verwendet die **IMAPIForm::** getviewcontext-Methode, um zu überprüfen, ob ein Formular einen Ansichtskontext aufweist.</span><span class="sxs-lookup"><span data-stu-id="2709a-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2709a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2709a-128">See also</span></span>



[<span data-ttu-id="2709a-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2709a-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="2709a-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2709a-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="2709a-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="2709a-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


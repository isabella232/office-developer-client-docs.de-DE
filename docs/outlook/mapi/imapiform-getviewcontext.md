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
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792125"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="d64ec-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="d64ec-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="d64ec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d64ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d64ec-105">Gibt den aktuellen Ansichtskontext für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="d64ec-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="d64ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d64ec-106">Parameters</span></span>

 <span data-ttu-id="d64ec-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="d64ec-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="d64ec-108">[out] Ein Zeiger auf einen Zeiger auf das Formular Ansichtskontext.</span><span class="sxs-lookup"><span data-stu-id="d64ec-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d64ec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d64ec-109">Return value</span></span>

<span data-ttu-id="d64ec-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d64ec-110">S_OK</span></span> 
  
> <span data-ttu-id="d64ec-111">Das Formular aktuellen Ansichtskontext wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d64ec-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="d64ec-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d64ec-112">S_FALSE</span></span> 
  
> <span data-ttu-id="d64ec-113">Es ist keine Ansichtskontext für das Formular.</span><span class="sxs-lookup"><span data-stu-id="d64ec-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d64ec-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d64ec-114">Remarks</span></span>

<span data-ttu-id="d64ec-115">Formular Viewer aufrufen **GetViewContext** um einen Zeiger auf die in einem vorherigen Aufruf von [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)hergestellt Ansichtskontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d64ec-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="d64ec-116">Falls keine vorherigen Aufruf **SetViewContext**vorgenommen wurden, legt **GetViewContext** _PpViewContext_ auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="d64ec-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d64ec-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d64ec-117">Notes to implementers</span></span>

<span data-ttu-id="d64ec-118">Kopieren des Formulars Ansicht Kontext Zeiger in der durch den aufrufenden Formular Viewer im _PpViewContext_ -Parameter übergebene Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d64ec-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="d64ec-119">Wenn das Formular nicht über ein Ansichtskontext verfügt, _PpViewContext_ auf NULL festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d64ec-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d64ec-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="d64ec-120">MFCMAPI reference</span></span>

<span data-ttu-id="d64ec-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d64ec-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d64ec-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d64ec-122">**File**</span></span>|<span data-ttu-id="d64ec-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d64ec-123">**Function**</span></span>|<span data-ttu-id="d64ec-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d64ec-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d64ec-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d64ec-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d64ec-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="d64ec-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="d64ec-127">MFCMAPI (engl.) verwendet die **IMAPIForm::GetViewContext** -Methode überprüfen, ob ein Formular ein Ansichtskontext aufweist.</span><span class="sxs-lookup"><span data-stu-id="d64ec-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d64ec-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d64ec-128">See also</span></span>



[<span data-ttu-id="d64ec-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d64ec-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="d64ec-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d64ec-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="d64ec-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d64ec-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792375"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="b6c97-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="b6c97-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="b6c97-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6c97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6c97-105">Ruft ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6c97-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="b6c97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6c97-106">Parameters</span></span>

 <span data-ttu-id="b6c97-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b6c97-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b6c97-108">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="b6c97-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="b6c97-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6c97-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b6c97-110">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt Fortschritt Fortschritt berechnen soll.</span><span class="sxs-lookup"><span data-stu-id="b6c97-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="b6c97-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b6c97-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b6c97-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b6c97-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="b6c97-113">Status für ein Element der obersten Ebene wie beispielsweise einen übergeordneten Ordner berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b6c97-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="b6c97-114">Das Objekt Fortschritt sollte verwenden Sie die Werte in [IMAPIProgress::Progress](imapiprogress-progress.md) _UlCount_ und _UlTotal_ Methodenparameter – die das aktuelle Element und die insgesamt Elemente bei der Konflikte jeweils angeben – um den Fortschritt zu erhöhen Symbol für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b6c97-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="b6c97-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="b6c97-115">_lppProgress_</span></span>
  
> <span data-ttu-id="b6c97-116">[out] Ein Zeiger auf einen Zeiger auf das Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6c97-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6c97-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b6c97-117">Return value</span></span>

<span data-ttu-id="b6c97-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6c97-118">S_OK</span></span> 
  
> <span data-ttu-id="b6c97-119">Das Fortschritt-Objekt wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b6c97-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6c97-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6c97-120">Remarks</span></span>

<span data-ttu-id="b6c97-121">Die **IMAPISupport::DoProgressDialog** -Methode wird für Adresse Adressbuch und Nachricht Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="b6c97-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="b6c97-122">Diese Anbieter Aufrufen **DoProgressDialog** Zugriff auf die MAPI-Implementierung der [IMAPIProgress](imapiprogressiunknown.md) -Schnittstelle, die berechnet der Fortschrittsinformationen und ein standard-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6c97-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="b6c97-123">Informationen zur Verwendung eines Objekts des Fortschritts und der **IMAPIProgress** -Schnittstelle finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b6c97-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6c97-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6c97-124">See also</span></span>



[<span data-ttu-id="b6c97-125">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6c97-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="b6c97-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="b6c97-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="b6c97-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6c97-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="b6c97-128">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="b6c97-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)


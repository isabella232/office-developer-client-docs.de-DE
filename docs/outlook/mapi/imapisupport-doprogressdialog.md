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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 32174e213334d784220b960364443e60db6d1d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582777"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="620f1-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="620f1-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="620f1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="620f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="620f1-105">Ruft ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="620f1-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="620f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="620f1-106">Parameters</span></span>

 <span data-ttu-id="620f1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="620f1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="620f1-108">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="620f1-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="620f1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="620f1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="620f1-110">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt Fortschritt Fortschritt berechnen soll.</span><span class="sxs-lookup"><span data-stu-id="620f1-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="620f1-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="620f1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="620f1-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="620f1-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="620f1-113">Status für ein Element der obersten Ebene wie beispielsweise einen übergeordneten Ordner berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="620f1-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="620f1-114">Das Objekt Fortschritt sollte verwenden Sie die Werte in [IMAPIProgress::Progress](imapiprogress-progress.md) _UlCount_ und _UlTotal_ Methodenparameter – die das aktuelle Element und die insgesamt Elemente bei der Konflikte jeweils angeben – um den Fortschritt zu erhöhen Symbol für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="620f1-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="620f1-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="620f1-115">_lppProgress_</span></span>
  
> <span data-ttu-id="620f1-116">[out] Ein Zeiger auf einen Zeiger auf das Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="620f1-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="620f1-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="620f1-117">Return value</span></span>

<span data-ttu-id="620f1-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="620f1-118">S_OK</span></span> 
  
> <span data-ttu-id="620f1-119">Das Fortschritt-Objekt wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="620f1-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="620f1-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="620f1-120">Remarks</span></span>

<span data-ttu-id="620f1-121">Die **IMAPISupport::DoProgressDialog** -Methode wird für Adresse Adressbuch und Nachricht Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="620f1-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="620f1-122">Diese Anbieter Aufrufen **DoProgressDialog** Zugriff auf die MAPI-Implementierung der [IMAPIProgress](imapiprogressiunknown.md) -Schnittstelle, die berechnet der Fortschrittsinformationen und ein standard-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="620f1-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="620f1-123">Informationen zur Verwendung eines Objekts des Fortschritts und der **IMAPIProgress** -Schnittstelle finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="620f1-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="620f1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="620f1-124">See also</span></span>



[<span data-ttu-id="620f1-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="620f1-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="620f1-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="620f1-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="620f1-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="620f1-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="620f1-128">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="620f1-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)


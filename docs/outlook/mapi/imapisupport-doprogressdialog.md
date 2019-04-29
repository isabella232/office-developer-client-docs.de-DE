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
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432583"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="a9ea6-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="a9ea6-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="a9ea6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9ea6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9ea6-105">Ruft ein Progress-Objekt ab, das eine Statusanzeige anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="a9ea6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9ea6-106">Parameters</span></span>

 <span data-ttu-id="a9ea6-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a9ea6-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a9ea6-108">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="a9ea6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9ea6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a9ea6-110">in Eine Bitmaske von Flags, die die Berechnung des Fortschritts durch das Progress-Objekt steuert.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="a9ea6-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a9ea6-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a9ea6-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="a9ea6-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="a9ea6-113">Der Fortschritt wird für ein Element auf oberster Ebene, wie beispielsweise einen übergeordneten Ordner, berechnet.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="a9ea6-114">Das Progress-Objekt sollte die Werte in den Parametern _ulCount_ und _ulTotal_ der [IMAPIProgress::P rogress](imapiprogress-progress.md) -Methode verwenden, die das aktuelle Element und die gesamten Elemente in der Operation angeben, um den Fortschritt zu erhöhen. Indikator für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="a9ea6-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="a9ea6-115">_lppProgress_</span></span>
  
> <span data-ttu-id="a9ea6-116">Out Ein Zeiger auf einen Zeiger auf das Progress-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9ea6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9ea6-117">Return value</span></span>

<span data-ttu-id="a9ea6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9ea6-118">S_OK</span></span> 
  
> <span data-ttu-id="a9ea6-119">Das Progress-Objekt wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9ea6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9ea6-120">Remarks</span></span>

<span data-ttu-id="a9ea6-121">Die **IMAPISupport::D oprogressdialog** -Methode wird für Support Objekte des Adressbuchs und des Nachrichtenspeichers implementiert.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="a9ea6-122">Diese Anbieter rufen **DoProgressDialog** auf, um auf die MAPI-Implementierung der [IMAPIProgress](imapiprogressiunknown.md) -Schnittstelle zuzugreifen, die die Fortschrittsinformationen berechnet und ein Standarddialogfeld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a9ea6-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="a9ea6-123">Informationen zur Verwendung eines Progress-Objekts und der **IMAPIProgress** -Schnittstelle finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="a9ea6-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9ea6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ea6-124">See also</span></span>



[<span data-ttu-id="a9ea6-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9ea6-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="a9ea6-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="a9ea6-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="a9ea6-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9ea6-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="a9ea6-128">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="a9ea6-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)


---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421466"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="f8553-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="f8553-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="f8553-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8553-105">Legt die unteren und oberen Grenzwerte für die Anzahl der Elemente im Vorgang und die Flags fest, die steuern, wie Fortschrittsinformationen für den Vorgang berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f8553-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f8553-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8553-106">Parameters</span></span>

 <span data-ttu-id="f8553-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="f8553-107">_lpulMin_</span></span>
  
> <span data-ttu-id="f8553-108">[in] Ein Zeiger auf eine Variable, die die untere Grenze der Elemente im Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="f8553-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="f8553-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="f8553-109">_lpulMax_</span></span>
  
> <span data-ttu-id="f8553-110">[in] Ein Zeiger auf eine Variable, die die obere Grenze der Elemente im Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="f8553-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="f8553-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8553-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="f8553-112">[in] Eine Bitmaske mit Flags, die die Vorgangsebene steuert, auf der Fortschrittsinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f8553-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="f8553-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f8553-113">The following flag can be set:</span></span>
    
<span data-ttu-id="f8553-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="f8553-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="f8553-115">Verwendet die Werte in den _UlCount-_ und _ulTotal-Parametern_ der [IMAPIProgress::P rogress-Methode,](imapiprogress-progress.md) die das aktuell verarbeitete Element bzw. die Gesamtelemente angeben, um den Fortschritt des Vorgangs zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f8553-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="f8553-116">Wenn dieses Flag festgelegt ist, müssen die Werte der globalen unteren und oberen Grenzwerte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8553-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8553-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8553-117">Return value</span></span>

<span data-ttu-id="f8553-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8553-118">S_OK</span></span> 
  
> <span data-ttu-id="f8553-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f8553-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8553-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8553-120">Remarks</span></span>

<span data-ttu-id="f8553-121">Dienstanbieter rufen die **IMAPIProgress::SetLimits-Methode** auf, um das flag MAPI_TOP_LEVEL und lokale und globale Mindest- und Höchstwerte zu setzen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f8553-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="f8553-122">Der Wert der Flageinstellung wirkt sich darauf aus, ob das progress-Objekt die minimalen und maximalen Werte als lokal oder global versteht.</span><span class="sxs-lookup"><span data-stu-id="f8553-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="f8553-123">Wenn das MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global betrachtet und zur Berechnung des Fortschritts für den gesamten Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8553-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="f8553-124">Progress-Objekte initialisieren den globalen Minimalwert auf 1 und den globalen Maximalwert auf 1000.</span><span class="sxs-lookup"><span data-stu-id="f8553-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="f8553-125">Wenn MAPI_TOP_LEVEL festgelegt ist, werden die Mindest- und Höchstwerte als lokal betrachtet, und Anbieter verwenden sie intern, um den Fortschritt für Unterobjekte auf niedrigerer Ebene zu anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f8553-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="f8553-126">Progress-Objekte speichern nur die lokalen Minimal- und Maximalwerte, sodass sie an Anbieter zurückgegeben werden können, wenn die [Methoden IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f8553-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="f8553-127">Weitere Informationen zum Implementieren von **SetLimits** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="f8553-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="f8553-128">Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="f8553-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8553-129">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="f8553-129">MFCMAPI reference</span></span>

<span data-ttu-id="f8553-130">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f8553-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8553-131">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f8553-131">**File**</span></span>|<span data-ttu-id="f8553-132">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f8553-132">**Function**</span></span>|<span data-ttu-id="f8553-133">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="f8553-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8553-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="f8553-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="f8553-135">CMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="f8553-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="f8553-136">MFCMAPI verwendet die **IMAPIProgress::SetLimits-Methode,** um die maximalen und minimalen Grenzwerte und Flags für das Progress-Objekt zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="f8553-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8553-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8553-137">See also</span></span>



[<span data-ttu-id="f8553-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="f8553-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="f8553-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="f8553-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="f8553-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="f8553-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="f8553-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8553-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="f8553-142">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f8553-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f8553-143">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="f8553-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="f8553-144">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="f8553-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


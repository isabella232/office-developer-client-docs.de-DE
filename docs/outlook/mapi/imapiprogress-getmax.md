---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436202"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="691e4-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="691e4-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="691e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="691e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="691e4-105">Gibt die maximale Anzahl von Elementen im Vorgang zurück, für die Statusinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="691e4-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="691e4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="691e4-106">Parameters</span></span>

 <span data-ttu-id="691e4-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="691e4-107">_lpulMax_</span></span>
  
> <span data-ttu-id="691e4-108">[out] Ein Zeiger auf die maximale Anzahl von Elementen im Vorgang.</span><span class="sxs-lookup"><span data-stu-id="691e4-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="691e4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="691e4-109">Return value</span></span>

<span data-ttu-id="691e4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="691e4-110">S_OK</span></span> 
  
> <span data-ttu-id="691e4-111">Die maximale Anzahl von Elementen im Vorgang wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="691e4-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="691e4-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="691e4-112">Remarks</span></span>

<span data-ttu-id="691e4-113">Der Maximalwert stellt das Ende des Vorgangs in numerischer Form dar.</span><span class="sxs-lookup"><span data-stu-id="691e4-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="691e4-114">Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="691e4-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="691e4-115">Der Wert der Kennzeicheneinstellung wirkt sich darauf aus, ob das progress-Objekt den maximalen Wert als lokal oder global versteht.</span><span class="sxs-lookup"><span data-stu-id="691e4-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="691e4-116">Wenn das MAPI_TOP_LEVEL festgelegt ist, wird der maximal zulässige Wert als global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="691e4-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="691e4-117">Wenn MAPI_TOP_LEVEL festgelegt ist, wird der maximal zulässige Wert als lokal betrachtet, und Anbieter verwenden ihn intern, um den Fortschritt für Unterobjekte auf niedrigerer Ebene anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="691e4-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="691e4-118">Progress-Objekte speichern den lokalen Maximalwert nur, um ihn über einen **GetMax-Aufruf** an einen Anbieter zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="691e4-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="691e4-119">Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="691e4-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="691e4-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="691e4-120">Notes to implementers</span></span>

<span data-ttu-id="691e4-121">Initialisieren Sie den Maximalwert auf 1000.</span><span class="sxs-lookup"><span data-stu-id="691e4-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="691e4-122">Dienstanbieter können diesen Wert durch Aufrufen der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="691e4-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="691e4-123">Weitere Informationen zum Implementieren von **GetMax** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="691e4-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="691e4-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="691e4-124">MFCMAPI reference</span></span>

<span data-ttu-id="691e4-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="691e4-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="691e4-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="691e4-126">**File**</span></span>|<span data-ttu-id="691e4-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="691e4-127">**Function**</span></span>|<span data-ttu-id="691e4-128">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="691e4-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="691e4-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="691e4-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="691e4-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="691e4-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="691e4-131">MFCMAPI verwendet die **IMAPIProgress::GetMax-Methode,** um den maximalen Wert für das Progress-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="691e4-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="691e4-132">Gibt 1000 zurück, es sei denn, mit der **IMAPIProgress::SetLimits-Methode** wurden zuvor Grenzwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="691e4-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="691e4-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="691e4-133">See also</span></span>



[<span data-ttu-id="691e4-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="691e4-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="691e4-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="691e4-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="691e4-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="691e4-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="691e4-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="691e4-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="691e4-138">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="691e4-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="691e4-139">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="691e4-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="691e4-140">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="691e4-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


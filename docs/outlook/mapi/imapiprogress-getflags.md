---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423643"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="eab69-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="eab69-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="eab69-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eab69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eab69-105">Gibt Kennzeicheneinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der Fortschrittsinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="eab69-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="eab69-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eab69-106">Parameters</span></span>

 <span data-ttu-id="eab69-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="eab69-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="eab69-108">[out] Eine Bitmaske mit Flags, die die Vorgangsebene steuert, auf der Fortschrittsinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="eab69-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="eab69-109">Das folgende Flag kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="eab69-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="eab69-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="eab69-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="eab69-111">Der Fortschritt wird für das Objekt auf oberster Ebene berechnet, das vom Client zum Starten des Vorgangs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eab69-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="eab69-112">Das Objekt auf oberster Ebene in einem Ordnerkopievorgang ist beispielsweise der Ordner, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="eab69-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="eab69-113">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Fortschritt für ein Objekt auf niedrigerer Ebene oder für ein Unterobjekt berechnet.</span><span class="sxs-lookup"><span data-stu-id="eab69-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="eab69-114">Im Ordnerkopievorgang ist ein Objekt der unteren Ebene einer der Unterordner im Ordner, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="eab69-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eab69-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eab69-115">Return value</span></span>

<span data-ttu-id="eab69-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="eab69-116">S_OK</span></span> 
  
> <span data-ttu-id="eab69-117">Der Flags-Wert wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eab69-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eab69-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eab69-118">Remarks</span></span>

<span data-ttu-id="eab69-119">MIT MAPI können Dienstanbieter mit dem Flag MAPI_TOP_LEVEL zwischen Objekten der obersten Ebene und Unterobjekten unterscheiden, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress-Implementierung](imapiprogressiunknown.md) verwenden können, um den Fortschritt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="eab69-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="eab69-120">Dies bewirkt, dass die Anzeige des Indikators reibungslos in einer einzigen positiven Richtung fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="eab69-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="eab69-121">Ob das MAPI_TOP_LEVEL festgelegt ist, bestimmt, wie Dienstanbieter die anderen Parameter in nachfolgenden Aufrufen des Progress-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="eab69-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="eab69-122">Der von **GetFlags** zurückgegebene Wert wird zunächst vom Implementier und anschließend vom Dienstanbieter über einen Aufruf der [IMAPIProgress::SetLimits-Methode](imapiprogress-setlimits.md) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eab69-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eab69-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="eab69-123">Notes to implementers</span></span>

<span data-ttu-id="eab69-124">Initialisieren Sie immer das Flag, MAPI_TOP_LEVEL und verlassen Sie sich dann auf Dienstanbieter, um es zu löschen, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="eab69-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="eab69-125">Dienstanbieter können das Flag löschen und zurücksetzen, indem sie die **IMAPIProgress::SetLimits-Methode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eab69-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="eab69-126">Weitere Informationen zum Implementieren von **GetFlags** und den anderen **IMAPIProgress-Methoden** finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="eab69-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="eab69-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eab69-127">Notes to callers</span></span>

<span data-ttu-id="eab69-128">Wenn Sie eine Statusanzeige anzeigen, rufen Sie im ERSTEN Schritt **IMAPIProgress::GetFlags auf.**</span><span class="sxs-lookup"><span data-stu-id="eab69-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="eab69-129">Der zurückgegebene Wert sollte MAPI_TOP_LEVEL werden, da alle Implementierungen den Inhalt des  _lpulFlags-Parameters_ auf diesen Wert initialisieren.</span><span class="sxs-lookup"><span data-stu-id="eab69-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="eab69-130">Weitere Informationen zur Reihenfolge der Aufrufe eines Statusobjekts finden Sie [unter Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="eab69-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eab69-131">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="eab69-131">MFCMAPI reference</span></span>

<span data-ttu-id="eab69-132">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="eab69-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eab69-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="eab69-133">**File**</span></span>|<span data-ttu-id="eab69-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="eab69-134">**Function**</span></span>|<span data-ttu-id="eab69-135">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="eab69-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eab69-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="eab69-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="eab69-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="eab69-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="eab69-138">MFCMAPI verwendet die **IMAPIProgress::GetFlags-Methode,** um zu bestimmen, welche Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eab69-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="eab69-139">Gibt MAPI_TOP_LEVEL zurück, es sei denn, Flags wurden mithilfe der **IMAPIProgress::SetLimits-Methode** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eab69-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eab69-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eab69-140">See also</span></span>



[<span data-ttu-id="eab69-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="eab69-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="eab69-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eab69-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="eab69-143">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="eab69-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="eab69-144">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="eab69-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="eab69-145">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="eab69-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


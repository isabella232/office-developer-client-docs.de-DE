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
# <a name="imapiprogressgetflags"></a><span data-ttu-id="b0d1b-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b0d1b-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="b0d1b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0d1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0d1b-105">Gibt Flageinstellungen aus dem Progress-Objekt für die Vorgangsebene zurück, auf der die Statusinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b0d1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0d1b-106">Parameters</span></span>

 <span data-ttu-id="b0d1b-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0d1b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b0d1b-108">Out Eine Bitmaske von Flags, die die Vorgangsebene steuert, auf der die Statusinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="b0d1b-109">Das folgende Flag kann zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="b0d1b-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="b0d1b-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b0d1b-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="b0d1b-111">Der Fortschritt wird für das Objekt der obersten Ebene, das Objekt, das vom Client zum Starten des Vorgangs aufgerufen wird, berechnet.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="b0d1b-112">Beispielsweise ist das Objekt der obersten Ebene in einem Ordner Kopiervorgang der Ordner, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="b0d1b-113">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird Progress für ein Objekt auf niedrigerer Ebene oder ein Subobjekt berechnet.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="b0d1b-114">Im Ordner Kopiervorgang ist ein Objekt auf niedrigerer Ebene einer der Unterordner in dem Ordner, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0d1b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0d1b-115">Return value</span></span>

<span data-ttu-id="b0d1b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0d1b-116">S_OK</span></span> 
  
> <span data-ttu-id="b0d1b-117">Der Flags-Wert wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0d1b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0d1b-118">Remarks</span></span>

<span data-ttu-id="b0d1b-119">Mit MAPI können Dienstanbieter zwischen Objekten auf oberster Ebene und Unterobjekten mit dem MAPI_TOP_LEVEL-Flag differenzieren, sodass alle an einem Vorgang beteiligten Objekte dieselbe [IMAPIProgress](imapiprogressiunknown.md) -Implementierung zum Anzeigen des Fortschritts verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="b0d1b-120">Dadurch wird die Anzeige des Indikators reibungslos in eine einzelne positive Richtung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="b0d1b-121">Ob das MAPI_TOP_LEVEL-Flag festgelegt ist, bestimmt, wie Dienstanbieter die anderen Parameter in nachfolgenden Aufrufen des Progress-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="b0d1b-122">Der von GetFlags zurückgegebene Wert wird anfänglich durch den Implementierer und anschließend durch den Dienstanbieter durch einen Aufruf der [IMAPIProgress::](imapiprogress-setlimits.md) setlimits-Methode festgelegt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b0d1b-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b0d1b-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b0d1b-123">Notes to implementers</span></span>

<span data-ttu-id="b0d1b-124">Initialisieren Sie das Flag immer für MAPI_TOP_LEVEL, und verlassen Sie sich dann auf Dienstanbieter, um es bei Bedarf zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="b0d1b-125">Dienstanbieter können das Flag löschen und zurücksetzen, indem Sie die **IMAPIProgress::** setlimits-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="b0d1b-126">Weitere Informationen zum Implementieren von GetFlags und den anderen **IMAPIProgress** -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b0d1b-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0d1b-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b0d1b-127">Notes to callers</span></span>

<span data-ttu-id="b0d1b-128">Wenn Sie eine Statusanzeige anzeigen, machen Sie Ihren ersten Aufruf einen Aufruf von **IMAPIProgress::** GetFlags.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="b0d1b-129">Der zurückgegebene Wert sollte MAPI_TOP_LEVEL sein, da alle Implementierungen den Inhalt des _lpulFlags_ -Parameters auf diesen Wert initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="b0d1b-130">Weitere Informationen zur Abfolge von Aufrufen eines Progress-Objekts finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b0d1b-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b0d1b-131">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b0d1b-131">MFCMAPI reference</span></span>

<span data-ttu-id="b0d1b-132">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b0d1b-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b0d1b-133">**File**</span></span>|<span data-ttu-id="b0d1b-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b0d1b-134">**Function**</span></span>|<span data-ttu-id="b0d1b-135">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="b0d1b-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0d1b-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="b0d1b-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="b0d1b-137">CMAPIProgress:: GetFlags</span><span class="sxs-lookup"><span data-stu-id="b0d1b-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="b0d1b-138">MFCMAPI verwendet die **IMAPIProgress::** GetFlags-Methode, um zu bestimmen, welche Flags festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="b0d1b-139">Gibt MAPI_TOP_LEVEL zurück, es sei denn, Flags wurden mithilfe der **IMAPIProgress::** setlimits-Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0d1b-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0d1b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0d1b-140">See also</span></span>



[<span data-ttu-id="b0d1b-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="b0d1b-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="b0d1b-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0d1b-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="b0d1b-143">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b0d1b-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b0d1b-144">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="b0d1b-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="b0d1b-145">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="b0d1b-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792257"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="b69a2-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b69a2-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="b69a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b69a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b69a2-105">Gibt kennzeichnen Einstellungen aus dem Fortschritt-Objekt für die Ebene des Vorgangs auf die Fortschrittsinformationen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="b69a2-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b69a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b69a2-106">Parameters</span></span>

 <span data-ttu-id="b69a2-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b69a2-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b69a2-108">[out] Eine Bitmaske aus Flags, die die Ebene des Vorgangs steuert, welche Fortschritt Informationen berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b69a2-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="b69a2-109">Das folgende Flag können zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="b69a2-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="b69a2-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b69a2-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="b69a2-111">Status wird für das Objekt der obersten Ebene, das Objekt berechnet wird, die durch den Client auf die Operation beginnen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b69a2-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="b69a2-112">Beispielsweise ist das Objekt der obersten Ebene in einem Ordnerkopiervorgang den Ordner, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="b69a2-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="b69a2-113">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird für einen niedrigeren Level-Objekt oder Unterobjekts Fortschritt berechnet.</span><span class="sxs-lookup"><span data-stu-id="b69a2-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="b69a2-114">In den Ordnerkopiervorgang ist eine niedrigere Level-Objekt eine Unterordner in den Ordner, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="b69a2-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b69a2-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b69a2-115">Return value</span></span>

<span data-ttu-id="b69a2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b69a2-116">S_OK</span></span> 
  
> <span data-ttu-id="b69a2-117">Der Wert des Flags wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b69a2-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b69a2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b69a2-118">Remarks</span></span>

<span data-ttu-id="b69a2-119">MAPI-Dienstanbieter zur Unterscheidung zwischen Objekte der obersten Ebene ermöglicht und Unterobjekte mit dem MAPI_TOP_LEVEL-Flag, damit alle Objekte in einem Vorgang beteiligt können die gleiche [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b69a2-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="b69a2-120">Daraufhin wird die Anzeige Indikator reibungslos in einer Richtung positive fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b69a2-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="b69a2-121">Ob das Flag MAPI_TOP_LEVEL festgelegt ist bestimmt, wie-Dienstanbieter die anderen Parameter in nachfolgenden Aufrufe der Fortschritt-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="b69a2-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="b69a2-122">Der Wert von **"GetFlags"** wird zunächst von der Implementierung und anschließend vom Dienstanbieter durch einen Aufruf an die [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b69a2-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b69a2-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b69a2-123">Notes to implementers</span></span>

<span data-ttu-id="b69a2-124">Initialisieren Sie das Flag MAPI_TOP_LEVEL immer, und klicken Sie dann stützen Sie sich auf Dienstanbieter, ihn bei Bedarf zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b69a2-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="b69a2-125">Dienstanbieter können deaktivieren und das Flag zurücksetzen, indem Sie die **IMAPIProgress::SetLimits** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b69a2-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="b69a2-126">Weitere Informationen zum Implementieren von **"GetFlags"** und die anderen **IMAPIProgress** Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b69a2-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b69a2-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b69a2-127">Notes to callers</span></span>

<span data-ttu-id="b69a2-128">Wenn Sie eine Statusanzeige anzeigen, stellen Sie Ihre erste Aufruf einen Anruf an **IMAPIProgress::GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="b69a2-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="b69a2-129">Der zurückgegebene Wert sollte MAPI_TOP_LEVEL, da allen Implementierungen den Inhalt des Parameters _LpulFlags_ auf diesen Wert initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b69a2-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="b69a2-130">Weitere Informationen zur Reihenfolge der Aufrufe eines Objekts Fortschritt finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b69a2-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b69a2-131">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="b69a2-131">MFCMAPI reference</span></span>

<span data-ttu-id="b69a2-132">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b69a2-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b69a2-133">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b69a2-133">**File**</span></span>|<span data-ttu-id="b69a2-134">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b69a2-134">**Function**</span></span>|<span data-ttu-id="b69a2-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b69a2-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b69a2-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="b69a2-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="b69a2-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b69a2-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="b69a2-138">MFCMAPI (engl.) wird die **IMAPIProgress::GetFlags** -Methode verwendet, um zu bestimmen, welche Attribute festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b69a2-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="b69a2-139">Gibt MAPI_TOP_LEVEL zurück, es sei denn, Flags mit der **IMAPIProgress::SetLimits** -Methode festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="b69a2-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b69a2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b69a2-140">See also</span></span>



[<span data-ttu-id="b69a2-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="b69a2-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="b69a2-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b69a2-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="b69a2-143">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b69a2-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b69a2-144">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="b69a2-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="b69a2-145">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="b69a2-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792256"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="04349-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="04349-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="04349-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04349-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04349-105">Gibt die maximale Anzahl von Elementen in den Vorgang für den Fortschritt Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="04349-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="04349-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04349-106">Parameters</span></span>

 <span data-ttu-id="04349-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="04349-107">_lpulMax_</span></span>
  
> <span data-ttu-id="04349-108">[out] Ein Zeiger auf die maximale Anzahl von Elementen in den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="04349-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04349-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="04349-109">Return value</span></span>

<span data-ttu-id="04349-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="04349-110">S_OK</span></span> 
  
> <span data-ttu-id="04349-111">Die maximale Anzahl von Elementen in der Vorgang wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="04349-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04349-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="04349-112">Remarks</span></span>

<span data-ttu-id="04349-113">Der maximale Wert stellt das Ende des Vorgangs in numerische Form dar.</span><span class="sxs-lookup"><span data-stu-id="04349-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="04349-114">Der Wert kann einen globalen Höchstwert zur Darstellung des Bereichs der gesamte Fortschrittsanzeige oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige sein.</span><span class="sxs-lookup"><span data-stu-id="04349-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="04349-115">Der Wert der Einstellung Flag wirkt sich auf, ob das Objekt Fortschritt den Höchstwert lokal oder global sein versteht.</span><span class="sxs-lookup"><span data-stu-id="04349-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="04349-116">Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, der maximale Wert gilt als globale und wird verwendet, um den Status für den gesamten Vorgang zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="04349-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="04349-117">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, der maximale Wert gilt als lokale und Anbieter mit es intern Fortschritt für unteren Ebene Unterobjekte angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04349-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="04349-118">Fortschritt Objekte speichern den lokalen Höchstwert nur, um einen Anbieter durch einen Aufruf **GetMax** wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="04349-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="04349-119">Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="04349-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="04349-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="04349-120">Notes to implementers</span></span>

<span data-ttu-id="04349-121">Initialisieren Sie den Höchstwert bis 1000 ein.</span><span class="sxs-lookup"><span data-stu-id="04349-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="04349-122">Dienstanbieter können durch Aufrufen der Methode [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) dieser Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="04349-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="04349-123">Weitere Informationen zum Implementieren von **GetMax** und anderen [IMAPIProgress](imapiprogressiunknown.md) Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="04349-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="04349-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="04349-124">MFCMAPI reference</span></span>

<span data-ttu-id="04349-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="04349-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="04349-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="04349-126">**File**</span></span>|<span data-ttu-id="04349-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="04349-127">**Function**</span></span>|<span data-ttu-id="04349-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="04349-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04349-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="04349-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="04349-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="04349-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="04349-131">MFCMAPI (engl.) verwendet die **IMAPIProgress::GetMax** -Methode, um den Höchstwert für den Fortschritt-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04349-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="04349-132">Gibt 1000 zurück, es sei denn, Grenzwerte zuvor mit der **IMAPIProgress::SetLimits** -Methode festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="04349-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04349-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04349-133">See also</span></span>



[<span data-ttu-id="04349-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="04349-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="04349-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="04349-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="04349-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="04349-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="04349-137">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04349-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="04349-138">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="04349-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="04349-139">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="04349-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="04349-140">Implementieren eine Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="04349-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cff866ce73eb6ada45a2b629a6c95c69ad189045
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587824"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="3f7eb-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="3f7eb-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="3f7eb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f7eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f7eb-105">Gibt den kleinsten Wert in der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode für die Fortschritt Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="3f7eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f7eb-106">Parameters</span></span>

 <span data-ttu-id="3f7eb-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="3f7eb-107">_lpulMin_</span></span>
  
> <span data-ttu-id="3f7eb-108">[out] Ein Zeiger auf die minimale Anzahl von Elementen in den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f7eb-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3f7eb-109">Return value</span></span>

<span data-ttu-id="3f7eb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f7eb-110">S_OK</span></span> 
  
> <span data-ttu-id="3f7eb-111">Die minimale Anzahl von Elementen in der Vorgang wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f7eb-112">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3f7eb-112">Remarks</span></span>

<span data-ttu-id="3f7eb-113">Der Mindestwert stellt den Anfang des Vorgangs in numerische Form dar.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="3f7eb-114">Der Wert kann einen globalen Höchstwert zur Darstellung des Bereichs der gesamte Fortschrittsanzeige oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige sein.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="3f7eb-115">Der Wert der Einstellung Flag bestimmt, ob das Objekt Fortschritt den Mindestwert lokal oder global sein versteht.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="3f7eb-116">Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, wird der Mindestwert gilt als globale und wird verwendet, um den Status für den gesamten Vorgang zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="3f7eb-117">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, gilt der Mindestwert lokalen und Anbieter mit es intern Fortschritt für unteren Ebene Unterobjekte angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="3f7eb-118">Fortschritt Objekte speichern den lokalen Mindestwert nur, um einen Anbieter durch einen Aufruf **GetMin** wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3f7eb-119">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="3f7eb-119">Notes to implementers</span></span>

<span data-ttu-id="3f7eb-120">Initialisieren Sie den kleinsten Wert auf 1.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="3f7eb-121">Dienstanbieter können durch Aufrufen der Methode **IMAPIProgress::SetLimits** dieser Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="3f7eb-122">Weitere Informationen zum Implementieren von **GetMin** und anderen [IMAPIProgress](imapiprogressiunknown.md) Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="3f7eb-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="3f7eb-123">Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="3f7eb-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f7eb-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="3f7eb-124">MFCMAPI reference</span></span>

<span data-ttu-id="3f7eb-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f7eb-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3f7eb-126">**File**</span></span>|<span data-ttu-id="3f7eb-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3f7eb-127">**Function**</span></span>|<span data-ttu-id="3f7eb-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3f7eb-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f7eb-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="3f7eb-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="3f7eb-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="3f7eb-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="3f7eb-131">MFCMAPI (engl.) verwendet die **IMAPIProgress::GetMin** -Methode, um den kleinsten Wert für die Statusanzeige zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="3f7eb-132">Gibt 1 zurück, es sei denn, Grenzwerte zuvor durch Aufrufen der Methode **IMAPIProgress::SetLimits** festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="3f7eb-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f7eb-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f7eb-133">See also</span></span>



[<span data-ttu-id="3f7eb-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="3f7eb-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="3f7eb-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="3f7eb-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="3f7eb-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="3f7eb-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="3f7eb-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f7eb-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="3f7eb-138">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3f7eb-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="3f7eb-139">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="3f7eb-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="3f7eb-140">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="3f7eb-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


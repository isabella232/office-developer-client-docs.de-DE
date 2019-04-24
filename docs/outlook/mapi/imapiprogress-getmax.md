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
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270203"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="1ac10-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="1ac10-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="1ac10-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ac10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ac10-105">Gibt die maximale Anzahl von Elementen in dem Vorgang zurück, für die Statusinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ac10-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="1ac10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ac10-106">Parameters</span></span>

 <span data-ttu-id="1ac10-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="1ac10-107">_lpulMax_</span></span>
  
> <span data-ttu-id="1ac10-108">Out Ein Zeiger auf die maximale Anzahl von Elementen in dem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1ac10-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ac10-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ac10-109">Return value</span></span>

<span data-ttu-id="1ac10-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ac10-110">S_OK</span></span> 
  
> <span data-ttu-id="1ac10-111">Die maximale Anzahl von Elementen in dem Vorgang wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1ac10-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ac10-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ac10-112">Remarks</span></span>

<span data-ttu-id="1ac10-113">Der Maximalwert stellt das Ende des Vorgangs in numerischer Form dar.</span><span class="sxs-lookup"><span data-stu-id="1ac10-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="1ac10-114">Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ac10-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="1ac10-115">Der Wert der Flag-Einstellung wirkt sich darauf aus, ob das Progress-Objekt den Maximalwert auf "lokal" oder "Global" versteht.</span><span class="sxs-lookup"><span data-stu-id="1ac10-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="1ac10-116">Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, wird der Höchstwert als Global betrachtet und zum Berechnen des Fortschritts für den gesamten Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ac10-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="1ac10-117">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Maximalwert als lokal betrachtet, und die Anbieter verwenden ihn intern, um den Fortschritt für unter Objekte auf niedrigerer Ebene anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1ac10-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="1ac10-118">Progress-Objekte speichern den lokalen Maximalwert nur, um ihn über einen **GetMax** -Aufruf an einen Anbieter zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1ac10-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="1ac10-119">Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1ac10-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1ac10-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="1ac10-120">Notes to implementers</span></span>

<span data-ttu-id="1ac10-121">Initialisieren Sie den Höchstwert auf 1000.</span><span class="sxs-lookup"><span data-stu-id="1ac10-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="1ac10-122">Dienstanbieter können diesen Wert durch Aufrufen der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="1ac10-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="1ac10-123">Weitere Informationen zum Implementieren von **GetMax** und den anderen [IMAPIProgress](imapiprogressiunknown.md) -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="1ac10-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ac10-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1ac10-124">MFCMAPI reference</span></span>

<span data-ttu-id="1ac10-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1ac10-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ac10-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1ac10-126">**File**</span></span>|<span data-ttu-id="1ac10-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1ac10-127">**Function**</span></span>|<span data-ttu-id="1ac10-128">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="1ac10-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ac10-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="1ac10-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="1ac10-130">CMAPIProgress:: GetMax</span><span class="sxs-lookup"><span data-stu-id="1ac10-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="1ac10-131">MFCMAPI verwendet die **IMAPIProgress:: GetMax** -Methode, um den Maximalwert für das Progress-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ac10-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="1ac10-132">Gibt 1000 zurück, es sei denn, es wurden zuvor Werte mit der **IMAPIProgress::** setlimits-Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1ac10-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ac10-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ac10-133">See also</span></span>



[<span data-ttu-id="1ac10-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="1ac10-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="1ac10-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="1ac10-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="1ac10-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="1ac10-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="1ac10-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ac10-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="1ac10-138">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1ac10-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1ac10-139">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="1ac10-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="1ac10-140">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="1ac10-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


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
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331682"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="da77b-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="da77b-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="da77b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da77b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da77b-105">Gibt den Mindestwert in der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)-Methode an, für die Statusinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="da77b-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="da77b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da77b-106">Parameters</span></span>

 <span data-ttu-id="da77b-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="da77b-107">_lpulMin_</span></span>
  
> <span data-ttu-id="da77b-108">[out] Ein Verweis auf die minimale Anzahl von Elementen in dem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="da77b-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da77b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da77b-109">Return value</span></span>

<span data-ttu-id="da77b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="da77b-110">S_OK</span></span> 
  
> <span data-ttu-id="da77b-111">Die minimale Anzahl von Elementen in dem Vorgang wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="da77b-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da77b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="da77b-112">Remarks</span></span>

<span data-ttu-id="da77b-113">Der Mindestwert stellt den Beginn des Vorgangs in numerischer Form dar.</span><span class="sxs-lookup"><span data-stu-id="da77b-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="da77b-114">Der Wert kann ein globaler Maximalwert sein, der verwendet wird, um den Umfang der gesamten Statusanzeige darzustellen, oder ein lokaler Wert, der zum Darstellen eines Teils der Anzeige verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da77b-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="da77b-115">Der Wert der Flageinstellung wirkt sich darauf aus, ob das Statusobjekt versteht, dass der Mindestwert lokal oder global ist.</span><span class="sxs-lookup"><span data-stu-id="da77b-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="da77b-116">Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, wird der Mindestwert als global betrachtet und zum Berechnen des Status für den gesamten Vorgang verwendet.</span><span class="sxs-lookup"><span data-stu-id="da77b-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="da77b-117">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, wird der Mindestwert als lokal betrachtet und von Anbietern intern verwendet, um den Status von Unterobjekten auf niedrigeren Ebenen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="da77b-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="da77b-118">Statusobjekte speichern den lokalen Mindestwert nur, um diesen an einen Anbieter über einen **GetMin**-Aufruf zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="da77b-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="da77b-119">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="da77b-119">Notes to implementers</span></span>

<span data-ttu-id="da77b-120">Initialisieren Sie den Mindestwert auf 1.</span><span class="sxs-lookup"><span data-stu-id="da77b-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="da77b-121">Dienstanbieter können diesen Wert durch Aufrufen der **IMAPIProgress::SetLimits**-Methode zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="da77b-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="da77b-122">Weitere Informationen zum Implementieren von **GetMin** und der anderen [IMAPIProgress](imapiprogressiunknown.md)-Methoden finden Sie unter [Implementieren eines Statusindikators](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="da77b-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="da77b-123">Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="da77b-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="da77b-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="da77b-124">MFCMAPI reference</span></span>

<span data-ttu-id="da77b-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da77b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da77b-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="da77b-126">**File**</span></span>|<span data-ttu-id="da77b-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="da77b-127">**Function**</span></span>|<span data-ttu-id="da77b-128">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="da77b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da77b-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="da77b-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="da77b-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="da77b-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="da77b-131">MFCMAPI verwendet die **IMAPIProgress::GetMin**-Methode, um den kleinsten Wert für die Statusanzeige abzurufen.</span><span class="sxs-lookup"><span data-stu-id="da77b-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="da77b-132">Gibt 1 zurück, es sei denn, zuvor wurden durch Aufrufen der **IMAPIProgress::SetLimits**-Methode Einschränkungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da77b-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da77b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da77b-133">See also</span></span>



[<span data-ttu-id="da77b-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="da77b-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="da77b-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="da77b-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="da77b-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="da77b-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="da77b-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da77b-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="da77b-138">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="da77b-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="da77b-139">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="da77b-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="da77b-140">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="da77b-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


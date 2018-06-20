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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 14abfaadcdb1710a7cb8275c8f82d502aea8300e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792264"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="8e329-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="8e329-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="8e329-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e329-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e329-105">Legt die oberen und unteren Grenzwerten für die Anzahl der Elemente in den Vorgang und die Kennzeichen, die steuern, wie die Statusinformationen für den Vorgang berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="8e329-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8e329-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e329-106">Parameters</span></span>

 <span data-ttu-id="8e329-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="8e329-107">_lpulMin_</span></span>
  
> <span data-ttu-id="8e329-108">[in] Ein Zeiger auf eine Variable, die die untere Grenze von Elementen in den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="8e329-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="8e329-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="8e329-109">_lpulMax_</span></span>
  
> <span data-ttu-id="8e329-110">[in] Ein Zeiger auf eine Variable, die den oberen Grenzwert von Elementen in den Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="8e329-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="8e329-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e329-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="8e329-112">[in] Eine Bitmaske aus Flags, die die Ebene des Vorgangs steuert, welche Fortschritt Informationen berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="8e329-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="8e329-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8e329-113">The following flag can be set:</span></span>
    
<span data-ttu-id="8e329-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="8e329-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="8e329-115">Verwendet die Werte in der [IMAPIProgress::Progress](imapiprogress-progress.md) -Methode _UlCount_ und _UlTotal_ -Parameter, die derzeit verarbeiteten Element und die gesamte Elemente, die jeweils auf Inkrement Bearbeitung auf den Vorgang anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e329-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="8e329-116">Wenn dieses Flag festgelegt ist, können die Werte der globalen unteren und oberen Grenzwerte festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e329-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e329-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8e329-117">Return value</span></span>

<span data-ttu-id="8e329-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e329-118">S_OK</span></span> 
  
> <span data-ttu-id="8e329-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8e329-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e329-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e329-120">Remarks</span></span>

<span data-ttu-id="8e329-121">Dienstanbieter rufen die **IMAPIProgress::SetLimits** -Methode festlegen oder Entfernen des Kennzeichens MAPI_TOP_LEVEL und lokaler und globaler minimale und maximale Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="8e329-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="8e329-122">Der Wert der Einstellung Flag bestimmt, ob das Fortschritt Objekt lokal oder global werden der höchste und der niedrigste versteht.</span><span class="sxs-lookup"><span data-stu-id="8e329-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="8e329-123">Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, werden diese Werte als global gelten und werden verwendet, um den Status für den gesamten Vorgang zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8e329-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="8e329-124">Fortschritt Objekte Initialisieren der globalen Mindestwert 1 und der globalen Höchstwert bis 1000.</span><span class="sxs-lookup"><span data-stu-id="8e329-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="8e329-125">Wenn MAPI_TOP_LEVEL nicht festgelegt ist, werden der höchste und der niedrigste als lokale betrachtet und Anbieter für deren Verwendung intern für unteren Ebene Unterobjekte Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e329-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="8e329-126">Fortschritt Objekte speichern die lokalen minimale und maximale Werte, sodass sie-Anbieter zurückgegeben werden können, wenn die Methoden [IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8e329-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="8e329-127">Weitere Informationen zum Implementieren von **SetLimits** und anderen [IMAPIProgress](imapiprogressiunknown.md) Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="8e329-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="8e329-128">Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="8e329-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e329-129">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="8e329-129">MFCMAPI reference</span></span>

<span data-ttu-id="8e329-130">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8e329-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e329-131">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8e329-131">**File**</span></span>|<span data-ttu-id="8e329-132">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8e329-132">**Function**</span></span>|<span data-ttu-id="8e329-133">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8e329-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e329-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="8e329-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="8e329-135">CMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="8e329-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="8e329-136">MFCMAPI (engl.) verwendet die **IMAPIProgress::SetLimits** -Methode, um die maximal- und Minimalwerte Grenzwerte und die Kennzeichen für den Fortschritt-Objekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8e329-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e329-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e329-137">See also</span></span>



[<span data-ttu-id="8e329-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="8e329-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="8e329-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="8e329-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="8e329-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="8e329-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="8e329-141">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e329-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="8e329-142">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8e329-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8e329-143">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="8e329-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="8e329-144">Implementieren eine Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="8e329-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


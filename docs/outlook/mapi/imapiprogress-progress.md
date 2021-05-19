---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435495"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="bdeb2-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="bdeb2-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="bdeb2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdeb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdeb2-105">Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, der zum Abschluss des Vorgangs erfolgt.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="bdeb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdeb2-106">Parameters</span></span>

 <span data-ttu-id="bdeb2-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="bdeb2-107">_ulValue_</span></span>
  
> <span data-ttu-id="bdeb2-108">[in] Eine Zahl, die die aktuelle Fortschrittsstufe (berechnet aus den  _Parametern ulCount_ und  _ulTotal_ oder  _den Parametern lpulMin_ und  _lpulMax_ der [IMAPIProgress::SetLimits-Methode)](imapiprogress-setlimits.md) zwischen dem globalen unteren Grenzwert und dem globalen oberen Grenzwert angibt.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="bdeb2-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="bdeb2-109">_ulCount_</span></span>
  
> <span data-ttu-id="bdeb2-110">[in] Eine Zahl, die das aktuell verarbeitete Element relativ zur Gesamtsumme angibt.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="bdeb2-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="bdeb2-111">_ulTotal_</span></span>
  
> <span data-ttu-id="bdeb2-112">[in] Die Gesamtanzahl der Während des Vorgangs zu verarbeitende Elemente.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bdeb2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdeb2-113">Return value</span></span>

<span data-ttu-id="bdeb2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="bdeb2-114">S_OK</span></span> 
  
> <span data-ttu-id="bdeb2-115">Die Statusanzeige wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="bdeb2-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="bdeb2-116">Notes to implementers</span></span>

<span data-ttu-id="bdeb2-117">Der  _ulValue-Parameter_ entspricht dem globalen Minimalwert nur zu Beginn des Vorgangs und dem globalen Maximalwert erst nach Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="bdeb2-118">Verwenden Sie  _die ulCount-_ und  _ulTotal-Parameter,_ wenn verfügbar, um eine optionale Meldung wie "5 von 10 abgeschlossene Elemente" anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="bdeb2-119">Wenn  _ulCount_ und  _ulTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="bdeb2-120">Einige Dienstanbieter legen diese Parameter auf 0 fest, um anzugeben, dass sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="bdeb2-121">In dieser Situation ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="bdeb2-122">Einige Dienstanbieter übergeben jedes Mal 0 für diese Parameter.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="bdeb2-123">Weitere Informationen zum Implementieren von **Progress** und den anderen [IMAPIProgress-Methoden](imapiprogressiunknown.md) finden Sie unter [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="bdeb2-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bdeb2-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="bdeb2-124">Notes to callers</span></span>

<span data-ttu-id="bdeb2-125">Nicht alle drei Parameter für **IMAPIProgress::P rogress** sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="bdeb2-126">Der einzige erforderliche Parameter ist  _ulValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="bdeb2-127">Wenn das MAPI_TOP_LEVEL festgelegt ist, können Sie auch eine Objektanzahl und eine Objektsumme übergeben.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="bdeb2-128">Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 von 10 abgeschlossene Elemente" mit der Statusanzeige zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="bdeb2-129">Wenn Sie alle Nachrichten in einem einzigen Ordner kopieren, legen Sie  _ulTotal_ auf die Gesamtanzahl der zu kopierende Nachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="bdeb2-130">Wenn Sie einen Ordner kopieren, legen Sie  _ulTotal_ auf die Anzahl der Unterordner im Ordner festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="bdeb2-131">Wenn der zu kopierende Ordner keine Unterordner und nur Nachrichten enthält, legen Sie  _ulTotal_ auf 1.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="bdeb2-132">Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="bdeb2-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bdeb2-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="bdeb2-133">MFCMAPI reference</span></span>

<span data-ttu-id="bdeb2-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bdeb2-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="bdeb2-135">**File**</span></span>|<span data-ttu-id="bdeb2-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="bdeb2-136">**Function**</span></span>|<span data-ttu-id="bdeb2-137">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="bdeb2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bdeb2-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="bdeb2-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="bdeb2-139">CMAPIProgress::P rogress</span><span class="sxs-lookup"><span data-stu-id="bdeb2-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="bdeb2-140">MFCMAPI verwendet die **IMAPIProgress::P rogress-Methode,** um die MFCMAPI-Statusleiste mit dem aktuellen Fortschrittsprozentsatz zu aktualisieren, der aus  _uValue_ und den aktuellen Maximal- und Minimalwerten berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="bdeb2-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdeb2-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdeb2-141">See also</span></span>



[<span data-ttu-id="bdeb2-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="bdeb2-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="bdeb2-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdeb2-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="bdeb2-144">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="bdeb2-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bdeb2-145">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="bdeb2-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="bdeb2-146">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="bdeb2-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


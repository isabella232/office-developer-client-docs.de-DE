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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270301"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="9a26f-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="9a26f-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="9a26f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a26f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a26f-105">Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts beim Abschließen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9a26f-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="9a26f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a26f-106">Parameters</span></span>

 <span data-ttu-id="9a26f-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="9a26f-107">_ulValue_</span></span>
  
> <span data-ttu-id="9a26f-108">in Eine Zahl, die die aktuelle Fortschritts Ebene angibt (berechnet aus den Parametern _ulCount_ und _ulTotal_ oder aus den Parametern _lpulMin_ und _lpulMax_ der [IMAPIProgress::](imapiprogress-setlimits.md) setlimits-Methode) zwischen dem globalen untere Grenze und die globale obere Grenze.</span><span class="sxs-lookup"><span data-stu-id="9a26f-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="9a26f-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="9a26f-109">_ulCount_</span></span>
  
> <span data-ttu-id="9a26f-110">in Eine Zahl, die das aktuell verarbeitete Element relativ zum Gesamtwert angibt.</span><span class="sxs-lookup"><span data-stu-id="9a26f-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="9a26f-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="9a26f-111">_ulTotal_</span></span>
  
> <span data-ttu-id="9a26f-112">in Die Gesamtzahl der während des Vorgangs zu verarbeitenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="9a26f-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a26f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a26f-113">Return value</span></span>

<span data-ttu-id="9a26f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a26f-114">S_OK</span></span> 
  
> <span data-ttu-id="9a26f-115">Die Statusanzeige wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9a26f-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9a26f-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9a26f-116">Notes to implementers</span></span>

<span data-ttu-id="9a26f-117">Der Parameter _ulValue_ ist gleich dem globalen Minimalwert nur zu Beginn des Vorgangs und zum globalen Maximalwert nur nach Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="9a26f-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="9a26f-118">Verwenden Sie die _ulCount_ -und _ulTotal_ -Parameter, falls verfügbar, um eine optionale Meldung anzuzeigen, wie etwa "5 Elemente, die von 10 abgeschlossen wurden".</span><span class="sxs-lookup"><span data-stu-id="9a26f-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="9a26f-119">Wenn _ulCount_ und _ulTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a26f-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="9a26f-120">Einige Dienstanbieter haben diese Parameter auf 0 festgelegt, um anzugeben, dass Sie ein Unterobjekt verarbeiten, dessen Fortschritt relativ zu einem übergeordneten Objekt überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="9a26f-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="9a26f-121">In dieser Situation ist es sinnvoll, die Anzeige nur zu ändern, wenn das übergeordnete Objekt den Fortschritt meldet.</span><span class="sxs-lookup"><span data-stu-id="9a26f-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="9a26f-122">Einige Dienstanbieter übergeben jedes Mal 0 für diese Parameter.</span><span class="sxs-lookup"><span data-stu-id="9a26f-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="9a26f-123">Weitere Informationen zum Implementieren des **Fortschritts** und der anderen [IMAPIProgress](imapiprogressiunknown.md) -Methoden finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="9a26f-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9a26f-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9a26f-124">Notes to callers</span></span>

<span data-ttu-id="9a26f-125">Nicht alle drei Parameter für **IMAPIProgress::P rogress** sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9a26f-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="9a26f-126">Der einzige erforderliche Parameter ist _ulValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="9a26f-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="9a26f-127">Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, können Sie auch eine Objektanzahl und ein Objekt insgesamt.</span><span class="sxs-lookup"><span data-stu-id="9a26f-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="9a26f-128">Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 Elemente, die von 10 abgeschlossen wurden" mit der Statusanzeige anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a26f-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="9a26f-129">Wenn Sie alle Nachrichten in einem einzelnen Ordner kopieren, legen Sie _ulTotal_ auf die Gesamtzahl der kopierten Nachrichten fest.</span><span class="sxs-lookup"><span data-stu-id="9a26f-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="9a26f-130">Wenn Sie einen Ordner kopieren, legen Sie _ulTotal_ auf die Anzahl der Unterordner im Ordner fest.</span><span class="sxs-lookup"><span data-stu-id="9a26f-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="9a26f-131">Wenn der zu kopierende Ordner keine Unterordner und nur Nachrichten enthält, legen Sie _ulTotal_ auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="9a26f-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="9a26f-132">Weitere Informationen dazu, wie und wann Statusobjekte aufgerufen werden, finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="9a26f-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9a26f-133">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="9a26f-133">MFCMAPI reference</span></span>

<span data-ttu-id="9a26f-134">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9a26f-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9a26f-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9a26f-135">**File**</span></span>|<span data-ttu-id="9a26f-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="9a26f-136">**Function**</span></span>|<span data-ttu-id="9a26f-137">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="9a26f-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a26f-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="9a26f-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="9a26f-139">CMAPIProgress::P rogress</span><span class="sxs-lookup"><span data-stu-id="9a26f-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="9a26f-140">MFCMAPI verwendet die **IMAPIProgress::P rogress** -Methode, um die MfcMapi-Statusleiste mit dem aktuellen prozentualen Fortschritt zu aktualisieren, berechnet von _uValue_ und den aktuellen maximalen und minimalen Werten.</span><span class="sxs-lookup"><span data-stu-id="9a26f-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a26f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a26f-141">See also</span></span>



[<span data-ttu-id="9a26f-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="9a26f-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="9a26f-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a26f-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="9a26f-144">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="9a26f-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9a26f-145">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="9a26f-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="9a26f-146">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="9a26f-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


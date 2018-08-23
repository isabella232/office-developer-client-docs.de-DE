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
ms.openlocfilehash: 3fc72f008d1c2610de3c74762aabc6231dabbfbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589056"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="fbc92-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="fbc92-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="fbc92-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbc92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbc92-105">Aktualisiert die Statusanzeige mit einer Anzeige des Fortschritts, sobald sie zum Abschluss des Vorgangs vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="fbc92-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="fbc92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc92-106">Parameters</span></span>

 <span data-ttu-id="fbc92-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="fbc92-107">_ulValue_</span></span>
  
> <span data-ttu-id="fbc92-108">[in] Eine Zahl, die dem aktuellen Stand des Fortschritts (der Parameter _UlCount_ und _UlTotal_ oder der Parameter _LpulMin_ und _LpulMax_ der [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode berechnet) zwischen der globalen an Untergrenze und der globalen Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="fbc92-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="fbc92-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="fbc92-109">_ulCount_</span></span>
  
> <span data-ttu-id="fbc92-110">[in] Eine Zahl, die das Element derzeit verarbeitete relativ zur Summe angibt.</span><span class="sxs-lookup"><span data-stu-id="fbc92-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="fbc92-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="fbc92-111">_ulTotal_</span></span>
  
> <span data-ttu-id="fbc92-112">[in] Die Gesamtanzahl von Elementen, die während des Vorgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="fbc92-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fbc92-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fbc92-113">Return value</span></span>

<span data-ttu-id="fbc92-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbc92-114">S_OK</span></span> 
  
> <span data-ttu-id="fbc92-115">Die Statusanzeige wurde erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fbc92-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="fbc92-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="fbc92-116">Notes to implementers</span></span>

<span data-ttu-id="fbc92-117">Der Parameter _UlValue_ werden gleich dem globalen minimalen Wert nur am Anfang des Vorgangs und dem globalen Höchstwert nur nach Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="fbc92-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="fbc92-118">Verwenden Sie die Parameter _UlCount_ und _UlTotal_ , falls verfügbar, um eine optionale Nachricht wie "5 Elemente nicht genügend 10 abgeschlossen." angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fbc92-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="fbc92-119">Wenn _UlCount_ und _UlTotal_ auf 0 festgelegt sind, entscheiden Sie, ob die Statusanzeige visuell zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fbc92-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="fbc92-120">Einige Dienstanbieter legen Sie diesen Parameter auf 0, um anzugeben, dass sie ein Unterobjekt verarbeitet werden, deren Status relativ zu einem übergeordneten Objekt überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="fbc92-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="fbc92-121">In diesem Fall ist es sinnvoll, die Anzeige nur ändern, wenn das übergeordnete Objekt des Fortschritts meldet.</span><span class="sxs-lookup"><span data-stu-id="fbc92-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="fbc92-122">Einige Dienstanbieter übergeben 0 für diese Parameter jedes Mal.</span><span class="sxs-lookup"><span data-stu-id="fbc92-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="fbc92-123">Weitere Informationen zur Verwendung **des Fortschritts** und der andere [IMAPIProgress](imapiprogressiunknown.md) -Methoden implementieren finden Sie unter [Implementieren einer Statusanzeige](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="fbc92-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="fbc92-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="fbc92-124">Notes to callers</span></span>

<span data-ttu-id="fbc92-125">Nicht alle drei Parameter zu **IMAPIProgress::Progress** sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fbc92-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="fbc92-126">Der einzige Parameter, der erforderlich ist ist _UlValue_, eine Zahl, die den Prozentsatz des Fortschritts angibt.</span><span class="sxs-lookup"><span data-stu-id="fbc92-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="fbc92-127">Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, können Sie auch die Anzahl der Objekte und ein Objekt insgesamt übergeben.</span><span class="sxs-lookup"><span data-stu-id="fbc92-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="fbc92-128">Einige Implementierungen verwenden diese Werte, um einen Ausdruck wie "5 Elemente nicht genügend 10 abgeschlossen" mit der Statusanzeige anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fbc92-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="fbc92-129">Wenn Sie alle Nachrichten in einem gemeinsamen Ordner kopieren möchten, legen Sie _UlTotal_ auf die Gesamtzahl der kopierten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="fbc92-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="fbc92-130">Wenn Sie einen Ordner kopieren, legen Sie _UlTotal_ auf die Anzahl der Unterordner im Ordner.</span><span class="sxs-lookup"><span data-stu-id="fbc92-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="fbc92-131">Wenn der Ordner kopiert werden keine Unterordner und nur Nachrichten enthält, setzen Sie _UlTotal_ auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="fbc92-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="fbc92-132">Weitere Informationen dazu, wie und wann ein Fortschritt-Objekt aufrufen finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="fbc92-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fbc92-133">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="fbc92-133">MFCMAPI reference</span></span>

<span data-ttu-id="fbc92-134">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fbc92-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fbc92-135">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fbc92-135">**File**</span></span>|<span data-ttu-id="fbc92-136">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fbc92-136">**Function**</span></span>|<span data-ttu-id="fbc92-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fbc92-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fbc92-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="fbc92-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="fbc92-139">CMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="fbc92-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="fbc92-140">MFCMAPI (engl.) verwendet die **IMAPIProgress::Progress** -Methode zum Aktualisieren der Statusleiste MFCMAPI (engl.) mit den aktuellen Prozentsatz des Fortschritts, aus _uValue_ und die aktuellen Werte der maximal- und Minimalwerte berechnet.</span><span class="sxs-lookup"><span data-stu-id="fbc92-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbc92-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbc92-141">See also</span></span>



[<span data-ttu-id="fbc92-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="fbc92-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="fbc92-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fbc92-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="fbc92-144">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fbc92-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fbc92-145">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="fbc92-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="fbc92-146">Implementieren eines Statusindikators</span><span class="sxs-lookup"><span data-stu-id="fbc92-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


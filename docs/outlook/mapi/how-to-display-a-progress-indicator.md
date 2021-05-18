---
title: Anzeigen einer Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408026"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="539f0-103">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="539f0-103">Display a progress indicator</span></span>
 
<span data-ttu-id="539f0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="539f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="539f0-105">Rufen Sie zum Anzeigen eines Statusindikators [IMAPIProgress::GetFlags](imapiprogress-getflags.md) auf, um die aktuelle Flagseinstellung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="539f0-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="539f0-106">Wenn das MAPI_TOP_LEVEL festgelegt ist, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="539f0-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="539f0-107">Legen Sie eine Variable fest, die der Gesamtanzahl von Elementen entspricht, die im Vorgang zu verarbeiten sind.</span><span class="sxs-lookup"><span data-stu-id="539f0-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="539f0-108">Wenn Sie z. B. den Inhalt eines Ordners kopieren, entspricht dieser Wert der Anzahl der Unterordner im Ordner plus der Anzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="539f0-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="539f0-109">Legen Sie eine Variable auf 1000 dividiert durch die Anzahl der Elemente fest.</span><span class="sxs-lookup"><span data-stu-id="539f0-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="539f0-110">Wenn Sie den Fortschritt für Unterobjekte anzeigen, rufen Sie die [IMAPIProgress::SetLimits-Methode](imapiprogress-setlimits.md) des Progress-Objekts auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="539f0-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="539f0-111">Legen Sie  _den lpulMin-Parameter_ auf 0.</span><span class="sxs-lookup"><span data-stu-id="539f0-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="539f0-112">Legen Sie  _den lpulMax-Parameter_ auf 1000.</span><span class="sxs-lookup"><span data-stu-id="539f0-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="539f0-113">Legen Sie  _den Parameter lpulFlags_ auf MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="539f0-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="539f0-114">Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="539f0-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="539f0-115">Rufen **Sie IMAPIProgress::SetLimits auf,** und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="539f0-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="539f0-116">Legen Sie  _den lpulMin-Parameter_ auf die Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Element minus 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="539f0-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="539f0-117">Legen Sie  _den lpulMax-Parameter_ auf die Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="539f0-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="539f0-118">Legen Sie  _den Parameter lpulFlags_ auf 0.</span><span class="sxs-lookup"><span data-stu-id="539f0-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="539f0-119">Führen Sie alle Verarbeitungsschritte aus, die für dieses Objekt durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="539f0-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="539f0-120">Wenn es sich um ein Unterobjekt handelt und Sie den Fortschritt für Unterobjekte anzeigen möchten, übergeben Sie einen Zeiger an das Progress-Objekt im  _lpProgress-Parameter_ an die -Methode.</span><span class="sxs-lookup"><span data-stu-id="539f0-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="539f0-121">Rufen [Sie IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="539f0-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="539f0-122">Legen Sie  _den ulValue-Parameter_ auf die Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="539f0-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="539f0-123">Legen Sie  _den ulCount-Parameter_ auf das aktuelle Objekt.</span><span class="sxs-lookup"><span data-stu-id="539f0-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="539f0-124">Legen Sie  _den ulTotal-Parameter_ auf die Variable fest, die in Schritt 1 festgelegt ist, die Gesamtanzahl der Objekte.</span><span class="sxs-lookup"><span data-stu-id="539f0-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="539f0-125">Wenn das MAPI_TOP_LEVEL nicht festgelegt ist, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="539f0-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="539f0-126">Rufen Sie die [IMAPIProgress::GetMin-Methode](imapiprogress-getmin.md) des Progress-Objekts auf, um den Minimalwert für die Anzeige abzurufen.</span><span class="sxs-lookup"><span data-stu-id="539f0-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="539f0-127">Rufen [Sie IMAPIProgress::GetMax auf,](imapiprogress-getmax.md) um den maximalen Wert für die Anzeige abzurufen.</span><span class="sxs-lookup"><span data-stu-id="539f0-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="539f0-128">Legen Sie eine Variable fest, die der Gesamtanzahl der zu verarbeitende Objekte entspricht.</span><span class="sxs-lookup"><span data-stu-id="539f0-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="539f0-129">Legen Sie eine Variable fest, die dem Ergebnis entspricht, indem Sie den Minimalwert vom Maximalwert subtrahieren und dann durch die Gesamtanzahl der Objekte dividieren.</span><span class="sxs-lookup"><span data-stu-id="539f0-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="539f0-130">Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="539f0-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="539f0-131">Wenn Ihr Anbieter den Fortschritt für Unterobjekte zeigt, rufen Sie **IMAPIProgress::SetLimits** auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="539f0-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="539f0-132">Legen Sie  _den lpulMin-Parameter_ auf den Minimalwert plus das aktuelle Element minus 1 multipliziert mit der variablen Einstellung in Schritt 4 fest.</span><span class="sxs-lookup"><span data-stu-id="539f0-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="539f0-133">Legen Sie  _den lpulMax-Parameter_ auf den Minimalwert plus die aktuelle Einheit fest, multipliziert mit der Variablen in Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="539f0-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="539f0-134">Legen Sie  _den Parameter lpulFlags_ auf 0.</span><span class="sxs-lookup"><span data-stu-id="539f0-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="539f0-135">Führen Sie alle Verarbeitungsschritte aus, die für dieses Objekt durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="539f0-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="539f0-136">Wenn es sich bei dem Objekt um ein Unterobjekt handelt und ihr Anbieter den Fortschritt für Unterobjekte anzeigt, übergeben Sie einen Zeiger an das Progress-Objekt im  _lpProgress-Parameter_ an die -Methode.</span><span class="sxs-lookup"><span data-stu-id="539f0-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="539f0-137">Rufen [Sie IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="539f0-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="539f0-138">Legen Sie  _den ulValue-Parameter_ auf eine Variable fest, die in Schritt 2 multipliziert mit dem aktuellen Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="539f0-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="539f0-139">Legen Sie  _den ulCount-Parameter_ auf 0.</span><span class="sxs-lookup"><span data-stu-id="539f0-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="539f0-140">Legen Sie  _den ulTotal-Parameter_ auf 0.</span><span class="sxs-lookup"><span data-stu-id="539f0-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="539f0-141">Im folgenden Codebeispiel wird die Logik veranschaulicht, die erforderlich ist, um den Fortschritt auf allen Ebenen eines Vorgangs anzuzeigen, der den Inhalt eines Ordners kopiert, der fünf Unterordner enthält.</span><span class="sxs-lookup"><span data-stu-id="539f0-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a><span data-ttu-id="539f0-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="539f0-142">See also</span></span>

- [<span data-ttu-id="539f0-143">MAPI-Fortschrittsindikatoren</span><span class="sxs-lookup"><span data-stu-id="539f0-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)


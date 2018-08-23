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
ms.openlocfilehash: 62549cbeea0044ceee8aa2e704b8a9bc271b7e8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564493"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="0aa80-103">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="0aa80-103">Display a progress indicator</span></span>
 
<span data-ttu-id="0aa80-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa80-105">Rufen Sie [IMAPIProgress::GetFlags](imapiprogress-getflags.md) zum Abrufen der aktuellen Flags festlegen, um eine Statusanzeige anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0aa80-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="0aa80-106">Wenn das Flag MAPI_TOP_LEVEL festgelegt ist, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0aa80-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="0aa80-107">Weisen Sie einer Variablen zur Gesamtanzahl der Elemente, die in den Vorgang verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0aa80-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="0aa80-108">Angenommen, wenn Sie den Inhalt eines Ordners kopieren, wird dieser Wert gleich der Anzahl der Unterordner im Ordner plus die Anzahl der Nachrichten sein.</span><span class="sxs-lookup"><span data-stu-id="0aa80-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="0aa80-109">Weisen Sie einer Variablen bis 1000 geteilt durch die Anzahl der Elemente.</span><span class="sxs-lookup"><span data-stu-id="0aa80-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="0aa80-110">Wenn Sie den Fortschritt für Unterobjekte angezeigt werden, rufen Sie den Fortschritt des Objekts [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) -Methode, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="0aa80-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="0aa80-111">Den Parameter _LpulMin_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="0aa80-112">Den Parameter _LpulMax_ auf 1000 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="0aa80-113">Den Parameter _LpulFlags_ auf MAPI_TOP_LEVEL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="0aa80-114">Führen Sie für jedes Objekt verarbeitet werden die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0aa80-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="0aa80-115">Rufen Sie **IMAPIProgress::SetLimits** und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="0aa80-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0aa80-116">Legen Sie den _LpulMin_ -Parameter der Variablen, die in Schritt 2 des aktuellen Elements minus 1 multipliziert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="0aa80-117">Legen Sie den _LpulMax_ -Parameter der Variablen, die in Schritt 2 multipliziert das aktuelle Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0aa80-118">Den Parameter _LpulFlags_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="0aa80-119">Führen Sie die Verarbeitung für dieses Objekt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0aa80-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="0aa80-120">Wenn dies ein Unterobjekt ist und Fortschritt auf Unterobjekte angezeigt werden soll, übergeben Sie einen Zeiger auf das Objekt Fortschritt im _LpProgress_ -Parameter der Methode.</span><span class="sxs-lookup"><span data-stu-id="0aa80-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="0aa80-121">Rufen Sie [IMAPIProgress::Progress](imapiprogress-progress.md) und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="0aa80-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0aa80-122">Legen Sie den _UlValue_ -Parameter der Variablen, die in Schritt 2 multipliziert das aktuelle Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0aa80-123">Den Parameter _UlCount_ auf das aktuelle Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="0aa80-124">Legen Sie den _UlTotal_ -Parameter der Variablen, die in Schritt 1, die Gesamtanzahl der Objekte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="0aa80-125">Wenn das Flag MAPI_TOP_LEVEL nicht festgelegt ist, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0aa80-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="0aa80-126">Rufen Sie den Fortschritt des Objekts [IMAPIProgress::GetMin](imapiprogress-getmin.md) -Methode zum Abrufen des Mindestwert für die Anzeige.</span><span class="sxs-lookup"><span data-stu-id="0aa80-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="0aa80-127">Rufen Sie [IMAPIProgress::GetMax](imapiprogress-getmax.md) , um den Maximalwert für die Anzeige abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0aa80-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="0aa80-128">Weisen Sie einer Variablen zur Gesamtanzahl der Objekte verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa80-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="0aa80-129">Weisen Sie einer Variablen auf das Ergebnis der Subtraktion des kleinsten Werts in den Höchstwert und klicken Sie dann Division durch die Gesamtanzahl der Objekte.</span><span class="sxs-lookup"><span data-stu-id="0aa80-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="0aa80-130">Führen Sie für jedes Objekt verarbeitet werden die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0aa80-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="0aa80-131">Wenn der Anbieter für Unterobjekte Fortschritt angezeigt wird, rufen Sie **IMAPIProgress::SetLimits** , und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="0aa80-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0aa80-132">Legen Sie den _LpulMin_ -Parameter auf den kleinsten Wert sowie das aktuelle Element minus 1 multipliziert die Variable, die in Schritt 4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="0aa80-133">Legen Sie den _LpulMax_ -Parameter auf den kleinsten Wert plus die aktuelle Maßeinheit multipliziert die Variable, die in Schritt 4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="0aa80-134">Den Parameter _LpulFlags_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="0aa80-135">Führen Sie die Verarbeitung für dieses Objekt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0aa80-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="0aa80-136">Wenn das Objekt ein Unterobjekt ist und Ihrem Anbieter zeigt den Status Unterobjekte, übergeben Sie einen Zeiger auf das Objekt Fortschritt im _LpProgress_ -Parameter an die-Methode.</span><span class="sxs-lookup"><span data-stu-id="0aa80-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="0aa80-137">Rufen Sie [IMAPIProgress::Progress](imapiprogress-progress.md) und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="0aa80-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="0aa80-138">Legen Sie den _UlValue_ -Parameter auf Variable, die in Schritt 2 multipliziert das aktuelle Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="0aa80-139">Den Parameter _UlCount_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="0aa80-140">Den Parameter _UlTotal_ auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0aa80-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="0aa80-141">Das folgende Codebeispiel veranschaulicht die Logik erforderlich, um den Fortschritt auf allen Ebenen eines Vorgangs angezeigt, die den Inhalt eines Ordners kopiert, die fünf Unterordner enthält.</span><span class="sxs-lookup"><span data-stu-id="0aa80-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="0aa80-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aa80-142">See also</span></span>

- [<span data-ttu-id="0aa80-143">MAPI-Statusanzeigen</span><span class="sxs-lookup"><span data-stu-id="0aa80-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)


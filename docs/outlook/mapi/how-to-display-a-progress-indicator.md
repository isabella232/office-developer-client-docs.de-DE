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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345129"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="a914e-103">Anzeigen einer Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="a914e-103">Display a progress indicator</span></span>
 
<span data-ttu-id="a914e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a914e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a914e-105">Um eine Statusanzeige anzuzeigen, rufen Sie [IMAPIProgress::](imapiprogress-getflags.md) GetFlags auf, um die aktuelle Flags-Einstellung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a914e-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="a914e-106">Wenn das MAPI_TOP_LEVEL-Flag festgelegt ist, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a914e-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="a914e-107">Legen Sie eine Variable auf die Gesamtanzahl der Elemente fest, die im Vorgang verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a914e-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="a914e-108">Wenn Sie beispielsweise den Inhalt eines Ordners kopieren, entspricht dieser Wert der Anzahl der Unterordner im Ordner und der Anzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="a914e-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="a914e-109">Legen Sie eine Variable auf 1000 geteilt durch die Anzahl der Elemente fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="a914e-110">Wenn Sie den Fortschritt für unter Objekte anzeigen möchten, rufen Sie die [IMAPIProgress::](imapiprogress-setlimits.md) setlimits-Methode des Progress-Objekts auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="a914e-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="a914e-111">Legen Sie den Parameter _lpulMin_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="a914e-112">Legen Sie den _lpulMax_ -parameter auf 1000.</span><span class="sxs-lookup"><span data-stu-id="a914e-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="a914e-113">Legen Sie den Parameter _lpulFlags_ auf MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="a914e-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="a914e-114">Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a914e-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="a914e-115">Rufen Sie **IMAPIProgress::** setlimits auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="a914e-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="a914e-116">Legen Sie den Parameter _lpulMin_ auf die Variable fest, die in Schritt 2 mit dem aktuellen Element minus 1 multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="a914e-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="a914e-117">Legen Sie den _lpulMax_ -Parameter auf die Variable fest, die in Schritt 2 mit dem aktuellen Objekt multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="a914e-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="a914e-118">Legen Sie den Parameter _lpulFlags_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="a914e-119">Führen Sie die Verarbeitung aus, die für dieses Objekt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a914e-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="a914e-120">Wenn es sich um ein Unterobjekt handelt und Sie den Fortschritt für unter Objekte anzeigen möchten, übergeben Sie einen Zeiger auf das Progress-Objekt im _lpProgress_ -Parameter an die Methode.</span><span class="sxs-lookup"><span data-stu-id="a914e-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="a914e-121">Rufen Sie [IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="a914e-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="a914e-122">Legen Sie den _ulValue_ -Parameter auf die Variable fest, die in Schritt 2 mit dem aktuellen Objekt multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="a914e-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="a914e-123">Legen Sie den Parameter _ulCount_ auf das aktuelle Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="a914e-124">Legen Sie den Parameter _ulTotal_ auf die in Schritt 1 festgelegte Variable fest, die Gesamtanzahl der Objekte.</span><span class="sxs-lookup"><span data-stu-id="a914e-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="a914e-125">Wenn das MAPI_TOP_LEVEL-Flag nicht festgelegt ist, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a914e-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="a914e-126">Rufen Sie die [IMAPIProgress:: GetMin](imapiprogress-getmin.md) -Methode des Progress-Objekts auf, um den kleinsten Wert für die Anzeige abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a914e-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="a914e-127">Rufen Sie [IMAPIProgress:: GetMax](imapiprogress-getmax.md) auf, um den Maximalwert für die Anzeige abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a914e-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="a914e-128">Legen Sie eine Variable fest, die der Gesamtanzahl der zu verarbeitenden Objekte entspricht.</span><span class="sxs-lookup"><span data-stu-id="a914e-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="a914e-129">Legen Sie eine Variable fest, die dem Ergebnis entspricht, dass der Minimalwert vom Maximalwert subtrahiert und dann durch die Gesamtanzahl der Objekte geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="a914e-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="a914e-130">Führen Sie für jedes zu verarbeitende Objekt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a914e-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="a914e-131">Wenn Ihr Anbieter den Fortschritt für unter Objekte anzeigt, rufen Sie **IMAPIProgress::** setlimits auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="a914e-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="a914e-132">Legen Sie den Parameter _lpulMin_ auf den Minimalwert plus dem aktuellen Element minus 1 multipliziert mit der in Schritt 4 festgelegten Variable fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="a914e-133">Legen Sie den Parameter _lpulMax_ auf den Minimalwert plus der aktuellen Einheit fest, multipliziert mit der in Schritt 4 festgelegten Variable.</span><span class="sxs-lookup"><span data-stu-id="a914e-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="a914e-134">Legen Sie den Parameter _lpulFlags_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="a914e-135">Führen Sie die Verarbeitung aus, die für dieses Objekt ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a914e-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="a914e-136">Wenn das Objekt ein Unterobjekt ist und Ihr Anbieter den Fortschritt für unter Objekte anzeigt, übergeben Sie einen Zeiger auf das Progress-Objekt im _lpProgress_ -Parameter an die Methode.</span><span class="sxs-lookup"><span data-stu-id="a914e-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="a914e-137">Rufen Sie [IMAPIProgress::P rogress](imapiprogress-progress.md) auf, und übergeben Sie die folgenden Werte für die drei Parameter:</span><span class="sxs-lookup"><span data-stu-id="a914e-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="a914e-138">Legen Sie den Parameter _ulValue_ auf Variable festgelegt, die in Schritt 2 mit dem aktuellen Objekt multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="a914e-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="a914e-139">Legen Sie den Parameter _ulCount_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="a914e-140">Legen Sie den Parameter _ulTotal_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="a914e-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="a914e-141">Das folgende Codebeispiel veranschaulicht die Logik, die erforderlich ist, um den Fortschritt auf allen Ebenen eines Vorgangs anzuzeigen, die den Inhalt eines Ordners mit fünf Unterordnern kopiert.</span><span class="sxs-lookup"><span data-stu-id="a914e-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="a914e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a914e-142">See also</span></span>

- [<span data-ttu-id="a914e-143">MAPI-fortSchrittsIndikatoren</span><span class="sxs-lookup"><span data-stu-id="a914e-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)


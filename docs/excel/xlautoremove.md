---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- Xlautoremove-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790597"
---
# <a name="xlautoremove"></a><span data-ttu-id="4da26-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="4da26-104">xlAutoRemove</span></span>

 <span data-ttu-id="4da26-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4da26-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4da26-106">Wird von Microsoft Excel aufgerufen, wenn der Benutzer mit dem Add-In-Manager die XLL während einer Sitzung Excel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4da26-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="4da26-107">Diese Funktion ist nicht aufgerufen, wenn eine Excel-Sitzung, ordnungsgemäß oder nicht ordnungsgemäß, mit der Add-in installiert wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="4da26-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="4da26-108">Diese Funktion kann zum Anzeigen eines benutzerdefinierten Dialogfelds, die den Anwender darüber, dass das Add-in deaktiviert wurde, oder zum Lesen oder Schreiben in die Registrierung, zum Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4da26-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="4da26-109">Excel erfordert eine XLL zu implementieren und exportieren Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="4da26-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="4da26-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4da26-110">Parameters</span></span>

<span data-ttu-id="4da26-111">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="4da26-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4da26-112">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4da26-112">Property value/Return value</span></span>

<span data-ttu-id="4da26-113">Die Implementierung dieser Funktion muss 1 (**Int**) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4da26-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4da26-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4da26-114">Remarks</span></span>

<span data-ttu-id="4da26-115">Verwenden Sie diese Funktion, wenn Ihre XLL muss jede Aufgabe abschließen, wenn es vom Add-In-Manager entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4da26-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="4da26-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4da26-116">Example</span></span>

<span data-ttu-id="4da26-117">Finden Sie die Dateien `\SAMPLES\EXAMPLE\EXAMPLE.C` und `\SAMPLES\GENERIC\GENERIC.C` beispielsweise Implementierungen von dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="4da26-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="4da26-118">Der folgende Code ist aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="4da26-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="4da26-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4da26-119">See also</span></span>



[<span data-ttu-id="4da26-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="4da26-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="4da26-121">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4da26-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)


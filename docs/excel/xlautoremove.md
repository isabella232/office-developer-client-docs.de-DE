---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlAutoRemove-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425477"
---
# <a name="xlautoremove"></a><span data-ttu-id="f1c86-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="f1c86-104">xlAutoRemove</span></span>

 <span data-ttu-id="f1c86-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1c86-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f1c86-106">Wird von Microsoft Excel aufgerufen, wenn der Benutzer die XLL während einer Excel-Sitzung mithilfe des Add-in-Managers deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f1c86-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="f1c86-107">Diese Funktion wird nicht aufgerufen, wenn eine Excel-Sitzung mit dem installierten Add-In (ordnungsgemäß oder unerwartet) beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1c86-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="f1c86-108">Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer mitteilt, dass das Add-in deaktiviert wurde, oder beispielsweise in die Registrierung zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="f1c86-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="f1c86-109">Excel benötigt keine XLL, um diese Funktion zu implementieren und zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="f1c86-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="f1c86-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1c86-110">Parameters</span></span>

<span data-ttu-id="f1c86-111">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f1c86-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f1c86-112">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1c86-112">Property value/Return value</span></span>

<span data-ttu-id="f1c86-113">Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).</span><span class="sxs-lookup"><span data-stu-id="f1c86-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1c86-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1c86-114">Remarks</span></span>

<span data-ttu-id="f1c86-115">Verwenden Sie diese Funktion, wenn Ihre XLL eine Aufgabe ausführen muss, wenn Sie vom Add-in-Manager entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f1c86-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="f1c86-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f1c86-116">Example</span></span>

<span data-ttu-id="f1c86-117">Schauen Sie sich die Dateien `\SAMPLES\EXAMPLE\EXAMPLE.C` und `\SAMPLES\GENERIC\GENERIC.C` für Beispiel-Implementierungen dieser Funktion an.</span><span class="sxs-lookup"><span data-stu-id="f1c86-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="f1c86-118">Der folgende Code stammt aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="f1c86-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="f1c86-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1c86-119">See also</span></span>



[<span data-ttu-id="f1c86-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="f1c86-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="f1c86-121">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f1c86-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)


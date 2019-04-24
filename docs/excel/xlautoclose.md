---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- XlAutoClose-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310234"
---
# <a name="xlautoclose"></a><span data-ttu-id="97a3c-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="97a3c-104">xlAutoClose</span></span>

 <span data-ttu-id="97a3c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97a3c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="97a3c-106">Microsoft Excel wird aufgerufen, sobald die XLL deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="97a3c-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="97a3c-107">Das Add-in wird normalerweise bei Ablauf einer Excel-Sitzung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="97a3c-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="97a3c-108">Das Add-in kann vom Benutzer während einer Excel-Sitzung deaktiviert werden, und diese Funktion wird in diesem Fall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="97a3c-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="97a3c-109">Excel benötigt keine XLL zum Implementieren und Exportieren dieser Funktion, obwohl dies ratsam ist, um Ihre XLL Funktionen und Befehle nicht zu registrieren, Ressourcen freizugeben, Anpassungen rückgängig zu machen und so weiter.</span><span class="sxs-lookup"><span data-stu-id="97a3c-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="97a3c-110">Falls Funktionen und Befehle nicht explizit durch die XLL nicht registriert sind, führt Excel dies nach Aufruf der **XlAutoClose** Funktion durch.</span><span class="sxs-lookup"><span data-stu-id="97a3c-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="97a3c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a3c-111">Parameters</span></span>

<span data-ttu-id="97a3c-112">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="97a3c-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="97a3c-113">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97a3c-113">Property value/Return value</span></span>

<span data-ttu-id="97a3c-114">Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).</span><span class="sxs-lookup"><span data-stu-id="97a3c-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97a3c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97a3c-115">Remarks</span></span>

<span data-ttu-id="97a3c-116">Excel ruft die **XlAutoClose** Funktion auf, sobald die XLL deaktiviert ist, d. h. aus dem Speicher entladen.</span><span class="sxs-lookup"><span data-stu-id="97a3c-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="97a3c-117">Die XLL wird in den folgenden Fällen deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="97a3c-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="97a3c-118">Am üblichen Ende einer Excel-Sitzung falls es während dieser Sitzung aktiviert war.</span><span class="sxs-lookup"><span data-stu-id="97a3c-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="97a3c-119">Falls es während einer Excel-Sitzung explizit entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="97a3c-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="97a3c-120">Eine XLL kann auf verschiedene Arten entladen werden:</span><span class="sxs-lookup"><span data-stu-id="97a3c-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="97a3c-121">Verwenden des Add-In-Managers.</span><span class="sxs-lookup"><span data-stu-id="97a3c-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="97a3c-122">Aus einem anderen XLL, welches [XlfUnregister](xlfunregister-form-1.md) mit dem Namen der DLL als einziges Argument aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="97a3c-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="97a3c-123">Aus einer XLM-Makrovorlage, die [UNREGISTER](xlfunregister-form-1.md) mit dem Namen der DLL als einziges Argument aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="97a3c-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="97a3c-124">Diese Funktion sollte folgendermaßen vorgehen:</span><span class="sxs-lookup"><span data-stu-id="97a3c-124">This function should do the following:</span></span>
  
- <span data-ttu-id="97a3c-125">Entfernen Sie alle Menüs oder Menüelemente, die von der XLL hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="97a3c-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="97a3c-126">Führen Sie jegliche erforderliche globale Reinigung durch.</span><span class="sxs-lookup"><span data-stu-id="97a3c-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="97a3c-127">Löschen Sie alle Namen, die erstellt worden sind, insbesondere die Namen der exportierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="97a3c-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="97a3c-128">Beachten Sie, dass das Registrieren von Funktionen die Erstellung einiger Namen zur Folge hat, falls das vierte Argument **Registrieren** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="97a3c-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="97a3c-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97a3c-129">Example</span></span>

<span data-ttu-id="97a3c-130">Schauen Sie sich die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C` für Beispiel-Implementierungen dieser Funktion an.</span><span class="sxs-lookup"><span data-stu-id="97a3c-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="97a3c-131">Der folgende Code stammt aus `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="97a3c-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="97a3c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a3c-132">See also</span></span>



[<span data-ttu-id="97a3c-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="97a3c-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="97a3c-134">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="97a3c-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)


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
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790600"
---
# <a name="xlautoclose"></a><span data-ttu-id="ac08f-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="ac08f-104">xlAutoClose</span></span>

 <span data-ttu-id="ac08f-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ac08f-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ac08f-106">Microsoft Excel wird aufgerufen, sobald die XLL deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ac08f-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="ac08f-107">Das Add-in wird normalerweise bei Ablauf einer Excel-Sitzung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac08f-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="ac08f-108">Das Add-in kann vom Benutzer während einer Excel-Sitzung deaktiviert werden, und diese Funktion wird in diesem Fall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ac08f-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="ac08f-109">Excel benötigt keine XLL zum Implementieren und Exportieren dieser Funktion, obwohl dies ratsam ist, um Ihre XLL Funktionen und Befehle nicht zu registrieren, Ressourcen freizugeben, Anpassungen rückgängig zu machen und so weiter.</span><span class="sxs-lookup"><span data-stu-id="ac08f-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="ac08f-110">Falls Funktionen und Befehle nicht explizit durch die XLL nicht registriert sind, führt Excel dies nach Aufruf der **XlAutoClose** Funktion durch.</span><span class="sxs-lookup"><span data-stu-id="ac08f-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="ac08f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac08f-111">Parameters</span></span>

<span data-ttu-id="ac08f-112">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ac08f-112">This function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ac08f-113">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac08f-113">Property Value/Return Value</span></span>

<span data-ttu-id="ac08f-114">Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).</span><span class="sxs-lookup"><span data-stu-id="ac08f-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac08f-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac08f-115">Remarks</span></span>

<span data-ttu-id="ac08f-116">Excel ruft die **XlAutoClose** Funktion auf, sobald die XLL deaktiviert ist, d. h. aus dem Speicher entladen.</span><span class="sxs-lookup"><span data-stu-id="ac08f-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="ac08f-117">Die XLL wird in den folgenden Fällen deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="ac08f-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="ac08f-118">Am üblichen Ende einer Excel-Sitzung falls es während dieser Sitzung aktiviert war.</span><span class="sxs-lookup"><span data-stu-id="ac08f-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="ac08f-119">Falls es während einer Excel-Sitzung explizit entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="ac08f-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="ac08f-120">Eine XLL kann auf verschiedene Arten entladen werden:</span><span class="sxs-lookup"><span data-stu-id="ac08f-120">An XLOPER/XLOPER12 can be created in several ways:</span></span>
    
- <span data-ttu-id="ac08f-121">Verwenden des Add-In-Managers.</span><span class="sxs-lookup"><span data-stu-id="ac08f-121">Using the Add-In Manager</span></span>
    
- <span data-ttu-id="ac08f-122">Aus einem anderen XLL, welches [XlfUnregister](xlfunregister-form-1.md) mit dem Namen der DLL als einziges Argument aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="ac08f-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="ac08f-123">Aus einer XLM-Makrovorlage, die [UNREGISTER](xlfunregister-form-1.md) mit dem Namen der DLL als einziges Argument aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="ac08f-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="ac08f-124">Diese Funktion sollte folgendermaßen vorgehen:</span><span class="sxs-lookup"><span data-stu-id="ac08f-124">This function should do the following:</span></span>
  
- <span data-ttu-id="ac08f-125">Entfernen Sie alle Menüs oder Menüelemente, die von der XLL hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="ac08f-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="ac08f-126">Führen Sie jegliche erforderliche globale Reinigung durch.</span><span class="sxs-lookup"><span data-stu-id="ac08f-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="ac08f-127">Löschen Sie alle Namen, die erstellt worden sind, insbesondere die Namen der exportierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ac08f-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="ac08f-128">Beachten Sie, dass das Registrieren von Funktionen die Erstellung einiger Namen zur Folge hat, falls das vierte Argument **Registrieren** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ac08f-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="ac08f-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ac08f-129">Example</span></span>

<span data-ttu-id="ac08f-130">Schauen Sie sich die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C` für Beispiel-Implementierungen dieser Funktion an.</span><span class="sxs-lookup"><span data-stu-id="ac08f-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="ac08f-131">Der folgende Code stammt aus `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="ac08f-131">The following is the output from the code example.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ac08f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac08f-132">See also</span></span>



[<span data-ttu-id="ac08f-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="ac08f-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="ac08f-134">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="ac08f-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)


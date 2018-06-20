---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- XlAutoClose-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790600"
---
# <a name="xlautoclose"></a><span data-ttu-id="377ce-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="377ce-104">xlAutoClose</span></span>

 <span data-ttu-id="377ce-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="377ce-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="377ce-106">Wird von Microsoft Excel aufgerufen, wenn die XLL deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="377ce-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="377ce-107">Das Add-In wird normalerweise am Ende eine Excel-Sitzung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="377ce-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="377ce-108">Das Add-in deaktiviert werden vom Benutzer während einer Excel-Sitzung, und diese Funktion wird in diesem Fall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="377ce-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="377ce-109">Excel erfordert eine XLL zu implementieren und exportieren Sie diese Funktion nicht auf, obwohl es ratsam ist, damit Ihre XLL Aufheben der Registrierung Funktionen und Befehle, Ressourcen freizugeben, rückgängig Anpassungen und usw..</span><span class="sxs-lookup"><span data-stu-id="377ce-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="377ce-110">Wenn die Funktionen und Befehle nicht explizit durch die XLL nicht registriert sind, wird Excel nach dem Aufrufen der **XlAutoClose** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="377ce-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="377ce-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="377ce-111">Parameters</span></span>

<span data-ttu-id="377ce-112">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="377ce-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="377ce-113">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="377ce-113">Property value/Return value</span></span>

<span data-ttu-id="377ce-114">Die Implementierung dieser Funktion muss 1 (**Int**) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="377ce-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="377ce-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="377ce-115">Remarks</span></span>

<span data-ttu-id="377ce-116">Excel Ruft die **XlAutoClose** -Funktion, wenn die XLL entladen aus dem Speicher deaktiviert wird, d. h..</span><span class="sxs-lookup"><span data-stu-id="377ce-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="377ce-117">Die XLL ist in den folgenden Situationen deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="377ce-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="377ce-118">Am normalen Ende einer Excel-Sitzung bei active während der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="377ce-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="377ce-119">Wenn Sie während einer Sitzung Excel explizit entladen.</span><span class="sxs-lookup"><span data-stu-id="377ce-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="377ce-120">Eine XLL kann auf verschiedene Weise entladen werden:</span><span class="sxs-lookup"><span data-stu-id="377ce-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="377ce-121">Verwenden Sie den Add-In-Manager.</span><span class="sxs-lookup"><span data-stu-id="377ce-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="377ce-122">Aus einer anderen XLL aufruft, [XlfUnregister](xlfunregister-form-1.md) mit dem Namen dieser DLL als einziges Argument.</span><span class="sxs-lookup"><span data-stu-id="377ce-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="377ce-123">Aus einer XLM-Makrovorlage aufruft, die mit dem Namen dieser DLL [UNREGISTER](xlfunregister-form-1.md) als einziges Argument.</span><span class="sxs-lookup"><span data-stu-id="377ce-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="377ce-124">Diese Funktion sollte Folgendes:</span><span class="sxs-lookup"><span data-stu-id="377ce-124">This function should do the following:</span></span>
  
- <span data-ttu-id="377ce-125">Entfernen Sie keine Menüs oder Menüelemente, die von der XLL hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="377ce-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="377ce-126">Führen Sie alle erforderliche globale Bereinigung aus.</span><span class="sxs-lookup"><span data-stu-id="377ce-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="377ce-127">Löschen Sie die Namen, die, insbesondere die Namen der exportierten Funktionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="377ce-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="377ce-128">Denken Sie daran, dass Funktionen registrieren einige Namen erstellt werden soll, führen kann, wenn das vierte Argument **Registrieren** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="377ce-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="377ce-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="377ce-129">Example</span></span>

<span data-ttu-id="377ce-130">Finden Sie die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C` beispielsweise Implementierungen von dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="377ce-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="377ce-131">Der folgende Code ist aus `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="377ce-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="377ce-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="377ce-132">See also</span></span>



[<span data-ttu-id="377ce-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="377ce-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="377ce-134">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="377ce-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)


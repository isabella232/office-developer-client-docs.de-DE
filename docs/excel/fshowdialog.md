---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433591"
---
# <a name="fshowdialog"></a><span data-ttu-id="bb6f0-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="bb6f0-104">fShowDialog</span></span>

 <span data-ttu-id="bb6f0-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bb6f0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bb6f0-106">Beispiel für benutzerdefinierten Befehl, der ein Beispiel für systemeigene Windows lädt und anzeigt.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="bb6f0-107">Wenn GENERIC.xll geladen wird, wird ein benutzerdefiniertes Menü, Generic, erstellt, über das auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="bb6f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb6f0-108">Parameters</span></span>

<span data-ttu-id="bb6f0-109">Die Funktion nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bb6f0-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb6f0-110">Property value/Return value</span></span>

<span data-ttu-id="bb6f0-111">Die Funktion gibt ganzzahlige Null zurück, um einen erfolgreichen Abschluss anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb6f0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb6f0-112">Remarks</span></span>

<span data-ttu-id="bb6f0-113">Die Schritte zum Anzeigen des systemeigenen Windows sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bb6f0-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="bb6f0-114">Rufen Sie Microsoft Excel Haupthandle Windows **GetHwnd ab.**</span><span class="sxs-lookup"><span data-stu-id="bb6f0-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="bb6f0-115">Hook the Excel main window using **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="bb6f0-116">Anzeigen des Dialogfelds mithilfe von **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="bb6f0-117">Enthook the Excel main window using **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="bb6f0-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bb6f0-118">Example</span></span>

<span data-ttu-id="bb6f0-119">Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="bb6f0-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb6f0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6f0-120">See also</span></span>



[<span data-ttu-id="bb6f0-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="bb6f0-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)


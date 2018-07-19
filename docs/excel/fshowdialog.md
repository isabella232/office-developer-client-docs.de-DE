---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fShowDialog-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790512"
---
# <a name="fshowdialog"></a><span data-ttu-id="fe7b1-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="fe7b1-104">fShowDialog</span></span>

 <span data-ttu-id="fe7b1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe7b1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fe7b1-106">Beispiel benutzerdefinierter Befehl, der geladen und ein Beispiel systemeigenen Windows-Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="fe7b1-107">Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="fe7b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe7b1-108">Parameters</span></span>

<span data-ttu-id="fe7b1-109">Die Funktion akzeptiert keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fe7b1-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe7b1-110">Property value/Return value</span></span>

<span data-ttu-id="fe7b1-111">Die Funktion return ganze Zahl 0 (null) an, dass erfolgreiche Abschluss</span><span class="sxs-lookup"><span data-stu-id="fe7b1-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe7b1-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe7b1-112">Remarks</span></span>

<span data-ttu-id="fe7b1-113">Die Schritte zum Anzeigen des systemeigenen Windows-Dialogfeld sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fe7b1-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="fe7b1-114">Abrufen von **GetHwnd**Hauptfenster Microsoft Excel-Windows-Handles.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="fe7b1-115">Das Excel-Hauptfenster mit **HookExcelWindow**zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="fe7b1-116">Zeigt das Dialogfeld **DialogBox**verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="fe7b1-117">Aufzuheben Sie das Excel-Hauptfenster mit **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="fe7b1-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe7b1-118">Example</span></span>

<span data-ttu-id="fe7b1-119">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="fe7b1-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe7b1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe7b1-120">See also</span></span>



[<span data-ttu-id="fe7b1-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="fe7b1-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)


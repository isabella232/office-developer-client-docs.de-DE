---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fShowDialog-Funktion [Excel 2007]
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
# <a name="fshowdialog"></a><span data-ttu-id="6d069-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="6d069-104">fShowDialog</span></span>

 <span data-ttu-id="6d069-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6d069-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6d069-106">Beispiel für einen benutzerdefinierten Befehl, mit dem ein Beispiel systemeigenes Windows-Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6d069-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="6d069-107">Wenn GENERIC. XLL geladen wird, wird ein benutzerdefiniertes Menü generisch erstellt, über das auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="6d069-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="6d069-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d069-108">Parameters</span></span>

<span data-ttu-id="6d069-109">Die Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d069-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6d069-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d069-110">Property value/Return value</span></span>

<span data-ttu-id="6d069-111">Die Funktion gibt Integer Zero zurück, um den erfolgreichen Abschluss anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6d069-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d069-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d069-112">Remarks</span></span>

<span data-ttu-id="6d069-113">Die Schritte zum Anzeigen des systemeigenen Windows-Dialogfelds lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6d069-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="6d069-114">Abrufen des Microsoft Excel-Haupt Windows- \*\*\*\* Handles mithilfe von GetHwnd.</span><span class="sxs-lookup"><span data-stu-id="6d069-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="6d069-115">Verknüpfen Sie das Excel-Hauptfenster mit **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="6d069-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="6d069-116">Zeigen Sie das Dialogfeld mit der **Dialogbox**an.</span><span class="sxs-lookup"><span data-stu-id="6d069-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="6d069-117">Enthaken des Excel-Hauptfensters mithilfe von **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="6d069-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="6d069-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d069-118">Example</span></span>

<span data-ttu-id="6d069-119">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="6d069-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6d069-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d069-120">See also</span></span>



[<span data-ttu-id="6d069-121">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="6d069-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)


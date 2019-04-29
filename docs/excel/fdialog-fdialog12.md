---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog-Funktion [Excel 2007], fDialog12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431526"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="bd3d3-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="bd3d3-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="bd3d3-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bd3d3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bd3d3-106">Beispiel für einen benutzerdefinierten Befehl, mit dem das Erstellen eines Microsoft Excel-UDD (benutzerdefiniertes Dialogfeld) in einer DLL mithilfe der Dialogfeldfunktionen in der C-API veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="bd3d3-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="bd3d3-107">Wenn GENERIC. XLL geladen wird, wird ein benutzerdefiniertes Menü generisch erstellt, über das auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="bd3d3-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="bd3d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd3d3-108">Parameters</span></span>

<span data-ttu-id="bd3d3-109">Die Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd3d3-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bd3d3-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd3d3-110">Property value/Return value</span></span>

<span data-ttu-id="bd3d3-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="bd3d3-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="bd3d3-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bd3d3-112">Example</span></span>

<span data-ttu-id="bd3d3-113">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="bd3d3-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd3d3-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd3d3-114">See also</span></span>



[<span data-ttu-id="bd3d3-115">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="bd3d3-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)


---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435957"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="0ce02-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="0ce02-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="0ce02-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0ce02-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0ce02-106">Frameworkbibliotheksfunktion, die eine temporäre **XLOPER** /  **XLOPER12 vom** Typ **xltypeMissing erstellt.**</span><span class="sxs-lookup"><span data-stu-id="0ce02-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="0ce02-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce02-107">Parameters</span></span>

<span data-ttu-id="0ce02-108">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0ce02-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0ce02-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ce02-109">Return value</span></span>

<span data-ttu-id="0ce02-110">Gibt einen Zeiger auf **xltypeMissing** **XLOPER** /  **XLOPER12 zurück.**</span><span class="sxs-lookup"><span data-stu-id="0ce02-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="0ce02-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ce02-111">Example</span></span>

<span data-ttu-id="0ce02-112">In diesem Beispiel wird **TempMissing12** verwendet, um **xlcWorkspace** drei fehlende Argumente zu geben, gefolgt von **einem Boolean** **FALSE,** um die Anzeige von Arbeitsblatt-Bildlaufleisten zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="0ce02-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="0ce02-113">Die ersten drei Argumente entsprechen anderen Arbeitsbereichseinstellungen, die nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="0ce02-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="0ce02-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ce02-114">See also</span></span>



[<span data-ttu-id="0ce02-115">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="0ce02-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


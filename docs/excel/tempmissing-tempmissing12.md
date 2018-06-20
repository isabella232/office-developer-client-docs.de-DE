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
- Tempmissing-Funktion [excel 2007], TempMissing12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790576"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="52543-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="52543-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="52543-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52543-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52543-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** des Typs **XltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="52543-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="52543-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="52543-107">Parameters</span></span>

<span data-ttu-id="52543-108">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="52543-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="52543-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="52543-109">Return value</span></span>

<span data-ttu-id="52543-110">Gibt einen Zeiger auf eine **XLOPER** **XltypeMissing** / **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="52543-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="52543-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52543-111">Example</span></span>

<span data-ttu-id="52543-112">In diesem Beispiel wird **TempMissing12** drei Fehlende Argumente für **XlcWorkspace** gefolgt von einem **booleschen** **FALSE** unterdrückt die Anzeige der Bildlaufleisten Arbeitsblatt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52543-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="52543-113">Die ersten drei Argumente entsprechen andere Workspace-Einstellungen nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="52543-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="52543-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52543-114">See also</span></span>



[<span data-ttu-id="52543-115">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="52543-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


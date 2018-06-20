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
- Fdialog-Funktion [excel 2007], fDialog12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790498"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="ca92b-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="ca92b-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="ca92b-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ca92b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ca92b-106">Beispiel benutzerdefinierter Befehl, der veranschaulicht, wie Sie eine Microsoft Excel-UDD (im Dialogfeld benutzerdefinierte) innerhalb einer DLL zu erstellen, indem Sie das Dialogfeld Feld-Funktionen in der C-API.</span><span class="sxs-lookup"><span data-stu-id="ca92b-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="ca92b-107">Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="ca92b-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="ca92b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca92b-108">Parameters</span></span>

<span data-ttu-id="ca92b-109">Die Funktion akzeptiert keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca92b-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ca92b-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca92b-110">Property value/Return value</span></span>

<span data-ttu-id="ca92b-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="ca92b-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="ca92b-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ca92b-112">Example</span></span>

<span data-ttu-id="ca92b-113">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="ca92b-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca92b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca92b-114">See also</span></span>



[<span data-ttu-id="ca92b-115">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="ca92b-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)


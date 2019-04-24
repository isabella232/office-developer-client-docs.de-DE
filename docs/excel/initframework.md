---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310682"
---
# <a name="initframework"></a><span data-ttu-id="2feb2-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="2feb2-104">InitFramework</span></span>

 <span data-ttu-id="2feb2-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2feb2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2feb2-106">Framework Library-Funktion, die die Framework-Bibliothek initialisiert, die lediglich die temporären **XLOPER**/ -**XLOPER12** -Speicherdaten Strukturen initialisiert, die bereits zugewiesene Speicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="2feb2-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="2feb2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2feb2-107">Parameters</span></span>

<span data-ttu-id="2feb2-108">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2feb2-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="2feb2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2feb2-109">Return value</span></span>

<span data-ttu-id="2feb2-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2feb2-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="2feb2-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2feb2-111">Example</span></span>

<span data-ttu-id="2feb2-112">In diesem Beispiel wird die **InitFramework** -Funktion verwendet, um den gesamten temporären Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2feb2-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2feb2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2feb2-113">See also</span></span>



[<span data-ttu-id="2feb2-114">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="2feb2-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


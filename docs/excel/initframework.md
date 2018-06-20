---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- Initframework-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790502"
---
# <a name="initframework"></a><span data-ttu-id="efb93-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="efb93-104">InitFramework</span></span>

 <span data-ttu-id="efb93-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="efb93-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="efb93-106">Framework-Bibliothek-Funktion, die der Framework-Klassenbibliothek initialisiert die einfach die temporäre **XLOPER**initialisiert/ **XLOPER12** Arbeitsspeicher Datenstrukturen, Freigeben von Speicher, der bereits zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="efb93-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="efb93-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="efb93-107">Parameters</span></span>

<span data-ttu-id="efb93-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="efb93-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="efb93-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="efb93-109">Return value</span></span>

<span data-ttu-id="efb93-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="efb93-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="efb93-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="efb93-111">Example</span></span>

<span data-ttu-id="efb93-112">In diesem Beispiel wird die **InitFramework** -Funktion verwendet, alle temporären Speicherplatz freizugeben.</span><span class="sxs-lookup"><span data-stu-id="efb93-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="efb93-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efb93-113">See also</span></span>



[<span data-ttu-id="efb93-114">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="efb93-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


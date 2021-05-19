---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420753"
---
# <a name="initframework"></a><span data-ttu-id="b9660-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="b9660-104">InitFramework</span></span>

 <span data-ttu-id="b9660-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b9660-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b9660-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER** /  **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span><span class="sxs-lookup"><span data-stu-id="b9660-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="b9660-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9660-107">Parameters</span></span>

<span data-ttu-id="b9660-108">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b9660-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b9660-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9660-109">Return value</span></span>

<span data-ttu-id="b9660-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b9660-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="b9660-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b9660-111">Example</span></span>

<span data-ttu-id="b9660-112">In diesem Beispiel wird die **InitFramework-Funktion** verwendet, um den temporären Arbeitsspeicher frei zu machen.</span><span class="sxs-lookup"><span data-stu-id="b9660-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="b9660-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9660-113">See also</span></span>



[<span data-ttu-id="b9660-114">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="b9660-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- Debugprintf-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790392"
---
# <a name="debugprintf"></a><span data-ttu-id="a5492-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="a5492-104">debugPrintf</span></span>

<span data-ttu-id="a5492-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5492-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a5492-106">Framework Bibliothek-Funktion, die eine Null terminierte Byte-Zeichenfolge in der aktiven Debugger über die Windows SDK-Funktion **OutputDebugStringA**schreibt.</span><span class="sxs-lookup"><span data-stu-id="a5492-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="a5492-107">Wenn die Anwendung keinen Debugger ist, zeigt der Systemdebugger die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5492-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="a5492-108">Wenn die Anwendung verfügt über keine Debugger und der Systemdebugger nicht aktiv ist, hat **DebugPrintf** keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="a5492-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="a5492-109">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a5492-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="a5492-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5492-110">Parameters</span></span>

 <span data-ttu-id="a5492-111">_LpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="a5492-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="a5492-112">Die Formatzeichenfolge, die folgende Syntax und Regeln für, die mit der **Sprintf** -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5492-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="a5492-113">_Argumente_</span><span class="sxs-lookup"><span data-stu-id="a5492-113">_arguments_</span></span>
  
<span data-ttu-id="a5492-114">NULL oder mehr Argumente, die der Formatzeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a5492-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="a5492-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a5492-115">Example</span></span>

<span data-ttu-id="a5492-116">Diese Funktion gibt eine Zeichenfolge, um anzuzeigen, dass die Steuerung übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a5492-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="a5492-117">_DEBUG-Flag muss vor dem Kompilieren definiert werden, da andernfalls dieser Funktion hat keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="a5492-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="a5492-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5492-118">See also</span></span>



[<span data-ttu-id="a5492-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="a5492-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


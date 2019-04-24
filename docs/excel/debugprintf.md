---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311004"
---
# <a name="debugprintf"></a><span data-ttu-id="2c581-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="2c581-104">debugPrintf</span></span>

<span data-ttu-id="2c581-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2c581-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2c581-106">Framework-Bibliotheksfunktion, die eine mit NULL endende Byte-Zeichenfolge in den aktiven Debugger über die Windows SDK-Funktion **OutputDebugStringA**schreibt.</span><span class="sxs-lookup"><span data-stu-id="2c581-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="2c581-107">Wenn die Anwendung keinen Debugger hat, zeigt der Systemdebugger die Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="2c581-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="2c581-108">Wenn die Anwendung keinen Debugger hat und der Systemdebugger nicht aktiv ist, wird von **debugPrintf** keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c581-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="2c581-109">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2c581-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="2c581-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c581-110">Parameters</span></span>

 <span data-ttu-id="2c581-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="2c581-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="2c581-112">Die Formatzeichenfolge, die die Syntax und Regeln für die mit der **sprintf** -Funktion verwendete folgt.</span><span class="sxs-lookup"><span data-stu-id="2c581-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="2c581-113">_Argumente_</span><span class="sxs-lookup"><span data-stu-id="2c581-113">_arguments_</span></span>
  
<span data-ttu-id="2c581-114">NULL oder mehr Argumente, die mit der Formatzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2c581-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="2c581-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c581-115">Example</span></span>

<span data-ttu-id="2c581-116">Diese Funktion druckt eine Zeichenfolge, um anzuzeigen, dass das Steuerelement an Sie übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2c581-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="2c581-117">Das _DEBUG-Flag muss vor dem Kompilieren definiert werden, sonst hat diese Funktion nichts.</span><span class="sxs-lookup"><span data-stu-id="2c581-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="2c581-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c581-118">See also</span></span>



[<span data-ttu-id="2c581-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="2c581-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


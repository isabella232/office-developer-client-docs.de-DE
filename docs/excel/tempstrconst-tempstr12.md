---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- tempstr12-Funktion [excel 2007],TempStrConst-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407151"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="0d391-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="0d391-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="0d391-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0d391-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0d391-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span><span class="sxs-lookup"><span data-stu-id="0d391-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="0d391-107">Die Funktion weist einen neuen Speicherpuffer zu und kopiert die übergebene Zeichenfolge in diesen.</span><span class="sxs-lookup"><span data-stu-id="0d391-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="0d391-108">Die Eingabezeichenfolge wird nicht geändert und daher als const **deklariert.**</span><span class="sxs-lookup"><span data-stu-id="0d391-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="0d391-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d391-109">Parameters</span></span>

 <span data-ttu-id="0d391-110">_str_</span><span class="sxs-lookup"><span data-stu-id="0d391-110">_str_</span></span>
  
<span data-ttu-id="0d391-111">Ein Zeiger auf die mit Null beendete Quellzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0d391-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="0d391-112">Bei **XLOPER** s abgeschnitten TempStrConst Zeichenfolgen, die länger als 255 Byte sind.</span><span class="sxs-lookup"><span data-stu-id="0d391-112">In the case of **XLOPER** s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="0d391-113">Bei **XLOPER12** s werden Zeichenfolgen, die länger als 32.767 Unicode-Zeichen sind, von TempStr12Const abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="0d391-113">In the case of **XLOPER12** s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0d391-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d391-114">Return value</span></span>

<span data-ttu-id="0d391-115">Gibt eine **xltypeStr-Zeichenfolge** zurück, die eine Kopie des übergebenen Zeichenfolgenpuffers enthält.</span><span class="sxs-lookup"><span data-stu-id="0d391-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0d391-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d391-116">Remarks</span></span>

<span data-ttu-id="0d391-117">Beachten Sie, dass sich die XLOPER-Zeichenfolgenframework-Funktion **TempStr** anders verhält und versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben. </span><span class="sxs-lookup"><span data-stu-id="0d391-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="0d391-118">Dies ist nicht immer sicher: Microsoft Excel kann abstürzen, wenn eine schreibgeschützte Zeichenfolge übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d391-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="0d391-119">Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun veraltet, da **tempStrConst** und **TempStr12 funktionieren.**</span><span class="sxs-lookup"><span data-stu-id="0d391-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="0d391-120">Daher wird das erste Zeichen der Eingabezeichenfolge als Anfang der Zeichenfolge behandelt, d. h. nicht als Längenzeichen oder als Leerzeichen für ein Längenzeichen.</span><span class="sxs-lookup"><span data-stu-id="0d391-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="0d391-121">Sie sollten keine Zeichenfolgen übergeben, deren Länge am Anfang codiert ist, da die Folgen unvorhersehbar sein können.</span><span class="sxs-lookup"><span data-stu-id="0d391-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0d391-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d391-122">Example</span></span>

<span data-ttu-id="0d391-123">In diesem Beispiel wird die **TempStr12-Funktion** verwendet, um eine Zeichenfolge für ein Meldungsfeld zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d391-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="0d391-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d391-124">See also</span></span>



[<span data-ttu-id="0d391-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="0d391-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


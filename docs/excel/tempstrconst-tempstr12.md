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
- tempstr12-Funktion [excel 2007], TempStrConst-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790581"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="528ba-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="528ba-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="528ba-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="528ba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="528ba-106">Framework-Bibliothek-Funktion, die eine temporäre **XLOPER/XLOPER12** erstellt eine **XltypeStr** Zeichenfolge enthält, übernimmt eine mit Null endende Quellzeichenfolge als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="528ba-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="528ba-107">Die Funktion weist einen neuen Speicherpuffer für und kopiert die übergebene Zeichenfolge hinein.</span><span class="sxs-lookup"><span data-stu-id="528ba-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="528ba-108">Die eingegebene Zeichenfolge wird nicht geändert und wird daher als **Konstante**deklariert.</span><span class="sxs-lookup"><span data-stu-id="528ba-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="528ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="528ba-109">Parameters</span></span>

 <span data-ttu-id="528ba-110">_Str_</span><span class="sxs-lookup"><span data-stu-id="528ba-110">_str_</span></span>
  
<span data-ttu-id="528ba-111">Ein Zeiger auf die mit Null endende Quellzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="528ba-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="528ba-112">Im Fall von **XLOPER**s schneidet TempStrConst Zeichenfolgen, die länger als 255 Byte sind.</span><span class="sxs-lookup"><span data-stu-id="528ba-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="528ba-113">Im Fall von **XLOPER12**s schneidet TempStr12Const Zeichenfolgen, die länger als 32.767 Unicode-Zeichen sind.</span><span class="sxs-lookup"><span data-stu-id="528ba-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="528ba-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="528ba-114">Return value</span></span>

<span data-ttu-id="528ba-115">Gibt eine **XltypeStr** -Zeichenfolge, die eine Kopie des Puffers übergebene Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="528ba-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="528ba-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="528ba-116">Remarks</span></span>

<span data-ttu-id="528ba-117">Beachten Sie, dass die Zeichenfolge **XLOPER** Framework-Funktion, **TempStr**, verhält sich anders und versucht, das erste Zeichen der angegebenen Zeichenfolge mit den nachfolgenden Zeichenfolgenlänge zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="528ba-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="528ba-118">Dies ist es nicht immer eine sichere: Microsoft Excel schlagen fehl, wenn eine nur-Lese-Zeichenfolge übergeben.</span><span class="sxs-lookup"><span data-stu-id="528ba-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="528ba-119">Auf diese Weise über das Erstellen der temporärer Zeichenfolgen ist durch die Möglichkeit, in denen **TempStrConst** und **TempStr12** jetzt veraltet.</span><span class="sxs-lookup"><span data-stu-id="528ba-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="528ba-120">Aus diesem Grund wird das erste Zeichen der Eingabe Zeichenfolge als den Anfang der Zeichenfolge, d. h., nicht als ein Zeichen Länge oder als Leerzeichen für ein Zeichen Länge behandelt.</span><span class="sxs-lookup"><span data-stu-id="528ba-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="528ba-121">Sie sollten keine Zeichenfolgen übergeben, die ein zu Beginn, codierte Länge Zeichen aufweisen wie die Folgen unvorhersehbar konnte.</span><span class="sxs-lookup"><span data-stu-id="528ba-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="528ba-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="528ba-122">Example</span></span>

<span data-ttu-id="528ba-123">In diesem Beispiel wird die **TempStr12** -Funktion zum Erstellen einer Zeichenfolge für ein Meldungsfeld verwendet.</span><span class="sxs-lookup"><span data-stu-id="528ba-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="528ba-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="528ba-124">See also</span></span>



[<span data-ttu-id="528ba-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="528ba-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


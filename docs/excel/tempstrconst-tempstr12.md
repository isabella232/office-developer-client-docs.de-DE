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
- tempstr12-Funktion [Excel 2007], TempStrConst-Funktion [Excel 2007]
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
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="18f36-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="18f36-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="18f36-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="18f36-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="18f36-106">Framework-Bibliotheksfunktion, die eine temporäre **XLOPER/XLOPER12** erstellt, die eine **xltypeStr** -Zeichenfolge enthält, wobei eine mit NULL endende Quelle als Eingabe eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="18f36-106">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input.</span></span> <span data-ttu-id="18f36-107">Die Funktion weist einen neuen Speicherpuffer zu und kopiert die übergebene Zeichenfolge hinein.</span><span class="sxs-lookup"><span data-stu-id="18f36-107">The function allocates a new memory buffer and copies the passed-in string into it.</span></span> <span data-ttu-id="18f36-108">Die Eingabezeichenfolge wird nicht geändert und wird daher als **const**deklariert.</span><span class="sxs-lookup"><span data-stu-id="18f36-108">The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="18f36-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="18f36-109">Parameters</span></span>

 <span data-ttu-id="18f36-110">_str_</span><span class="sxs-lookup"><span data-stu-id="18f36-110">_str_</span></span>
  
<span data-ttu-id="18f36-111">Ein Zeiger auf die NULL-terminierte Quellzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="18f36-111">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="18f36-112">Im Fall von **XLOPER**s schneidet TempStrConst Zeichenfolgen ab, die länger als 255 Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="18f36-112">In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes.</span></span> <span data-ttu-id="18f36-113">Im Fall von **XLOPER12**s schneidet TempStr12Const Zeichenfolgen ab, die länger als 32.767 Unicode-Zeichen sind.</span><span class="sxs-lookup"><span data-stu-id="18f36-113">In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="18f36-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18f36-114">Return value</span></span>

<span data-ttu-id="18f36-115">Gibt eine **xltypeStr** -Zeichenfolge mit einer Kopie des übergebenen Zeichenfolgenpuffers zurück.</span><span class="sxs-lookup"><span data-stu-id="18f36-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="18f36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18f36-116">Remarks</span></span>

<span data-ttu-id="18f36-117">Beachten Sie, dass die **XLOPER** -Zeichenfolgen Framework-Funktion, **TempStr**, sich anders verhält und versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="18f36-117">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="18f36-118">Dies ist nicht immer sicher: Microsoft Excel stürzt möglicherweise ab, wenn eine schreibgeschützte Zeichenfolge übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="18f36-118">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> <span data-ttu-id="18f36-119">Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun zugunsten der Art und Weise veraltet, in der sowohl **TempStrConst** als auch **TempStr12** funktionieren.</span><span class="sxs-lookup"><span data-stu-id="18f36-119">This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work.</span></span> <span data-ttu-id="18f36-120">Daher wird das erste Zeichen der Eingabezeichenfolge als Anfang der Zeichenfolge behandelt, also nicht als Längenzeichen oder als Leerzeichen für ein Längezeichen.</span><span class="sxs-lookup"><span data-stu-id="18f36-120">Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character.</span></span> <span data-ttu-id="18f36-121">Sie sollten keine Zeichenfolgen mit einem Zeichen vom Typs length, die am Anfang codiert sind, als Folge der Konsequenzen nicht vorhersagen.</span><span class="sxs-lookup"><span data-stu-id="18f36-121">You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="18f36-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="18f36-122">Example</span></span>

<span data-ttu-id="18f36-123">In diesem Beispiel wird die **TempStr12** -Funktion verwendet, um eine Zeichenfolge für ein Meldungsfeld zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="18f36-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="18f36-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18f36-124">See also</span></span>



[<span data-ttu-id="18f36-125">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="18f36-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


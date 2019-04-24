---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- TempStr-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310318"
---
# <a name="tempstr"></a><span data-ttu-id="e0c93-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="e0c93-104">TempStr</span></span>

 <span data-ttu-id="e0c93-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0c93-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e0c93-106">VerAltete Framework-Bibliotheksfunktion, die eine temporäre **XLOPER** mit einer **xltypeStr** -Byte Zeichenfolge erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0c93-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="e0c93-107">Als Eingabe wird eine nullterminierte Quellzeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0c93-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="e0c93-108">Es wird versucht, das erste Zeichen der angegebenen Zeichenfolge mit der Länge der nachfolgenden Zeichenfolge zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="e0c93-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="e0c93-109">Dies ist nicht immer sicher: Microsoft Excel stürzt möglicherweise ab, wenn eine schreibgeschützte Zeichenfolge übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e0c93-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="e0c93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c93-110">Parameters</span></span>

 <span data-ttu-id="e0c93-111">_str_</span><span class="sxs-lookup"><span data-stu-id="e0c93-111">_str_</span></span>
  
<span data-ttu-id="e0c93-112">Ein Zeiger auf die NULL-terminierte Quellzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e0c93-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="e0c93-113">**TempStr** schneidet Zeichenfolgen ab, die länger als 255 Bytes sind.</span><span class="sxs-lookup"><span data-stu-id="e0c93-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="e0c93-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0c93-114">Return value</span></span>

<span data-ttu-id="e0c93-115">Gibt eine **xltypeStr** -Zeichenfolge zurück, die einen Zeiger auf den übergebenen Zeichenfolgenpuffer enthält.</span><span class="sxs-lookup"><span data-stu-id="e0c93-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e0c93-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0c93-116">Remarks</span></span>

<span data-ttu-id="e0c93-117">Diese Methode zum Erstellen temporärer Zeichenfolgen ist nun zugunsten der Art und Weise veraltet, in der sowohl TempStrConst als auch [TempStr12](tempstrconst-tempstr12.md) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e0c93-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="e0c93-118">Diese Funktionen weisen einen neuen Speicherpuffer zu und kopieren die übergebene Zeichenfolge hinein.</span><span class="sxs-lookup"><span data-stu-id="e0c93-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="e0c93-119">Die Eingabezeichenfolgen für **TempStrConst** und **TempStr12** werden nicht geändert und werden daher als **const**deklariert.</span><span class="sxs-lookup"><span data-stu-id="e0c93-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="e0c93-120">Im Gegensatz dazu wird die Eingabezeichenfolge zu **TempStr** geändert und kann daher nicht als **const**deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="e0c93-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="e0c93-121">Das erste Zeichen der Eingabezeichenfolge wird als Platz für ein Längenzeichen behandelt und von dieser Funktion überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0c93-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0c93-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0c93-122">See also</span></span>



[<span data-ttu-id="e0c93-123">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="e0c93-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


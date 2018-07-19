---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Tempstr-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790578"
---
# <a name="tempstr"></a><span data-ttu-id="63ee3-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="63ee3-104">TempStr</span></span>

 <span data-ttu-id="63ee3-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="63ee3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="63ee3-106">Veraltete Framework Bibliothek-Funktion, die eine temporäre **XLOPER** mit einer **XltypeStr** Byte-Zeichenfolge erstellt.</span><span class="sxs-lookup"><span data-stu-id="63ee3-106">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string.</span></span> <span data-ttu-id="63ee3-107">Es wird eine mit Null endende Quellzeichenfolge als Eingabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="63ee3-107">It takes a null-terminated source string as input.</span></span> <span data-ttu-id="63ee3-108">Er versucht, das erste Zeichen der angegebenen Zeichenfolge mit den nachfolgenden Zeichenfolgenlänge zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="63ee3-108">It tries to overwrite the first character of the supplied string with the subsequent string's length.</span></span> <span data-ttu-id="63ee3-109">Dies ist es nicht immer eine sichere: Microsoft Excel schlagen fehl, wenn eine nur-Lese-Zeichenfolge übergeben.</span><span class="sxs-lookup"><span data-stu-id="63ee3-109">This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="63ee3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="63ee3-110">Parameters</span></span>

 <span data-ttu-id="63ee3-111">_Str_</span><span class="sxs-lookup"><span data-stu-id="63ee3-111">_str_</span></span>
  
<span data-ttu-id="63ee3-112">Ein Zeiger auf die mit Null endende Quellzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="63ee3-112">A pointer to the null-terminated source string.</span></span> <span data-ttu-id="63ee3-113">**TempStr** kürzt Zeichenfolgen, die länger als 255 Byte sind.</span><span class="sxs-lookup"><span data-stu-id="63ee3-113">**TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="63ee3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63ee3-114">Return value</span></span>

<span data-ttu-id="63ee3-115">Eine **XltypeStr** Zeichenfolge enthält einen Zeiger auf den Puffer übergebene Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63ee3-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="63ee3-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63ee3-116">Remarks</span></span>

<span data-ttu-id="63ee3-117">Auf diese Weise über das Erstellen der temporärer Zeichenfolgen ist durch die Möglichkeit, in denen sowohl [TempStrConst und TempStr12](tempstrconst-tempstr12.md) jetzt veraltet.</span><span class="sxs-lookup"><span data-stu-id="63ee3-117">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work.</span></span> <span data-ttu-id="63ee3-118">Diese Funktionen ein neuer Speicher Puffer und kopieren Sie die übergebene Zeichenfolge hinein.</span><span class="sxs-lookup"><span data-stu-id="63ee3-118">These functions allocate a new memory buffer and copy the passed-in string into it.</span></span> <span data-ttu-id="63ee3-119">Die Zeichenfolgen für **TempStrConst** und **TempStr12** nicht geändert werden und werden daher als **Konstante**deklariert.</span><span class="sxs-lookup"><span data-stu-id="63ee3-119">The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**.</span></span> <span data-ttu-id="63ee3-120">Im Gegensatz dazu die input-Zeichenfolge, die **TempStr** wird geändert und kann nicht als **Konstante**deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="63ee3-120">In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**.</span></span> <span data-ttu-id="63ee3-121">Das erste Zeichen der input-Zeichenfolge wird als Speicherplatz für ein Länge Zeichen behandelt und wird durch diese Funktion überschrieben.</span><span class="sxs-lookup"><span data-stu-id="63ee3-121">The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63ee3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63ee3-122">See also</span></span>



[<span data-ttu-id="63ee3-123">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="63ee3-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)


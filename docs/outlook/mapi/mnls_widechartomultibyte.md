---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Letzte Änderung: 21. Februar 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338731"
---
# <a name="mnls_widechartomultibyte"></a><span data-ttu-id="65841-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="65841-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="65841-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65841-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65841-105">Diese Funktion ähnelt **WideCharToMultiByte**, das eine UTF-16-Zeichenfolge (breite Zeichen) einer neuen Zeichenzeichenfolge zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="65841-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="65841-106">Die neue Zeichenzeichenfolge ist nicht unbedingt aus einem Mehrbyte-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="65841-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a><span data-ttu-id="65841-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="65841-107">Parameters</span></span>

 <span data-ttu-id="65841-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="65841-108">_uCodePage_</span></span>
  
> <span data-ttu-id="65841-109">[in] Codeseite, die beim Ausführen der Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="65841-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="65841-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="65841-110">_dwFlags_</span></span>
  
> <span data-ttu-id="65841-111">[in] Flags, die den Konvertierungstyp angeben.</span><span class="sxs-lookup"><span data-stu-id="65841-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="65841-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="65841-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="65841-113">[in] Zeiger auf die zu konvertierende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="65841-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="65841-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="65841-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="65841-115">[in] Flags, die den Konvertierungstyp angeben.</span><span class="sxs-lookup"><span data-stu-id="65841-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="65841-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="65841-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="65841-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="65841-117">[out] Optional.</span></span> <span data-ttu-id="65841-118">Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="65841-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="65841-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="65841-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="65841-120">[in] Größe des puffers in Bytes, der durch _lpMultiByteStr angegeben wird._</span><span class="sxs-lookup"><span data-stu-id="65841-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="65841-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="65841-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="65841-122">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="65841-122">[in] Optional.</span></span> <span data-ttu-id="65841-123">Zeiger auf das zu verwendende Zeichen, wenn ein Zeichen nicht auf der angegebenen Codeseite dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="65841-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="65841-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="65841-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="65841-125">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="65841-125">[out] Optional.</span></span> <span data-ttu-id="65841-126">Zeiger auf ein Flag, das angibt, ob die Funktion in der Konvertierung ein Standardzeichen verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="65841-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65841-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65841-127">Return value</span></span>

<span data-ttu-id="65841-128">Gibt die Anzahl der Bytes zurück, die in den Puffer geschrieben werden, auf den  _lpMultiByteStr_ verweist, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="65841-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="65841-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65841-129">Remarks</span></span>

<span data-ttu-id="65841-130">Diese Funktion umschließt die **WideCharToMultiByte-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="65841-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="65841-131">Weitere Informationen finden Sie unter [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="65841-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65841-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65841-132">See also</span></span>



[<span data-ttu-id="65841-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="65841-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)


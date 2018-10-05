---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385515"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="2b67e-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="2b67e-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="2b67e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b67e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b67e-105">Diese Funktion ähnelt **WideCharToMultiByte**, der eine Zeichenfolge mit UTF-16 (Breitzeichen) in eine neue Zeichenfolge zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2b67e-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="2b67e-106">Die neue Zeichenfolge ist nicht unbedingt aus einem multibyte-Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b67e-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2b67e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b67e-107">Parameters</span></span>

 <span data-ttu-id="2b67e-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="2b67e-108">_uCodePage_</span></span>
  
> <span data-ttu-id="2b67e-109">[in] Codepage verwendet wird, in die Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b67e-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="2b67e-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="2b67e-110">_dwFlags_</span></span>
  
> <span data-ttu-id="2b67e-111">[in] Flags, die den Typ für die Konvertierung angibt.</span><span class="sxs-lookup"><span data-stu-id="2b67e-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="2b67e-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="2b67e-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="2b67e-113">[in] Zeiger auf die Unicode-Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="2b67e-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="2b67e-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="2b67e-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="2b67e-115">[in] Flags, die den Typ für die Konvertierung angibt.</span><span class="sxs-lookup"><span data-stu-id="2b67e-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="2b67e-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="2b67e-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="2b67e-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="2b67e-117">[out] Optional.</span></span> <span data-ttu-id="2b67e-118">Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="2b67e-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="2b67e-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="2b67e-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="2b67e-120">[in] Größe des Puffers durch _LpMultiByteStr_in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2b67e-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="2b67e-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="2b67e-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="2b67e-122">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="2b67e-122">[in] Optional.</span></span> <span data-ttu-id="2b67e-123">Zeiger auf das Zeichen verwenden, wenn ein Zeichen in der angegebenen Codepage dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b67e-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="2b67e-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="2b67e-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="2b67e-125">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="2b67e-125">[out] Optional.</span></span> <span data-ttu-id="2b67e-126">Zeiger auf ein Flag, das angibt, ob die Funktion einer Standardwerte für die Zeichen in der Konvertierung verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="2b67e-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2b67e-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b67e-127">Return value</span></span>

<span data-ttu-id="2b67e-128">Gibt die Anzahl der in den Puffer auf den _LpMultiByteStr_ bei erfolgreicher geschriebenen Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="2b67e-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2b67e-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b67e-129">Remarks</span></span>

<span data-ttu-id="2b67e-130">Diese Funktion wird die Funktion **WideCharToMultiByte** umbrochen.</span><span class="sxs-lookup"><span data-stu-id="2b67e-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="2b67e-131">Weitere Informationen finden Sie unter [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2b67e-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b67e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b67e-132">See also</span></span>



[<span data-ttu-id="2b67e-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="2b67e-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)


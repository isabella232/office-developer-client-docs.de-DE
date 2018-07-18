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
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793286"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="5e106-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="5e106-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="5e106-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e106-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e106-105">Diese Funktion ähnelt **WideCharToMultiByte**, der eine Zeichenfolge mit UTF-16 (Breitzeichen) in eine neue Zeichenfolge zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5e106-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="5e106-106">Die neue Zeichenfolge ist nicht unbedingt aus einem multibyte-Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5e106-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5e106-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e106-107">Parameters</span></span>

 <span data-ttu-id="5e106-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="5e106-108">_uCodePage_</span></span>
  
> <span data-ttu-id="5e106-109">[in] Codepage verwendet wird, in die Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e106-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="5e106-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5e106-110">_dwFlags_</span></span>
  
> <span data-ttu-id="5e106-111">[in] Flags, die den Typ für die Konvertierung angibt.</span><span class="sxs-lookup"><span data-stu-id="5e106-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="5e106-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="5e106-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="5e106-113">[in] Zeiger auf die Unicode-Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5e106-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="5e106-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="5e106-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="5e106-115">[in] Flags, die den Typ für die Konvertierung angibt.</span><span class="sxs-lookup"><span data-stu-id="5e106-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="5e106-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="5e106-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="5e106-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="5e106-117">[out] Optional.</span></span> <span data-ttu-id="5e106-118">Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="5e106-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="5e106-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="5e106-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="5e106-120">[in] Größe des Puffers durch _LpMultiByteStr_in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5e106-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="5e106-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="5e106-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="5e106-122">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="5e106-122">[in] Optional.</span></span> <span data-ttu-id="5e106-123">Zeiger auf das Zeichen verwenden, wenn ein Zeichen in der angegebenen Codepage dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e106-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="5e106-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="5e106-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="5e106-125">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="5e106-125">[out] Optional.</span></span> <span data-ttu-id="5e106-126">Zeiger auf ein Flag, das angibt, ob die Funktion einer Standardwerte für die Zeichen in der Konvertierung verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="5e106-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e106-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5e106-127">Return value</span></span>

<span data-ttu-id="5e106-128">Gibt die Anzahl der in den Puffer auf den _LpMultiByteStr_ bei erfolgreicher geschriebenen Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="5e106-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5e106-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e106-129">Remarks</span></span>

<span data-ttu-id="5e106-130">Diese Funktion wird die Funktion **WideCharToMultiByte** umbrochen.</span><span class="sxs-lookup"><span data-stu-id="5e106-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="5e106-131">Weitere Informationen finden Sie unter [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e106-131">For more information, see [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5e106-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e106-132">See also</span></span>



[<span data-ttu-id="5e106-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="5e106-133">WideCharToMultiByte</span></span>](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)


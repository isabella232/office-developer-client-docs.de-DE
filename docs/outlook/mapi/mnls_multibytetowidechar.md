---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Zuletzt geändert: 21 Februar 2012'
ms.openlocfilehash: 66e8c3b61caac6fb8d8b57d74ade6fa8aac3a9dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571705"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="02a20-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="02a20-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="02a20-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02a20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02a20-105">Vergleichbar mit der **MultiByteToWideChar**, der eine Zeichenfolge in einen String UTF-16 (Breitzeichen) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02a20-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="02a20-106">Die Zeichenfolge ist nicht unbedingt aus einem multibyte-Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02a20-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="02a20-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02a20-107">Parameters</span></span>

 <span data-ttu-id="02a20-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="02a20-108">_uCodePage_</span></span>
  
> <span data-ttu-id="02a20-109">[in] Codepage verwendet wird, in die Konvertierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02a20-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="02a20-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="02a20-110">_dwFlags_</span></span>
  
> <span data-ttu-id="02a20-111">[in] Flags, die den Typ für die Konvertierung angibt.</span><span class="sxs-lookup"><span data-stu-id="02a20-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="02a20-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="02a20-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="02a20-113">[in] Zeiger auf die Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="02a20-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="02a20-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="02a20-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="02a20-115">[in] Größe in Bytes, der von der _LpMultiByteStr_ -Parameter angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="02a20-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="02a20-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="02a20-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="02a20-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="02a20-117">[out] Optional.</span></span> <span data-ttu-id="02a20-118">Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="02a20-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="02a20-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="02a20-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="02a20-120">[in] Größe des Puffers durch _LpWideCharStr_in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="02a20-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02a20-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="02a20-121">Return value</span></span>

<span data-ttu-id="02a20-122">Gibt die Anzahl der Zeichen in den Puffer angegeben durch _LpWideCharStr_ bei erfolgreicher geschriebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="02a20-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02a20-123">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="02a20-123">Remarks</span></span>

<span data-ttu-id="02a20-124">Diese Funktion wird die Funktion **MultiByteToWideChar** umbrochen.</span><span class="sxs-lookup"><span data-stu-id="02a20-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="02a20-125">Weitere Informationen finden Sie unter [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="02a20-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span></span>
  


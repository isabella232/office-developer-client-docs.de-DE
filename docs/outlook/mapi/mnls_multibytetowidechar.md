---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Zuletzt geändert: 21, 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338241"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="5c58d-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="5c58d-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="5c58d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c58d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c58d-105">Ähnlich wie **MultiByteToWideChar**wird eine zeichenFOLGE einer UTF-16-Zeichenfolge zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5c58d-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="5c58d-106">Die Zeichenfolge ist nicht unbedingt aus einem Mehrbyte-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="5c58d-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="5c58d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c58d-107">Parameters</span></span>

 <span data-ttu-id="5c58d-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="5c58d-108">_uCodePage_</span></span>
  
> <span data-ttu-id="5c58d-109">in Codepage, die beim Ausführen der Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c58d-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="5c58d-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5c58d-110">_dwFlags_</span></span>
  
> <span data-ttu-id="5c58d-111">in Flags, die den Konvertierungs angeben.</span><span class="sxs-lookup"><span data-stu-id="5c58d-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="5c58d-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="5c58d-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="5c58d-113">in Zeiger auf die Zeichenfolge, die konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c58d-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="5c58d-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="5c58d-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="5c58d-115">in Größe (in Bytes) der vom _lpMultiByteStr_ -Parameter angegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5c58d-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="5c58d-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="5c58d-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="5c58d-117">[out] Optional.</span><span class="sxs-lookup"><span data-stu-id="5c58d-117">[out] Optional.</span></span> <span data-ttu-id="5c58d-118">Zeiger auf einen Puffer, der die konvertierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="5c58d-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="5c58d-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="5c58d-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="5c58d-120">in Die Größe des von _lpWideCharStr_angegebenen Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5c58d-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c58d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c58d-121">Return value</span></span>

<span data-ttu-id="5c58d-122">Gibt die Anzahl von Zeichen zurück, die in den von _lpWideCharStr_ angegebenen Puffer geschrieben werden, falls erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5c58d-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5c58d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c58d-123">Remarks</span></span>

<span data-ttu-id="5c58d-124">Diese Funktion umschließt die **MultiByteToWideChar** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5c58d-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="5c58d-125">Weitere Informationen finden Sie unter [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5c58d-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  


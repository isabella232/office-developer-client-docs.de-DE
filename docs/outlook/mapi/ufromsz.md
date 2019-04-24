---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346536"
---
# <a name="ufromsz"></a><span data-ttu-id="5f9e1-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="5f9e1-103">UFromSz</span></span>

  
  
<span data-ttu-id="5f9e1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f9e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f9e1-105">Konvertiert eine NULL-terminierte Zeichenfolge von Dezimalstellen in eine unsignierte Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f9e1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5f9e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f9e1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5f9e1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5f9e1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5f9e1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5f9e1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5f9e1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5f9e1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5f9e1-110">Called by:</span></span>  <br/> |<span data-ttu-id="5f9e1-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5f9e1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="5f9e1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f9e1-112">Parameters</span></span>

 <span data-ttu-id="5f9e1-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="5f9e1-113">_lpsz_</span></span>
  
> <span data-ttu-id="5f9e1-114">in Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="5f9e1-115">Der _lpsz_ -parameter darf 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5f9e1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f9e1-116">Return value</span></span>

 <span data-ttu-id="5f9e1-117">**UFromSz** gibt eine ganze Zahl ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="5f9e1-118">Wenn die Zeichenfolge nicht mit mindestens einer Dezimalstelle beginnt, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5f9e1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f9e1-119">Remarks</span></span>

<span data-ttu-id="5f9e1-120">Die **UFromSz** -Funktion wird nicht mehr konvertiert, wenn Sie das erste Zeichen in der Zeichenfolge erreicht, die keine Dezimalziffer ist.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="5f9e1-121">Beispiel: bei der Zeichenfolge "55" gibt **UFromSz** den ganzzahligen Wert 55 zurück.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="5f9e1-122">Bei der Zeichenfolge "5a5b" gibt die Funktion den ganzzahligen Wert 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="5f9e1-123">Bei der Zeichenfolge "a5b5" gibt **UFromSz** NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="5f9e1-124">**UFromSz** ist anfällig für diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="5f9e1-125">Zeichenfolgen im Unicode-und DBCS-Format werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="5f9e1-126">Die Längenbeschränkung für _lpsz_ ist in Zeichen, nicht unbedingt in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5f9e1-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  


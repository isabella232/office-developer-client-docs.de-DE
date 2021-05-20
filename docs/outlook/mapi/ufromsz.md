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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439009"
---
# <a name="ufromsz"></a><span data-ttu-id="51878-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="51878-103">UFromSz</span></span>

  
  
<span data-ttu-id="51878-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51878-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51878-105">Wandelt eine mit Null beendete Zeichenfolge von Dezimalstellen in eine ganze Zahl ohne Vorzeichen um.</span><span class="sxs-lookup"><span data-stu-id="51878-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51878-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="51878-106">Header file:</span></span>  <br/> |<span data-ttu-id="51878-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51878-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="51878-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="51878-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="51878-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="51878-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="51878-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="51878-110">Called by:</span></span>  <br/> |<span data-ttu-id="51878-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="51878-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="51878-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="51878-112">Parameters</span></span>

 <span data-ttu-id="51878-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="51878-113">_lpsz_</span></span>
  
> <span data-ttu-id="51878-114">[in] Zeiger auf die zu konvertierte Zeichenfolge mit Nullen terminiert.</span><span class="sxs-lookup"><span data-stu-id="51878-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="51878-115">Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="51878-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="51878-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51878-116">Return value</span></span>

 <span data-ttu-id="51878-117">**UFromSz** gibt eine ganze Zahl ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="51878-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="51878-118">Wenn die Zeichenfolge nicht mit mindestens einer Dezimalziffer beginnt, wird Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51878-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="51878-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51878-119">Remarks</span></span>

<span data-ttu-id="51878-120">Die **UFromSz-Funktion** beendet die Konvertierung, wenn sie das erste Zeichen in der Zeichenfolge erreicht, das keine Dezimalziffer ist.</span><span class="sxs-lookup"><span data-stu-id="51878-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="51878-121">Bei der Zeichenfolge "55" gibt **UFromSz** beispielsweise den ganzzahligen Wert 55 zurück.</span><span class="sxs-lookup"><span data-stu-id="51878-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="51878-122">Angesichts der Zeichenfolge "5a5b" gibt die Funktion den ganzzahligen Wert 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="51878-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="51878-123">Angesichts der Zeichenfolge "a5b5" gibt **UFromSz** null zurück.</span><span class="sxs-lookup"><span data-stu-id="51878-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="51878-124">**UFromSz** ist für diakritische Unterschiede sensibel.</span><span class="sxs-lookup"><span data-stu-id="51878-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="51878-125">Zeichenfolgen in den Formaten Unicode und DBCS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51878-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="51878-126">Der Längengrenzwert für  _lpsz_ beträgt Zeichen, nicht unbedingt Byte.</span><span class="sxs-lookup"><span data-stu-id="51878-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  


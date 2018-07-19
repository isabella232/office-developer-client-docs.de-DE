---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795786"
---
# <a name="ulfromszhex"></a><span data-ttu-id="0d3c4-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="0d3c4-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="0d3c4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d3c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d3c4-105">Konvertiert eine mit Null endende Zeichenfolge von Hexadezimalzahlen in eine lange Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d3c4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0d3c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d3c4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d3c4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0d3c4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0d3c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d3c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d3c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d3c4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0d3c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d3c4-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0d3c4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="0d3c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d3c4-112">Parameters</span></span>

 <span data-ttu-id="0d3c4-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="0d3c4-113">_lpsz_</span></span>
  
> <span data-ttu-id="0d3c4-114">[in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="0d3c4-115">Der Parameter _Lpsz_ muss 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d3c4-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d3c4-116">Return value</span></span>

 <span data-ttu-id="0d3c4-117">**UlFromSzHex** gibt eine lange Ganzzahl ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="0d3c4-118">Wenn die Zeichenfolge nicht mit mindestens eine hexadezimale Ziffer beginnt, wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0d3c4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d3c4-119">Remarks</span></span>

<span data-ttu-id="0d3c4-120">Die Funktion **UlFromSzHex** beendet konvertieren, wenn das erste Zeichen in der Zeichenfolge, die keine hexadezimale Ziffer ist erreicht.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="0d3c4-121">Beispielsweise gibt **UlFromSzHex** die Zeichenfolge "5a" wird angegeben, den Ganzzahlwert 90.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="0d3c4-122">Die Zeichenfolge "5g5h" angegeben, gibt die Funktion den ganzzahligen Wert 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="0d3c4-123">Wenn die Zeichenfolge "g5h5", gibt **UlFromSzHex** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="0d3c4-124">**UlFromSzHex** wird entsprechend diakritischen Unterschiede ermöglicht aber auch "a" bis "f" und "A" bis "F" für Hexadezimalzahlen.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="0d3c4-125">In den Formaten Unicode und DBCS Zeichenfolgen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="0d3c4-126">Die maximale Länge _Lpsz_ ist in Zeichen, was nicht notwendigerweise Bytes.</span><span class="sxs-lookup"><span data-stu-id="0d3c4-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  


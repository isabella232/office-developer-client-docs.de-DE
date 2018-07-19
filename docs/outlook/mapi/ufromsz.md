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
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795796"
---
# <a name="ufromsz"></a><span data-ttu-id="73cd6-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="73cd6-103">UFromSz</span></span>

  
  
<span data-ttu-id="73cd6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73cd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73cd6-105">Konvertiert eine mit Null endende Zeichenfolge der Nachkommastellen in ganze Zahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="73cd6-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73cd6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="73cd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="73cd6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73cd6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="73cd6-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="73cd6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="73cd6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="73cd6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="73cd6-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="73cd6-110">Called by:</span></span>  <br/> |<span data-ttu-id="73cd6-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="73cd6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="73cd6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="73cd6-112">Parameters</span></span>

 <span data-ttu-id="73cd6-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="73cd6-113">_lpsz_</span></span>
  
> <span data-ttu-id="73cd6-114">[in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="73cd6-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="73cd6-115">Der Parameter _Lpsz_ muss 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="73cd6-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="73cd6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73cd6-116">Return value</span></span>

 <span data-ttu-id="73cd6-117">**UFromSz** gibt eine Ganzzahl ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="73cd6-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="73cd6-118">Wenn die Zeichenfolge nicht mit mindestens eine Dezimalzahl beginnt, wird 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="73cd6-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73cd6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73cd6-119">Remarks</span></span>

<span data-ttu-id="73cd6-120">Die Funktion **UFromSz** beendet konvertieren, wenn das erste Zeichen in der Zeichenfolge, die kein Dezimalzahl ist erreicht.</span><span class="sxs-lookup"><span data-stu-id="73cd6-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="73cd6-121">Beispielsweise gibt **UFromSz** die Zeichenfolge "55" angegeben, den Ganzzahlwert 55.</span><span class="sxs-lookup"><span data-stu-id="73cd6-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="73cd6-122">Die Zeichenfolge "5a5b" angegeben, gibt die Funktion den ganzzahligen Wert 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="73cd6-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="73cd6-123">Wenn die Zeichenfolge "a5b5", gibt **UFromSz** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="73cd6-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="73cd6-124">**UFromSz** wird Kleinschreibung mit diakritischen Zeichen unterschieden.</span><span class="sxs-lookup"><span data-stu-id="73cd6-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="73cd6-125">In den Formaten Unicode und DBCS Zeichenfolgen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73cd6-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="73cd6-126">Die maximale Länge _Lpsz_ ist in Zeichen, was nicht notwendigerweise Bytes.</span><span class="sxs-lookup"><span data-stu-id="73cd6-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  


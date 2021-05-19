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
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433052"
---
# <a name="ulfromszhex"></a><span data-ttu-id="3c146-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="3c146-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="3c146-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c146-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c146-105">Wandelt eine mit Null beendete Zeichenfolge von Hexadezimalziffern in eine nicht signierte lange ganze Zahl um.</span><span class="sxs-lookup"><span data-stu-id="3c146-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c146-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3c146-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c146-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c146-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3c146-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3c146-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c146-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3c146-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3c146-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3c146-110">Called by:</span></span>  <br/> |<span data-ttu-id="3c146-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="3c146-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="3c146-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c146-112">Parameters</span></span>

 <span data-ttu-id="3c146-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="3c146-113">_lpsz_</span></span>
  
> <span data-ttu-id="3c146-114">[in] Zeiger auf die zu konvertierte Zeichenfolge mit Nullen terminiert.</span><span class="sxs-lookup"><span data-stu-id="3c146-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="3c146-115">Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="3c146-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3c146-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c146-116">Return value</span></span>

 <span data-ttu-id="3c146-117">**UlFromSzHex gibt** eine nicht signierte lange ganze Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="3c146-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="3c146-118">Wenn die Zeichenfolge nicht mit mindestens einer hexadezimalen Ziffer beginnt, wird Null zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c146-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3c146-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c146-119">Remarks</span></span>

<span data-ttu-id="3c146-120">Die **UlFromSzHex-Funktion** beendet die Konvertierung, wenn sie das erste Zeichen in der Zeichenfolge erreicht, das keine hexadezimale Ziffer ist.</span><span class="sxs-lookup"><span data-stu-id="3c146-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="3c146-121">Wenn beispielsweise die Zeichenfolge "5a" angegeben wird, gibt **UlFromSzHex** den ganzzahligen Wert 90 zurück.</span><span class="sxs-lookup"><span data-stu-id="3c146-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="3c146-122">Angesichts der Zeichenfolge "5g5h" gibt die Funktion den ganzzahligen Wert 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="3c146-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="3c146-123">Angesichts der Zeichenfolge "g5h5" gibt **UlFromSzHex** null zurück.</span><span class="sxs-lookup"><span data-stu-id="3c146-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="3c146-124">**UlFromSzHex** ist für diakritische Unterschiede sensibel, ermöglicht jedoch sowohl "a" über "f" als auch "A" bis "F" für Hexadezimalziffern.</span><span class="sxs-lookup"><span data-stu-id="3c146-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="3c146-125">Zeichenfolgen in den Formaten Unicode und DBCS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c146-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="3c146-126">Der Längengrenzwert für  _lpsz_ beträgt Zeichen, nicht unbedingt Byte.</span><span class="sxs-lookup"><span data-stu-id="3c146-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  


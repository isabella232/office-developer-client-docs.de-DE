---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87a470c1c682225eb1deefba9ccc8c12fbdc49c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569827"
---
# <a name="fbinfromhex"></a><span data-ttu-id="fce4b-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="fce4b-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="fce4b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fce4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fce4b-105">Zeichenfolgendarstellung einer eine hexadezimale Zahl konvertiert um Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="fce4b-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fce4b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fce4b-106">Header file:</span></span>  <br/> |<span data-ttu-id="fce4b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fce4b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fce4b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fce4b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fce4b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fce4b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fce4b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fce4b-110">Called by:</span></span>  <br/> |<span data-ttu-id="fce4b-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fce4b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="fce4b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fce4b-112">Parameters</span></span>

 <span data-ttu-id="fce4b-113">_su_</span><span class="sxs-lookup"><span data-stu-id="fce4b-113">_sz_</span></span>
  
> <span data-ttu-id="fce4b-114">[in] Zeiger auf Null endende ASCII-Zeichenfolge konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fce4b-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="fce4b-115">Es ist keine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fce4b-115">It is not a Unicode string.</span></span> <span data-ttu-id="fce4b-116">Gültige Zeichen umfassen die Hexadezimalzeichen 0 (null) bis neun und sowohl Groß- und Kleinbuchstaben Zeichen A bis F.</span><span class="sxs-lookup"><span data-stu-id="fce4b-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="fce4b-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="fce4b-117">_pb_</span></span>
  
> <span data-ttu-id="fce4b-118">[out] Zeiger auf das zurückgegebene binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="fce4b-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fce4b-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fce4b-119">Return value</span></span>

<span data-ttu-id="fce4b-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="fce4b-120">TRUE</span></span> 
  
> <span data-ttu-id="fce4b-121">Die Zeichenfolge wurde erfolgreich in eine binäre Zahl konvertiert.</span><span class="sxs-lookup"><span data-stu-id="fce4b-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="fce4b-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="fce4b-122">FALSE</span></span> 
  
> <span data-ttu-id="fce4b-123">Die eingegebene Zeichenfolge enthält ungültige hexadezimale ASCII-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fce4b-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fce4b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fce4b-124">See also</span></span>



[<span data-ttu-id="fce4b-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="fce4b-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)


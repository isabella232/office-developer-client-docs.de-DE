---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357498"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="fa9b4-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="fa9b4-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="fa9b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa9b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa9b4-105">Konvertiert den angegebenen Teil einer Zeichenfolgendarstellung einer hexadezimalen Zahl in eine binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa9b4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fa9b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa9b4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="fa9b4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fa9b4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fa9b4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa9b4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa9b4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa9b4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fa9b4-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa9b4-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fa9b4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="fa9b4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa9b4-112">Parameters</span></span>

 <span data-ttu-id="fa9b4-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="fa9b4-113">_sz_</span></span>
  
> <span data-ttu-id="fa9b4-114">in Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="fa9b4-115">Gültige Zeichen sind die Hexadezimalzeichen 0 bis 9 und groß-und Kleinbuchstaben a bis f.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="fa9b4-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="fa9b4-116">_pb_</span></span>
  
> <span data-ttu-id="fa9b4-117">Out Zeiger auf die zurückgegebene binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="fa9b4-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="fa9b4-118">_cb_</span></span>
  
> <span data-ttu-id="fa9b4-119">in Die Größe des _PB_ -Parameters in Byte.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa9b4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa9b4-120">Return value</span></span>

<span data-ttu-id="fa9b4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa9b4-121">S_OK</span></span>
  
> <span data-ttu-id="fa9b4-122">Die Konvertierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-122">Conversion was successful.</span></span>
    
<span data-ttu-id="fa9b4-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="fa9b4-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="fa9b4-124">Ungültige Zeichen wurden gefunden.</span><span class="sxs-lookup"><span data-stu-id="fa9b4-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa9b4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa9b4-125">See also</span></span>



[<span data-ttu-id="fa9b4-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="fa9b4-126">FBinFromHex</span></span>](fbinfromhex.md)


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
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795430"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="8f552-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="8f552-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="8f552-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f552-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f552-105">Konvertiert den angegebenen Teil einer Zeichenfolgendarstellung eine hexadezimale Zahl in eine binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="8f552-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f552-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8f552-106">Header file:</span></span>  <br/> |<span data-ttu-id="8f552-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8f552-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8f552-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8f552-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8f552-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8f552-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8f552-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8f552-110">Called by:</span></span>  <br/> |<span data-ttu-id="8f552-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8f552-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="8f552-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f552-112">Parameters</span></span>

 <span data-ttu-id="8f552-113">_su_</span><span class="sxs-lookup"><span data-stu-id="8f552-113">_sz_</span></span>
  
> <span data-ttu-id="8f552-114">[in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f552-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="8f552-115">Gültige Zeichen umfassen den Hexadezimalzeichen 0 bis 9 und beide Zeichen von Groß- und Kleinbuchstaben a bis f.</span><span class="sxs-lookup"><span data-stu-id="8f552-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="8f552-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="8f552-116">_pb_</span></span>
  
> <span data-ttu-id="8f552-117">[out] Zeiger auf das zurückgegebene binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="8f552-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="8f552-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="8f552-118">_cb_</span></span>
  
> <span data-ttu-id="8f552-119">[in] Größe des Parameters _pb_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8f552-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8f552-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8f552-120">Return value</span></span>

<span data-ttu-id="8f552-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f552-121">S_OK</span></span>
  
> <span data-ttu-id="8f552-122">Konvertierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="8f552-122">Conversion was successful.</span></span>
    
<span data-ttu-id="8f552-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="8f552-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="8f552-124">Ungültige Zeichen sind aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8f552-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f552-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f552-125">See also</span></span>



[<span data-ttu-id="8f552-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="8f552-126">FBinFromHex</span></span>](fbinfromhex.md)


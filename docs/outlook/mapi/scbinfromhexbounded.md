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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589280"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="12fad-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="12fad-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="12fad-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12fad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12fad-105">Konvertiert den angegebenen Teil einer Zeichenfolgendarstellung eine hexadezimale Zahl in eine binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="12fad-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12fad-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="12fad-106">Header file:</span></span>  <br/> |<span data-ttu-id="12fad-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="12fad-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="12fad-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="12fad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="12fad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="12fad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="12fad-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="12fad-110">Called by:</span></span>  <br/> |<span data-ttu-id="12fad-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="12fad-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="12fad-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="12fad-112">Parameters</span></span>

 <span data-ttu-id="12fad-113">_su_</span><span class="sxs-lookup"><span data-stu-id="12fad-113">_sz_</span></span>
  
> <span data-ttu-id="12fad-114">[in] Zeiger auf die Null-Zeichenfolge konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="12fad-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="12fad-115">Gültige Zeichen umfassen den Hexadezimalzeichen 0 bis 9 und beide Zeichen von Groß- und Kleinbuchstaben a bis f.</span><span class="sxs-lookup"><span data-stu-id="12fad-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="12fad-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="12fad-116">_pb_</span></span>
  
> <span data-ttu-id="12fad-117">[out] Zeiger auf das zurückgegebene binäre Zahl.</span><span class="sxs-lookup"><span data-stu-id="12fad-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="12fad-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="12fad-118">_cb_</span></span>
  
> <span data-ttu-id="12fad-119">[in] Größe des Parameters _pb_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="12fad-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="12fad-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="12fad-120">Return value</span></span>

<span data-ttu-id="12fad-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="12fad-121">S_OK</span></span>
  
> <span data-ttu-id="12fad-122">Konvertierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="12fad-122">Conversion was successful.</span></span>
    
<span data-ttu-id="12fad-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="12fad-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="12fad-124">Ungültige Zeichen sind aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="12fad-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12fad-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12fad-125">See also</span></span>



[<span data-ttu-id="12fad-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="12fad-126">FBinFromHex</span></span>](fbinfromhex.md)


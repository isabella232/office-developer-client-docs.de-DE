---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412576"
---
# <a name="hexfrombin"></a><span data-ttu-id="395fb-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="395fb-103">HexFromBin</span></span>

  
  
<span data-ttu-id="395fb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="395fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="395fb-105">Konvertiert eine binäre Zahl in eine Zeichenfolgendarstellung einer Hexadezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="395fb-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="395fb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="395fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="395fb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="395fb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="395fb-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="395fb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="395fb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="395fb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="395fb-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="395fb-110">Called by:</span></span>  <br/> |<span data-ttu-id="395fb-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="395fb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="395fb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="395fb-112">Parameters</span></span>

 <span data-ttu-id="395fb-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="395fb-113">_pb_</span></span>
  
> <span data-ttu-id="395fb-114">in Zeiger auf die zu konvertierenden Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="395fb-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="395fb-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="395fb-115">_cb_</span></span>
  
> <span data-ttu-id="395fb-116">in Die Größe der Binärdaten, auf die durch den _PB_ -Parameter verwiesen wird, in Byte.</span><span class="sxs-lookup"><span data-stu-id="395fb-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="395fb-117">_SZ_</span><span class="sxs-lookup"><span data-stu-id="395fb-117">_sz_</span></span>
  
> <span data-ttu-id="395fb-118">Out Zeiger auf eine mit NULL endende ASCII-Zeichenfolge, die die Binärdaten in Hexadezimalziffern darstellt.</span><span class="sxs-lookup"><span data-stu-id="395fb-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="395fb-119">Return value</span><span class="sxs-lookup"><span data-stu-id="395fb-119">Return value</span></span>

<span data-ttu-id="395fb-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="395fb-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="395fb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="395fb-121">Remarks</span></span>

<span data-ttu-id="395fb-122">Die **HexFromBin** -Funktion verwendet einen Zeiger auf eine Einheit von Binärdaten, deren Größe durch den _CB_ -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="395fb-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="395fb-123">In der _SZ_ -Zeichenfolge wird innerhalb von (2 \* _CB_) + 1 Byte des Arbeitsspeichers eine Darstellung dieser Binärinformationen in Hexadezimalzahlen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="395fb-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="395fb-124">Wenn der Byte-Wert dezimal 10 ist, wird beispielsweise die hexadezimale Zeichenfolge 0A, sodass ein Byte in zwei Bytes in der Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="395fb-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  


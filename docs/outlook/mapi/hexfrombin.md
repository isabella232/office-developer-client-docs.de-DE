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
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791859"
---
# <a name="hexfrombin"></a><span data-ttu-id="0219b-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="0219b-103">HexFromBin</span></span>

  
  
<span data-ttu-id="0219b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0219b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0219b-105">Konvertiert eine binäre Zahl in eine String-Darstellung eine hexadezimale Zahl.</span><span class="sxs-lookup"><span data-stu-id="0219b-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0219b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0219b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0219b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0219b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0219b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0219b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0219b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0219b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0219b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0219b-110">Called by:</span></span>  <br/> |<span data-ttu-id="0219b-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0219b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="0219b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0219b-112">Parameters</span></span>

 <span data-ttu-id="0219b-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="0219b-113">_pb_</span></span>
  
> <span data-ttu-id="0219b-114">[in] Zeiger auf die binären Daten konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0219b-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="0219b-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="0219b-115">_cb_</span></span>
  
> <span data-ttu-id="0219b-116">[in] Größe in Bytes, die binären Daten, die durch den Parameter _pb_ auf.</span><span class="sxs-lookup"><span data-stu-id="0219b-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="0219b-117">_su_</span><span class="sxs-lookup"><span data-stu-id="0219b-117">_sz_</span></span>
  
> <span data-ttu-id="0219b-118">[out] Zeiger auf eine Null endende ASCII-Zeichenfolge, die binären Daten in Hexadezimalzahlen darstellt.</span><span class="sxs-lookup"><span data-stu-id="0219b-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0219b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0219b-119">Return value</span></span>

<span data-ttu-id="0219b-120">None.</span><span class="sxs-lookup"><span data-stu-id="0219b-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0219b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0219b-121">Remarks</span></span>

<span data-ttu-id="0219b-122">Die **HexFromBin** -Funktion verwendet einen Zeiger auf einer Einheit von binären Daten, deren Größe von der _Cb_ -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0219b-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="0219b-123">Es gibt in der Zeichenfolge _su_ innerhalb (2 \* _Cb_) + 1 Byte an Arbeitsspeicher, eine Darstellung dieses Binärdaten in Hexadezimalzahlen.</span><span class="sxs-lookup"><span data-stu-id="0219b-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="0219b-124">Wenn der Bytewert Dezimalzahl 10 ist, beispielsweise werden die hexadezimale Zeichenfolge 0A, dies der Fall ist ein Byte in die beiden Bytes in der Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0219b-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  


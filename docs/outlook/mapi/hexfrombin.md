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
# <a name="hexfrombin"></a><span data-ttu-id="a3530-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="a3530-103">HexFromBin</span></span>

  
  
<span data-ttu-id="a3530-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3530-105">Wandelt eine binäre Zahl in eine Zeichenfolgendarstellung einer hexadezimalen Zahl um.</span><span class="sxs-lookup"><span data-stu-id="a3530-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3530-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a3530-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3530-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3530-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3530-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a3530-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3530-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3530-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3530-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a3530-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3530-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a3530-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="a3530-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3530-112">Parameters</span></span>

 <span data-ttu-id="a3530-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="a3530-113">_pb_</span></span>
  
> <span data-ttu-id="a3530-114">[in] Zeiger auf die zu konvertierten Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="a3530-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="a3530-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="a3530-115">_cb_</span></span>
  
> <span data-ttu-id="a3530-116">[in] Größe der binären Daten, auf die  der pb-Parameter verweist, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a3530-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="a3530-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="a3530-117">_sz_</span></span>
  
> <span data-ttu-id="a3530-118">[out] Zeiger auf eine mit Null beendete ASCII-Zeichenfolge, die die Binärdaten in hexadezimalen Ziffern darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3530-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3530-119">Return value</span><span class="sxs-lookup"><span data-stu-id="a3530-119">Return value</span></span>

<span data-ttu-id="a3530-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3530-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3530-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3530-121">Remarks</span></span>

<span data-ttu-id="a3530-122">Die **HexFromBin-Funktion** verwendet einen Zeiger auf eine Binärdateneinheit, deren Größe durch den  _cb-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="a3530-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="a3530-123">Es gibt in der  _sz-Zeichenfolge_ innerhalb (2\*  _cb_)+1 Byte Arbeitsspeicher eine Darstellung dieser binären Informationen in hexadezimalen Zahlen zurück.</span><span class="sxs-lookup"><span data-stu-id="a3530-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="a3530-124">Wenn der Bytewert z. B. dezimal 10 ist, ist die hexadezimale Zeichenfolge 0A, sodass ein Byte in zwei Bytes in der Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="a3530-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  


---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407844"
---
# <a name="sbinary"></a><span data-ttu-id="521bb-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="521bb-103">SBinary</span></span>

  
  
<span data-ttu-id="521bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="521bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="521bb-105">Beschreibt eine Eigenschaft vom Typ PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="521bb-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="521bb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="521bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="521bb-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="521bb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="521bb-108">Members</span><span class="sxs-lookup"><span data-stu-id="521bb-108">Members</span></span>

 <span data-ttu-id="521bb-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="521bb-109">**cb**</span></span>
  
> <span data-ttu-id="521bb-110">Die Anzahl der Bytes im **LPB** -Element.</span><span class="sxs-lookup"><span data-stu-id="521bb-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="521bb-111">**LPB**</span><span class="sxs-lookup"><span data-stu-id="521bb-111">**lpb**</span></span>
  
> <span data-ttu-id="521bb-112">Zeiger auf den Wert der PT_BINARY-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="521bb-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="521bb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="521bb-113">Remarks</span></span>

<span data-ttu-id="521bb-114">Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="521bb-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="521bb-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="521bb-115">See also</span></span>



[<span data-ttu-id="521bb-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="521bb-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="521bb-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="521bb-117">MAPI Structures</span></span>](mapi-structures.md)


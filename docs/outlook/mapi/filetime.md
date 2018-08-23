---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583253"
---
# <a name="filetime"></a><span data-ttu-id="c89b3-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c89b3-103">FILETIME</span></span>

  
  
<span data-ttu-id="c89b3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c89b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c89b3-105">Enthält eine nicht signierte 64-Bit-Datums- und Uhrzeitwert für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="c89b3-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="c89b3-106">Dieser Wert gibt die Anzahl der Einheiten von 100 Nanosekunden seit dem Start der 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="c89b3-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c89b3-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c89b3-107">Header file:</span></span>  <br/> |<span data-ttu-id="c89b3-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c89b3-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="c89b3-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="c89b3-109">Members</span></span>

 <span data-ttu-id="c89b3-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="c89b3-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="c89b3-111">Niederwertige 32 Bit der Datei Time-Wert.</span><span class="sxs-lookup"><span data-stu-id="c89b3-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="c89b3-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="c89b3-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="c89b3-113">Obere 32 Bit der Datei Time-Wert.</span><span class="sxs-lookup"><span data-stu-id="c89b3-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c89b3-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c89b3-114">Remarks</span></span>

<span data-ttu-id="c89b3-115">Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME** -Struktur für ihren Wert.</span><span class="sxs-lookup"><span data-stu-id="c89b3-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="c89b3-116">Eine solche Eigenschaft hat einen **FILETIME** -Datentyp für den **Wert** Member in der Definition in eine [SPropValue](spropvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c89b3-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="c89b3-117">Die Definition der **FILETIME** -Struktur ist in der _Win32 Programmer's Reference_ und in der MAPI-Headerdatei Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="c89b3-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="c89b3-118">MAPI definiert die Struktur bedingt, um sicherzustellen, dass er definiert wird, wenn die Win32-Definition nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c89b3-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c89b3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c89b3-119">See also</span></span>



[<span data-ttu-id="c89b3-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c89b3-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c89b3-121">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c89b3-121">MAPI Structures</span></span>](mapi-structures.md)


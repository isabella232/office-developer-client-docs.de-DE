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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791686"
---
# <a name="filetime"></a><span data-ttu-id="16f12-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="16f12-103">FILETIME</span></span>

  
  
<span data-ttu-id="16f12-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16f12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16f12-105">Enthält eine nicht signierte 64-Bit-Datums- und Uhrzeitwert für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="16f12-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="16f12-106">Dieser Wert gibt die Anzahl der Einheiten von 100 Nanosekunden seit dem Start der 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="16f12-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16f12-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="16f12-107">Header file:</span></span>  <br/> |<span data-ttu-id="16f12-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16f12-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="16f12-109">Members</span><span class="sxs-lookup"><span data-stu-id="16f12-109">Members</span></span>

 <span data-ttu-id="16f12-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="16f12-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="16f12-111">Niederwertige 32 Bit der Datei Time-Wert.</span><span class="sxs-lookup"><span data-stu-id="16f12-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="16f12-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="16f12-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="16f12-113">Obere 32 Bit der Datei Time-Wert.</span><span class="sxs-lookup"><span data-stu-id="16f12-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16f12-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16f12-114">Remarks</span></span>

<span data-ttu-id="16f12-115">Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME** -Struktur für ihren Wert.</span><span class="sxs-lookup"><span data-stu-id="16f12-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="16f12-116">Eine solche Eigenschaft hat einen **FILETIME** -Datentyp für den **Wert** Member in der Definition in eine [SPropValue](spropvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="16f12-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="16f12-117">Die Definition der **FILETIME** -Struktur ist in der _Win32 Programmer's Reference_ und in der MAPI-Headerdatei Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="16f12-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="16f12-118">MAPI definiert die Struktur bedingt, um sicherzustellen, dass er definiert wird, wenn die Win32-Definition nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="16f12-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16f12-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16f12-119">See also</span></span>



[<span data-ttu-id="16f12-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="16f12-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="16f12-121">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="16f12-121">MAPI Structures</span></span>](mapi-structures.md)


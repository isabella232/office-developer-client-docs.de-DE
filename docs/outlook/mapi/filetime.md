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
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409503"
---
# <a name="filetime"></a><span data-ttu-id="27614-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="27614-103">FILETIME</span></span>

  
  
<span data-ttu-id="27614-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27614-105">Enthält einen nicht signierten 64-Bit-Datums- und Uhrzeitwert für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="27614-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="27614-106">Dieser Wert stellt die Anzahl von 100 Nanosekundeneinheiten seit Dem 1. Januar 1601 dar.</span><span class="sxs-lookup"><span data-stu-id="27614-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27614-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="27614-107">Header file:</span></span>  <br/> |<span data-ttu-id="27614-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27614-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="27614-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="27614-109">Members</span></span>

 <span data-ttu-id="27614-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="27614-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="27614-111">Niedrige Reihenfolge 32 Bit des Dateizeitwerts.</span><span class="sxs-lookup"><span data-stu-id="27614-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="27614-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="27614-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="27614-113">32 Bit des Dateizeitwerts in hoher Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="27614-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27614-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27614-114">Remarks</span></span>

<span data-ttu-id="27614-115">Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME-Struktur** für ihren Wert.</span><span class="sxs-lookup"><span data-stu-id="27614-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="27614-116">Eine solche Eigenschaft verfügt über einen **FILETIME-Datentyp** für das **Value-Element** in seiner Definition in einer [SPropValue-Struktur.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="27614-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="27614-117">Die Definition der **FILETIME-Struktur** befindet sich in  _der Win32-Programmerreferenz_ und in der MAPI-Headerdatei Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="27614-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="27614-118">MAPI definiert die Struktur bedingt, um sicherzustellen, dass sie definiert ist, wenn die Win32-Definition nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="27614-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27614-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27614-119">See also</span></span>



[<span data-ttu-id="27614-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="27614-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="27614-121">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="27614-121">MAPI Structures</span></span>](mapi-structures.md)


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
# <a name="filetime"></a><span data-ttu-id="c052e-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c052e-103">FILETIME</span></span>

  
  
<span data-ttu-id="c052e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c052e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c052e-105">Enthält einen nicht signierten 64-Bit-Wert für Datum und Uhrzeit für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="c052e-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="c052e-106">Dieser Wert stellt die Anzahl von 100-Nanosekunden-Einheiten seit Beginn des 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="c052e-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c052e-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c052e-107">Header file:</span></span>  <br/> |<span data-ttu-id="c052e-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c052e-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="c052e-109">Members</span><span class="sxs-lookup"><span data-stu-id="c052e-109">Members</span></span>

 <span data-ttu-id="c052e-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="c052e-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="c052e-111">Low-Order 32 Bits des dateitime-Werts.</span><span class="sxs-lookup"><span data-stu-id="c052e-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="c052e-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="c052e-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="c052e-113">Hochwertige 32-Bits des dateitime-Werts.</span><span class="sxs-lookup"><span data-stu-id="c052e-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c052e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c052e-114">Remarks</span></span>

<span data-ttu-id="c052e-115">Eine Eigenschaft vom Typ PT_SYSTIME hat eine **FILETIME** -Struktur für ihren Wert.</span><span class="sxs-lookup"><span data-stu-id="c052e-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="c052e-116">Eine solche Eigenschaft verfügt über \*\*\*\* einen FILETIME-Datentyp für das **value** -Element in der Definition in einer [SPropValue](spropvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c052e-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="c052e-117">Die Definition der FILETIME-Struktur befindet sich in der _Win32-Programmierreferenz_ und in der MAPI-Headerdatei Mapidefs. h. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c052e-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="c052e-118">MAPI definiert die strukturbedingt, um sicherzustellen, dass Sie definiert wird, wenn die Win32-Definition nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c052e-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c052e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c052e-119">See also</span></span>



[<span data-ttu-id="c052e-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c052e-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c052e-121">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c052e-121">MAPI Structures</span></span>](mapi-structures.md)


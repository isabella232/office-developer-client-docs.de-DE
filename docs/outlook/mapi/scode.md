---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430133"
---
# <a name="scode"></a><span data-ttu-id="45cf8-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="45cf8-103">SCODE</span></span>

<span data-ttu-id="45cf8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45cf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45cf8-105">Ein 32-Bit-Statuswert, der zum Beschreiben eines Fehlers oder einer Warnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="45cf8-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="45cf8-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45cf8-106">Remarks</span></span>

<span data-ttu-id="45cf8-107">Der **SCODE-Datentyp** ist identisch mit dem [HRESULT-Datentyp.](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="45cf8-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="45cf8-108">Ein **SCODE-Wert** ist in vier Felder unterteilt:</span><span class="sxs-lookup"><span data-stu-id="45cf8-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="45cf8-109">Ein Ein-Bit-Schweregradcode, der auf 0 festgelegt ist, um den Erfolg anzuzeigen, und 1, um einen Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="45cf8-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="45cf8-110">Ein reserviertes 11-Bit-Feld</span><span class="sxs-lookup"><span data-stu-id="45cf8-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="45cf8-111">Ein 4-Bit-Einrichtungscode, der den Bereich angibt, der für den Fehler oder die Warnung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="45cf8-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="45cf8-112">Ein 16-Bit-Fehler oder Warnungscode, der das Problem beschreibt, das den Fehler oder die Warnung verursacht.</span><span class="sxs-lookup"><span data-stu-id="45cf8-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="45cf8-113">Viele der MAPI-Funktionen und -Methoden geben **SCODE-Werte** zurück, die als **HRESULT-Datentypen** definiert sind, ebenso wie die OLE-Methoden und -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="45cf8-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="45cf8-114">OLE definiert mehrere Makros, die zum Konvertieren zwischen einem **SCODE** und einem **HRESULT verwendet werden können.**</span><span class="sxs-lookup"><span data-stu-id="45cf8-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="45cf8-115">In 64-Bit-MAPI ist **SCODE** weiterhin ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="45cf8-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="45cf8-116">Weitere Informationen dazu, wie MAPI den **SCODE-Datentyp** verwendet, finden Sie unter [Error Handling](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="45cf8-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="45cf8-117">Weitere Informationen zu OLE und dem **SCODE-Datentyp** finden Sie unter  *OLE Programmer's Reference*  .</span><span class="sxs-lookup"><span data-stu-id="45cf8-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="45cf8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45cf8-118">See also</span></span>



<span data-ttu-id="45cf8-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="45cf8-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="45cf8-120">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="45cf8-120">MAPI Data Types</span></span>](mapi-data-types.md)


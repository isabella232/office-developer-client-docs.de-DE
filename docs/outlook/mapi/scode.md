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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351240"
---
# <a name="scode"></a><span data-ttu-id="49502-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="49502-103">SCODE</span></span>

<span data-ttu-id="49502-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49502-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49502-105">Ein 32-Bit-Statuswert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="49502-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="49502-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49502-106">Remarks</span></span>

<span data-ttu-id="49502-107">Der **SCODE** -Datentyp ist derselbe wie der [HRESULT](hresult.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="49502-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="49502-108">Ein **SCODE** -Wert ist in vier Felder unterteilt:</span><span class="sxs-lookup"><span data-stu-id="49502-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="49502-109">Ein Single-Bit-Schweregradcode, der auf 0 festgelegt ist, um den Erfolg und 1 zum Anzeigen des Fehlers anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="49502-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="49502-110">Ein reserviertes 11-Bit-Feld</span><span class="sxs-lookup"><span data-stu-id="49502-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="49502-111">Ein 4-Bit-Code, der den für den Fehler oder die Warnung verantwortlichen Bereich angibt.</span><span class="sxs-lookup"><span data-stu-id="49502-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="49502-112">Ein 16-Bit-Fehler oder Warnungscode, der das Problem beschreibt, das den Fehler oder die Warnung verursacht.</span><span class="sxs-lookup"><span data-stu-id="49502-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="49502-113">Viele der MAPI-Funktionen und-Methoden geben **SCODE** -Werte zurück, die als **HRESULT** -Datentypen definiert sind, ebenso wie die OLE-Methoden und-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="49502-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="49502-114">OLE definiert mehrere Makros, die zum Konvertieren zwischen einem **SCODE** und einem **HRESULT**verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="49502-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="49502-115">In 64-Bit-MAPI ist **SCODE** immer noch ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="49502-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="49502-116">Weitere Informationen zur Verwendung des **SCODE** -Datentyps in MAPI finden Sie unter [Error Handling](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="49502-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="49502-117">Weitere Informationen zu OLE und zum **SCODE** -Datentyp finden Sie unter *OLE Programmer es Reference* .</span><span class="sxs-lookup"><span data-stu-id="49502-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49502-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49502-118">See also</span></span>



<span data-ttu-id="49502-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="49502-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="49502-120">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="49502-120">MAPI Data Types</span></span>](mapi-data-types.md)


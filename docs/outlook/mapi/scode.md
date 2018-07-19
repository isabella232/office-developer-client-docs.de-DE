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
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795450"
---
# <a name="scode"></a><span data-ttu-id="19f93-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="19f93-103">SCODE</span></span>

<span data-ttu-id="19f93-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19f93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19f93-105">Eine 32-Bit Statuswert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="19f93-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="19f93-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19f93-106">Remarks</span></span>

<span data-ttu-id="19f93-107">Der Datentyp **SCODE** ist identisch mit der [HRESULT](hresult.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="19f93-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="19f93-108">Ein **SCODE** -Wert wird in vier Felder unterteilt:</span><span class="sxs-lookup"><span data-stu-id="19f93-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="19f93-109">Ein Einzel-Bit Schweregradcode, der auf 0 festgelegt ist, um Erfolg und 1 Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="19f93-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="19f93-110">Ein reserviertes 11-Bit-Feld</span><span class="sxs-lookup"><span data-stu-id="19f93-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="19f93-111">Ein 4-Bit-Facility-Code, der den Bereich verantwortlich für die Fehlermeldung oder einer Warnung angibt.</span><span class="sxs-lookup"><span data-stu-id="19f93-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="19f93-112">Eine 16-Bit-Fehler oder eine Warnung Code, der das Problem beschreibt, das den Fehler verursacht oder einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="19f93-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="19f93-113">Viele der MAPI-Funktionen und Methoden zurückgeben **SCODE** -Werte als **HRESULT** -Datentypen definiert, wie die OLE-Methoden und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="19f93-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="19f93-114">OLE definiert verschiedene Makros, die für die Konvertierung zwischen **SCODE** und ein **HRESULT**verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="19f93-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="19f93-115">In 64-Bit-MAPI ist **SCODE** noch ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="19f93-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="19f93-116">Weitere Informationen dazu, wie den **SCODE** -Datentyp in MAPI verwendet werden finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="19f93-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="19f93-117">Weitere Informationen zu OLE und den Datentyp **SCODE** finden Sie unter der *OLE Programmer's Reference* .</span><span class="sxs-lookup"><span data-stu-id="19f93-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19f93-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19f93-118">See also</span></span>



<span data-ttu-id="19f93-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="19f93-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="19f93-120">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="19f93-120">MAPI Data Types</span></span>](mapi-data-types.md)


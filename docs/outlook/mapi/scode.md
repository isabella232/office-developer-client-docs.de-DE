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
ms.openlocfilehash: 7f8ede3761ca10589c686e2ec4fac18fbe00fb2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588587"
---
# <a name="scode"></a><span data-ttu-id="da331-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="da331-103">SCODE</span></span>

<span data-ttu-id="da331-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da331-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da331-105">Eine 32-Bit Statuswert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="da331-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="da331-106">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="da331-106">Remarks</span></span>

<span data-ttu-id="da331-107">Der Datentyp **SCODE** ist identisch mit der [HRESULT](hresult.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="da331-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="da331-108">Ein **SCODE** -Wert wird in vier Felder unterteilt:</span><span class="sxs-lookup"><span data-stu-id="da331-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="da331-109">Ein Einzel-Bit Schweregradcode, der auf 0 festgelegt ist, um Erfolg und 1 Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="da331-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="da331-110">Ein reserviertes 11-Bit-Feld</span><span class="sxs-lookup"><span data-stu-id="da331-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="da331-111">Ein 4-Bit-Facility-Code, der den Bereich verantwortlich für die Fehlermeldung oder einer Warnung angibt.</span><span class="sxs-lookup"><span data-stu-id="da331-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="da331-112">Eine 16-Bit-Fehler oder eine Warnung Code, der das Problem beschreibt, das den Fehler verursacht oder einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="da331-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="da331-113">Viele der MAPI-Funktionen und Methoden zurückgeben **SCODE** -Werte als **HRESULT** -Datentypen definiert, wie die OLE-Methoden und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="da331-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="da331-114">OLE definiert verschiedene Makros, die für die Konvertierung zwischen **SCODE** und ein **HRESULT**verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="da331-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="da331-115">In 64-Bit-MAPI ist **SCODE** noch ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="da331-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="da331-116">Weitere Informationen dazu, wie den **SCODE** -Datentyp in MAPI verwendet werden finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="da331-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="da331-117">Weitere Informationen zu OLE und den Datentyp **SCODE** finden Sie unter der *OLE Programmer's Reference* .</span><span class="sxs-lookup"><span data-stu-id="da331-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da331-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da331-118">See also</span></span>



<span data-ttu-id="da331-119">[[HRESULT]](hresult.md)</span><span class="sxs-lookup"><span data-stu-id="da331-119">[HRESULT](hresult.md)</span></span>


[<span data-ttu-id="da331-120">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="da331-120">MAPI Data Types</span></span>](mapi-data-types.md)


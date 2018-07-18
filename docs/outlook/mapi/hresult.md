---
title: HRESULT
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
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791905"
---
# <a name="hresult"></a><span data-ttu-id="1b356-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1b356-103">HRESULT</span></span>

  
  
<span data-ttu-id="1b356-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b356-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b356-105">Ein 32-Bit-Wert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1b356-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="1b356-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b356-106">Remarks</span></span>

<span data-ttu-id="1b356-107">Der **HRESULT** -Datentyp ist identisch mit der [SCODE](scode.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1b356-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="1b356-108">Ein **HRESULT** -Wert besteht aus den folgenden Feldern:</span><span class="sxs-lookup"><span data-stu-id="1b356-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="1b356-109">Einen Schweregrad 1-Bit-Code, darstellt wobei 0 (null) Erfolg und 1 steht Fehler.</span><span class="sxs-lookup"><span data-stu-id="1b356-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="1b356-110">Ein reserviertes 4-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="1b356-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="1b356-111">Ein 11-Bit-Code, der angibt, die Verantwortung für die Fehlermeldung oder einer Warnung, auch bekannt als einen Facility Code.</span><span class="sxs-lookup"><span data-stu-id="1b356-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="1b356-112">Ein 16-Bit-Code Beschreibung des Fehlers oder eine Warnung ein.</span><span class="sxs-lookup"><span data-stu-id="1b356-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="1b356-113">Die meisten MAPI-Schnittstellenmethoden und Funktionen zurückgeben **HRESULT** -Werte, um ausführliche Ursache Bildung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1b356-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="1b356-114">**HRESULT** -Werte werden auch in OLE-Schnittstellenmethoden großem Maß genutzt.</span><span class="sxs-lookup"><span data-stu-id="1b356-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="1b356-115">OLE bietet mehrere Makros für die Konvertierung zwischen **HRESULT** -Werte und **SCODE** -Werte von einer anderen gemeinsamen Datentyp für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="1b356-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1b356-116">In 64-Bit-MAPI ist **HRESULT** noch ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="1b356-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="1b356-117">Informationen über die Verwendung von OLE **HRESULT** -Werte finden Sie unter der *OLE Programmer's Reference* .</span><span class="sxs-lookup"><span data-stu-id="1b356-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="1b356-118">Weitere Informationen zur Verwendung der folgenden Werte in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md) und eine der folgenden Schnittstellenmethoden:</span><span class="sxs-lookup"><span data-stu-id="1b356-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="1b356-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b356-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="1b356-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b356-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="1b356-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b356-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="1b356-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b356-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="1b356-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1b356-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="1b356-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="1b356-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="1b356-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b356-125">See also</span></span>



[<span data-ttu-id="1b356-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="1b356-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="1b356-127">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="1b356-127">MAPI Data Types</span></span>](mapi-data-types.md)


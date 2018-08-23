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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3e46732f9b74b9cdf2dc4c961e7b6b66e3d91d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565228"
---
# <a name="hresult"></a><span data-ttu-id="74525-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="74525-103">HRESULT</span></span>

  
  
<span data-ttu-id="74525-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74525-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74525-105">Ein 32-Bit-Wert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="74525-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="74525-106">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="74525-106">Remarks</span></span>

<span data-ttu-id="74525-107">Der **HRESULT** -Datentyp ist identisch mit der [SCODE](scode.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="74525-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="74525-108">Ein **HRESULT** -Wert besteht aus den folgenden Feldern:</span><span class="sxs-lookup"><span data-stu-id="74525-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="74525-109">Einen Schweregrad 1-Bit-Code, darstellt wobei 0 (null) Erfolg und 1 steht Fehler.</span><span class="sxs-lookup"><span data-stu-id="74525-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="74525-110">Ein reserviertes 4-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="74525-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="74525-111">Ein 11-Bit-Code, der angibt, die Verantwortung für die Fehlermeldung oder einer Warnung, auch bekannt als einen Facility Code.</span><span class="sxs-lookup"><span data-stu-id="74525-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="74525-112">Ein 16-Bit-Code Beschreibung des Fehlers oder eine Warnung ein.</span><span class="sxs-lookup"><span data-stu-id="74525-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="74525-113">Die meisten MAPI-Schnittstellenmethoden und Funktionen zurückgeben **HRESULT** -Werte, um ausführliche Ursache Bildung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="74525-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="74525-114">**HRESULT** -Werte werden auch in OLE-Schnittstellenmethoden großem Maß genutzt.</span><span class="sxs-lookup"><span data-stu-id="74525-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="74525-115">OLE bietet mehrere Makros für die Konvertierung zwischen **HRESULT** -Werte und **SCODE** -Werte von einer anderen gemeinsamen Datentyp für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="74525-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="74525-116">In 64-Bit-MAPI ist **HRESULT** noch ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="74525-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="74525-117">Informationen über die Verwendung von OLE **HRESULT** -Werte finden Sie unter der *OLE Programmer's Reference* .</span><span class="sxs-lookup"><span data-stu-id="74525-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="74525-118">Weitere Informationen zur Verwendung der folgenden Werte in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md) und eine der folgenden Schnittstellenmethoden:</span><span class="sxs-lookup"><span data-stu-id="74525-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="74525-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74525-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="74525-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74525-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="74525-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74525-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="74525-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74525-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="74525-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="74525-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="74525-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="74525-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="74525-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74525-125">See also</span></span>



[<span data-ttu-id="74525-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="74525-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="74525-127">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="74525-127">MAPI Data Types</span></span>](mapi-data-types.md)


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
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435019"
---
# <a name="hresult"></a><span data-ttu-id="10522-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="10522-103">HRESULT</span></span>

  
  
<span data-ttu-id="10522-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10522-105">Ein 32-Bit-Wert, der verwendet wird, um einen Fehler oder eine Warnung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="10522-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="10522-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10522-106">Remarks</span></span>

<span data-ttu-id="10522-107">Der **HRESULT** -Datentyp ist identisch mit dem Datentyp [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="10522-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="10522-108">Ein **HRESULT** -Wert besteht aus den folgenden Feldern:</span><span class="sxs-lookup"><span data-stu-id="10522-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="10522-109">Ein 1-Bit-Code, der den Schweregrad angibt, wobei NULL den Erfolg darstellt und 1 einen Fehler darstellt.</span><span class="sxs-lookup"><span data-stu-id="10522-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="10522-110">Ein reservierter 4-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="10522-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="10522-111">Ein 11-Bit-Code, der die Verantwortlichkeit für den Fehler oder die Warnung angibt, auch als Facility-Code bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10522-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="10522-112">Ein 16-Bit-Code zur Beschreibung des Fehlers oder der Warnung.</span><span class="sxs-lookup"><span data-stu-id="10522-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="10522-113">Die meisten MAPI-Schnittstellenmethoden und-Funktionen geben **HRESULT** -Werte zurück, um eine detaillierte Ursachen Bildung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="10522-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="10522-114">**HRESULT** -Werte werden auch in OLE-Schnittstellenmethoden verwendet.</span><span class="sxs-lookup"><span data-stu-id="10522-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="10522-115">OLE bietet mehrere Makros für die Konvertierung zwischen **HRESULT** -Werten und **SCODE** -Werten, einen weiteren allgemeinen Datentyp für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="10522-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="10522-116">In 64-Bit-MAPI ist **HRESULT** weiterhin ein 32-Bit-Wert.</span><span class="sxs-lookup"><span data-stu-id="10522-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="10522-117">Informationen zur OLE-Verwendung von **HRESULT** -Werten finden Sie unter *OLE Programmer es Reference* .</span><span class="sxs-lookup"><span data-stu-id="10522-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="10522-118">Weitere Informationen zur Verwendung dieser Werte in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md) und einer der folgenden Schnittstellenmethoden:</span><span class="sxs-lookup"><span data-stu-id="10522-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="10522-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="10522-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="10522-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="10522-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="10522-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="10522-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="10522-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="10522-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="10522-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="10522-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="10522-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="10522-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="10522-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10522-125">See also</span></span>



[<span data-ttu-id="10522-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="10522-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="10522-127">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="10522-127">MAPI Data Types</span></span>](mapi-data-types.md)


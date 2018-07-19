---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792503"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="7a243-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="7a243-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="7a243-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a243-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a243-105">Ruft die aktuellen Drucken von Informationen.</span><span class="sxs-lookup"><span data-stu-id="7a243-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="7a243-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a243-106">Parameters</span></span>

 <span data-ttu-id="7a243-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a243-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7a243-108">[in] Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="7a243-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="7a243-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7a243-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7a243-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a243-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7a243-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7a243-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="7a243-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7a243-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7a243-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="7a243-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="7a243-114">[out] Zeiger auf einen Zeiger auf eine Struktur, die die Drucken von Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7a243-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a243-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a243-115">Return value</span></span>

<span data-ttu-id="7a243-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a243-116">S_OK</span></span> 
  
> <span data-ttu-id="7a243-117">Die Drucken von Informationen wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7a243-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a243-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a243-118">Remarks</span></span>

<span data-ttu-id="7a243-119">Formularobjekte Aufrufen die **IMAPIViewContext::GetPrintSetup** -Methode zum Abrufen von Informationen zur Einrichtung Druckers bevor Sie versuchen, die aktuelle Nachricht zu drucken.</span><span class="sxs-lookup"><span data-stu-id="7a243-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a243-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7a243-120">Notes to implementers</span></span>

<span data-ttu-id="7a243-121">Ordnen Sie die **hDevMode-Feld** und **hDevName** Member der Struktur [FORMPRINTSETUP](formprintsetup.md) mithilfe der Win32-Funktion **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="7a243-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a243-122">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7a243-122">Notes to callers</span></span>

<span data-ttu-id="7a243-123">Wenn Sie erwarten, die **hDevMode-Feld dass** und **hDevName** Member der Struktur **FORMPRINTSETUP** auf das durch den Parameter _LppFormPrintSetup_ Unicode-Zeichenfolgen werden, legen Sie _UlFlags_ auf Parameter MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="7a243-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="7a243-124">Andernfalls wird **GetPrintSetup** diese Zeichenfolgen in ANSI-Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a243-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="7a243-125">Freigegeben Sie die **hDevMode-Feld** und **hDevName** Member der Struktur **FORMPRINTSETUP** durch Aufrufen der Win32-Funktion **GlobalFree**werden.</span><span class="sxs-lookup"><span data-stu-id="7a243-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="7a243-126">Freigegeben Sie die gesamte Struktur **FORMPRINTSETUP** durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md)werden.</span><span class="sxs-lookup"><span data-stu-id="7a243-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a243-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a243-127">See also</span></span>



[<span data-ttu-id="7a243-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="7a243-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="7a243-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a243-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


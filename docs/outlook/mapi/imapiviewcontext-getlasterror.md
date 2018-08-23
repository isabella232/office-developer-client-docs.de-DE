---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e373a4abd5e2435d08fc263316ff6ebf650410ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568098"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="ea726-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ea726-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="ea726-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea726-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea726-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftreten Kontext View-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="ea726-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ea726-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea726-106">Parameters</span></span>

 <span data-ttu-id="ea726-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ea726-107">_hResult_</span></span>
  
> <span data-ttu-id="ea726-108">[in] HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="ea726-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="ea726-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ea726-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ea726-110">[in] Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="ea726-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ea726-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ea726-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ea726-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ea726-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ea726-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ea726-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ea726-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ea726-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ea726-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ea726-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ea726-116">[out] Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="ea726-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ea726-117">Dieser Parameter kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea726-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ea726-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ea726-118">Return value</span></span>

<span data-ttu-id="ea726-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea726-119">S_OK</span></span> 
  
> <span data-ttu-id="ea726-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ea726-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ea726-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ea726-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ea726-122">Entweder die Option MAPI_UNICODE festgelegt wurde und **GetLastError** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **GetLastError** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="ea726-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ea726-123">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ea726-123">Remarks</span></span>

<span data-ttu-id="ea726-124">Die **IMAPIViewContext::GetLastError** -Methode stellt Informationen zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ea726-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="ea726-125">Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ea726-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ea726-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ea726-126">Notes to callers</span></span>

<span data-ttu-id="ea726-127">Sie können nutzen Sie die **MAPIERROR** auf die Struktur durch den Parameter _LppMAPIError_ gezeigt, wenn MAPI eine bereitstellt, nur wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ea726-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="ea726-128">In einigen Fällen kann MAPI nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="ea726-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="ea726-129">In diesem Fall wird ein Zeiger auf NULL stattdessen in _LppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea726-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="ea726-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="ea726-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea726-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea726-131">See also</span></span>



[<span data-ttu-id="ea726-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ea726-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ea726-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ea726-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ea726-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea726-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


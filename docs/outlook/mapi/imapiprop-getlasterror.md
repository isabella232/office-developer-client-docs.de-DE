---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792273"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="d3016-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d3016-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="d3016-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3016-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3016-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="d3016-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d3016-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3016-106">Parameters</span></span>

 <span data-ttu-id="d3016-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="d3016-107">_hResult_</span></span>
  
> <span data-ttu-id="d3016-108">[in] Ein Handle für den im vorherigen Methodenaufruf generierten Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d3016-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="d3016-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3016-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d3016-110">[in] Eine Bitmaske aus Flags, die das Format für den Text in der **MAPIERROR** -Struktur, die auf den _LppMAPIError_zurückgegeben angibt.</span><span class="sxs-lookup"><span data-stu-id="d3016-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="d3016-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d3016-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d3016-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d3016-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d3016-113">Die Zeichenfolgen sollte im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d3016-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="d3016-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d3016-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="d3016-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d3016-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d3016-116">[out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="d3016-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d3016-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn keine Fehler Informationen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d3016-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d3016-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d3016-118">Return value</span></span>

<span data-ttu-id="d3016-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3016-119">S_OK</span></span> 
  
> <span data-ttu-id="d3016-120">Die Fehlerinformationen wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3016-120">The error information was returned.</span></span>
    
<span data-ttu-id="d3016-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d3016-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d3016-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="d3016-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3016-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3016-123">Remarks</span></span>

<span data-ttu-id="d3016-124">Die **IMAPIProp::GetLastError** -Methode stellt Informationen zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d3016-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="d3016-125">Clients können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d3016-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="d3016-126">Alle Implementierungen der **GetLastError** von MAPI bereitgestellt sind ANSI Implementierungen, mit Ausnahme der [IAddrBook](iaddrbookimapiprop.md) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="d3016-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="d3016-127">Die enthaltene **IAddrBook** **GetLastError** -Methode unterstützt Unicode.</span><span class="sxs-lookup"><span data-stu-id="d3016-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d3016-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d3016-128">Notes to implementers</span></span>

<span data-ttu-id="d3016-129">Die Details eines Remote-transport-Implementierung dieser Methode und worauf Nachrichten von die dieser Methode zurückgegebenen bis zu der Adressbuchhierarchie des Anbieters, da die bestimmten fehlerbedingungen, die zu verschiedenen HRESULT-Werte für verschiedene Transport abweichen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d3016-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d3016-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d3016-130">Notes to callers</span></span>

<span data-ttu-id="d3016-131">Sie können die **MAPIERROR** -Struktur auf durch den Parameter _LppMAPIError_ zeigt, wenn **GetLastError** bereitstellt, nur, wenn S_OK zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3016-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="d3016-132">In einigen Fällen kann **GetLastError** nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="d3016-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="d3016-133">In diesem Fall wird ein Zeiger auf NULL stattdessen in _LppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3016-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="d3016-134">Um den Speicher für die Struktur **MAPIERROR** freizugeben, rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d3016-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="d3016-135">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d3016-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3016-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3016-136">See also</span></span>



[<span data-ttu-id="d3016-137">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d3016-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="d3016-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d3016-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d3016-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d3016-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d3016-140">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3016-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="d3016-141">Fehler Extended MAPI</span><span class="sxs-lookup"><span data-stu-id="d3016-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)


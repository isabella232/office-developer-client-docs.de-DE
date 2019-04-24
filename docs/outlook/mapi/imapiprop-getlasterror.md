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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342049"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="80530-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="80530-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="80530-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80530-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="80530-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="80530-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80530-106">Parameters</span></span>

 <span data-ttu-id="80530-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="80530-107">_hResult_</span></span>
  
> <span data-ttu-id="80530-108">in Ein Handle für den im vorherigen Methodenaufruf generierten Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="80530-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="80530-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80530-109">_ulFlags_</span></span>
  
> <span data-ttu-id="80530-110">in Eine Bitmaske von Flags, die das Format für den Text angibt, der in der **MAPIERROR** -Struktur zurückgegeben wird, auf die durch _lppMAPIError_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="80530-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="80530-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="80530-111">The following flag can be set:</span></span>
    
<span data-ttu-id="80530-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80530-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="80530-113">Die Zeichenfolgen sollten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="80530-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="80530-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format sein.</span><span class="sxs-lookup"><span data-stu-id="80530-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="80530-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="80530-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="80530-116">Out Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Versions-, Komponenten-und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="80530-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="80530-117">Der Parameter _lppMAPIError_ kann auf NULL festgelegt werden, wenn keine Fehlerinformationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80530-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="80530-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80530-118">Return value</span></span>

<span data-ttu-id="80530-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="80530-119">S_OK</span></span> 
  
> <span data-ttu-id="80530-120">Die Fehlerinformationen wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80530-120">The error information was returned.</span></span>
    
<span data-ttu-id="80530-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="80530-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="80530-122">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="80530-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80530-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80530-123">Remarks</span></span>

<span data-ttu-id="80530-124">Die **IMAPIProp:: getlasterroraufzurufen** -Methode liefert Informationen zu einem vorherigen Methodenaufruf, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="80530-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="80530-125">Clients können Ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem Sie die Daten aus der **MAPIERROR** -Struktur in ein Dialogfeld einschließen.</span><span class="sxs-lookup"><span data-stu-id="80530-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="80530-126">Alle von MAPI bereitgestellten Implementierungen von **getlasterroraufzurufen** sind ANSI-Implementierungen, mit Ausnahme der [IAddrBook](iaddrbookimapiprop.md) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="80530-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="80530-127">Die **getlasterroraufzurufen** -Methode, die in **IAddrBook** enthalten ist, unterstützt Unicode.</span><span class="sxs-lookup"><span data-stu-id="80530-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="80530-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="80530-128">Notes to implementers</span></span>

<span data-ttu-id="80530-129">Die Details der Implementierung der Methode eines Remote Transportanbieters und der von dieser Methode zurückgegebenen Nachrichten sind für den Transportanbieter, da die besonderen Fehlerbedingungen, die zu verschiedenen HRESULT-Werten führen, für unterschiedliche Transportvorgänge unterschiedlich sind. Anbieter.</span><span class="sxs-lookup"><span data-stu-id="80530-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="80530-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="80530-130">Notes to callers</span></span>

<span data-ttu-id="80530-131">Sie können die **MAPIERROR** -Struktur, auf die durch den _lppMAPIError_ -Parameter verwiesen wird, verwenden, wenn **getlasterroraufzurufen** eine bereitstellt, nur, wenn der Rückgabewert S_OK ist.</span><span class="sxs-lookup"><span data-stu-id="80530-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="80530-132">Manchmal kann **getlasterroraufzurufen** nicht ermitteln, was der letzte Fehler war oder nicht mehr über den Fehler berichtet.</span><span class="sxs-lookup"><span data-stu-id="80530-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="80530-133">In dieser Situation wird stattdessen ein Zeiger auf NULL in _lppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80530-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="80530-134">Zum Freigeben des Speichers für die **MAPIERROR** -Struktur rufen Sie die [Mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="80530-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="80530-135">Weitere Informationen zur **getlasterroraufzurufen** -Methode finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="80530-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80530-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80530-136">See also</span></span>



[<span data-ttu-id="80530-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="80530-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="80530-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="80530-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="80530-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="80530-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="80530-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80530-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="80530-141">Erweiterte MAPI-Fehler</span><span class="sxs-lookup"><span data-stu-id="80530-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)


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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435831"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="9baf1-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9baf1-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="9baf1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9baf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9baf1-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="9baf1-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="9baf1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9baf1-106">Parameters</span></span>

 <span data-ttu-id="9baf1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9baf1-107">_hResult_</span></span>
  
> <span data-ttu-id="9baf1-108">[in] Ein Handle für den Fehlercode, der im vorherigen Methodenaufruf generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9baf1-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="9baf1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9baf1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9baf1-110">[in] Eine Bitmaske mit Flags, die das Format für den in der **MAPIERROR-Struktur** zurückgegebenen Text angibt, auf den _lppMAPIError zeigt._</span><span class="sxs-lookup"><span data-stu-id="9baf1-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="9baf1-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9baf1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9baf1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9baf1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9baf1-113">Die Zeichenfolgen sollten im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="9baf1-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="9baf1-114">Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="9baf1-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="9baf1-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9baf1-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="9baf1-116">[out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="9baf1-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="9baf1-117">Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine Fehlerinformationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9baf1-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9baf1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9baf1-118">Return value</span></span>

<span data-ttu-id="9baf1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9baf1-119">S_OK</span></span> 
  
> <span data-ttu-id="9baf1-120">Die Fehlerinformationen wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9baf1-120">The error information was returned.</span></span>
    
<span data-ttu-id="9baf1-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9baf1-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9baf1-122">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="9baf1-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9baf1-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9baf1-123">Remarks</span></span>

<span data-ttu-id="9baf1-124">Die **IMAPIProp::GetLastError-Methode** stellt Informationen zu einem vorherigen Methodenaufruf zur Verfügung, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="9baf1-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="9baf1-125">Clients können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="9baf1-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="9baf1-126">Alle von MAPI bereitgestellten Implementierungen von **GetLastError** sind ANSI-Implementierungen, mit Ausnahme der [IAddrBook-Implementierung.](iaddrbookimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="9baf1-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="9baf1-127">Die **getLastError-Methode,** die in **IAddrBook enthalten** ist, unterstützt Unicode.</span><span class="sxs-lookup"><span data-stu-id="9baf1-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9baf1-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9baf1-128">Notes to implementers</span></span>

<span data-ttu-id="9baf1-129">Die Details der Implementierung dieser Methode durch einen Remote-Transport-Anbieter und die von dieser Methode zurückgegebenen Nachrichten liegen beim Transportanbieter, da die besonderen Fehlerbedingungen, die zu verschiedenen HRESULT-Werten führen, für unterschiedliche Transportanbieter unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="9baf1-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9baf1-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9baf1-130">Notes to callers</span></span>

<span data-ttu-id="9baf1-131">Sie können die **MAPIERROR-Struktur** verwenden, auf die der  _lppMAPIError-Parameter_ verweist, wenn **GetLastError** einen Parameter anriert, nur wenn der Rückgabewert S_OK.</span><span class="sxs-lookup"><span data-stu-id="9baf1-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="9baf1-132">Manchmal **kann GetLastError** nicht bestimmen, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="9baf1-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="9baf1-133">In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9baf1-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="9baf1-134">Um den Arbeitsspeicher für die **MAPIERROR-Struktur frei** zu geben, rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf.</span><span class="sxs-lookup"><span data-stu-id="9baf1-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="9baf1-135">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="9baf1-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9baf1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9baf1-136">See also</span></span>



[<span data-ttu-id="9baf1-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9baf1-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="9baf1-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="9baf1-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="9baf1-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9baf1-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9baf1-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9baf1-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="9baf1-141">ERWEITERTE MAPI-Fehler</span><span class="sxs-lookup"><span data-stu-id="9baf1-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)


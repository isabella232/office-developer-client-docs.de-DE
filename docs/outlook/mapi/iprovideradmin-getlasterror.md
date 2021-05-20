---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439849"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="fd2bf-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fd2bf-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="fd2bf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd2bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd2bf-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Anbieterverwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="fd2bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd2bf-106">Parameters</span></span>

 <span data-ttu-id="fd2bf-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="fd2bf-107">_hResult_</span></span>
  
> <span data-ttu-id="fd2bf-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="fd2bf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd2bf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fd2bf-110">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="fd2bf-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fd2bf-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fd2bf-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd2bf-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fd2bf-113">Die Zeichenfolgen im **MAPIERROR,die** im  _lppMAPIError-Parameter_ zurückgegeben werden, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="fd2bf-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="fd2bf-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="fd2bf-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="fd2bf-116">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="fd2bf-117">Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn **kein MAPIERROR zurückgegeben** werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fd2bf-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd2bf-118">Return value</span></span>

<span data-ttu-id="fd2bf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd2bf-119">S_OK</span></span> 
  
> <span data-ttu-id="fd2bf-120">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="fd2bf-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fd2bf-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fd2bf-122">Entweder wurde das MAPI_UNICODE festgelegt, **und GetLastError** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, **und GetLastError** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fd2bf-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd2bf-123">Remarks</span></span>

<span data-ttu-id="fd2bf-124">Die **IProviderAdmin::GetLastError-Methode** stellt Informationen zu einem vorherigen Methodenaufruf zur Verfügung, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="fd2bf-125">Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fd2bf-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="fd2bf-126">Notes to callers</span></span>

<span data-ttu-id="fd2bf-127">Sie können die **MAPIERROR-Struktur** verwenden, wenn MAPI eine angibt, auf die der  _lppMAPIError-Parameter_ nur verweist, wenn **GetLastError** eine S_OK.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="fd2bf-128">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="fd2bf-129">In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd2bf-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="fd2bf-130">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="fd2bf-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd2bf-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd2bf-131">See also</span></span>



[<span data-ttu-id="fd2bf-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="fd2bf-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="fd2bf-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fd2bf-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fd2bf-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd2bf-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 250074b28b98269df58fecfcb2d178f73e26c571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792749"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="b08d8-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b08d8-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="b08d8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b08d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b08d8-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält, die auf ein Profil Administration-Objekt aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="b08d8-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b08d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b08d8-106">Parameters</span></span>

 <span data-ttu-id="b08d8-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b08d8-107">_hResult_</span></span>
  
> <span data-ttu-id="b08d8-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="b08d8-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="b08d8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b08d8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b08d8-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="b08d8-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b08d8-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b08d8-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b08d8-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b08d8-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b08d8-113">Die Zeichenfolgen in der [MAPIERROR](mapierror.md) -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b08d8-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b08d8-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b08d8-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b08d8-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b08d8-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b08d8-116">[out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="b08d8-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b08d8-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b08d8-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b08d8-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b08d8-118">Return value</span></span>

<span data-ttu-id="b08d8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b08d8-119">S_OK</span></span> 
  
> <span data-ttu-id="b08d8-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b08d8-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b08d8-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b08d8-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b08d8-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="b08d8-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b08d8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b08d8-123">Remarks</span></span>

<span data-ttu-id="b08d8-124">Die **IProfAdmin::GetLastError** -Methode ruft Informationen über den letzten Fehler, die von einem Methodenaufruf für das Profil Administration-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b08d8-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b08d8-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b08d8-125">Notes to callers</span></span>

<span data-ttu-id="b08d8-126">Die Struktur **MAPIERROR** können MAPI, bereitstellt, auf die die _LppMAPIError_ Parameter nur, wenn **GetLastError** S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b08d8-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b08d8-127">In einigen Fällen kann MAPI nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="b08d8-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b08d8-128">In diesem Fall wird ein Zeiger auf NULL in _LppMAPIError_zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b08d8-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="b08d8-129">Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um alle durch Arbeitsspeicher MAPI für die Struktur **MAPIERROR** freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b08d8-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b08d8-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Erweiterte Fehler verwenden](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b08d8-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b08d8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b08d8-131">See also</span></span>



[<span data-ttu-id="b08d8-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b08d8-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b08d8-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b08d8-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b08d8-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b08d8-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


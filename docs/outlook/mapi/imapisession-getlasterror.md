---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792304"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="15695-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="15695-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="15695-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15695-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15695-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Sitzungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="15695-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="15695-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15695-106">Parameters</span></span>

 <span data-ttu-id="15695-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="15695-107">_hResult_</span></span>
  
> <span data-ttu-id="15695-108">[in] Ein Handle für den Fehlerwert in der vorherigen Aufruf-Methode generiert.</span><span class="sxs-lookup"><span data-stu-id="15695-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="15695-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15695-109">_ulFlags_</span></span>
  
> <span data-ttu-id="15695-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="15695-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="15695-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="15695-111">The following flag can be set:</span></span>
    
<span data-ttu-id="15695-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15695-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="15695-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="15695-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="15695-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="15695-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="15695-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="15695-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="15695-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="15695-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="15695-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn MAPI entsprechenden Informationen für eine **MAPIERROR** Struktur angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="15695-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15695-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="15695-118">Return value</span></span>

<span data-ttu-id="15695-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="15695-119">S_OK</span></span> 
  
> <span data-ttu-id="15695-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="15695-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="15695-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="15695-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="15695-122">Die Option MAPI_UNICODE wurde festgelegt, und die Sitzung Unicode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15695-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15695-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15695-123">Remarks</span></span>

<span data-ttu-id="15695-124">Die **IMAPISession::GetLastError** -Methode ruft Informationen über den letzten Fehler, der durch einen Aufruf der Methode **IMAPISession** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="15695-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="15695-125">Clients können die Benutzer mit ausführlichen Informationen zu dem Fehler bereitstellen, indem Sie diese Informationen in einem Dialogfeld einschließlich.</span><span class="sxs-lookup"><span data-stu-id="15695-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="15695-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="15695-126">Notes to callers</span></span>

<span data-ttu-id="15695-127">Die Struktur **MAPIERROR** können MAPI, bereitstellt, auf die die _LppMAPIError_ Parameter nur, wenn **GetLastError** S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15695-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="15695-128">In einigen Fällen kann nicht MAPI was letzten Fehler erkennen, oder es wurde keine weiteren zu dem Fehler melden.</span><span class="sxs-lookup"><span data-stu-id="15695-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="15695-129">In diesem Fall gibt **GetLastError** einen Zeiger auf NULL in _LppMAPIError_ stattdessen.</span><span class="sxs-lookup"><span data-stu-id="15695-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="15695-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="15695-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15695-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15695-131">See also</span></span>



[<span data-ttu-id="15695-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="15695-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="15695-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="15695-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="15695-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="15695-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="15695-135">Fehler Extended MAPI</span><span class="sxs-lookup"><span data-stu-id="15695-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)


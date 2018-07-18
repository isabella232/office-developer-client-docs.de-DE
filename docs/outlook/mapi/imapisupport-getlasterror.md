---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2a20f0f48eebe2194bc92afb98a620f9b39bb88d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792358"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="c291d-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c291d-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="c291d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c291d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c291d-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Support-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="c291d-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c291d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c291d-106">Parameters</span></span>

 <span data-ttu-id="c291d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c291d-107">_hResult_</span></span>
  
> <span data-ttu-id="c291d-108">[in] Ein Handle für den Fehlerwert generiert, die in der vorherigen Aufruf-Methode für das Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c291d-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="c291d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c291d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c291d-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="c291d-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c291d-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c291d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c291d-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c291d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c291d-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c291d-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c291d-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c291d-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c291d-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c291d-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c291d-116">[out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="c291d-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="c291d-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn eine **MAPIERROR** -Struktur mit den entsprechenden Fehlerinformationen bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c291d-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c291d-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c291d-118">Return value</span></span>

<span data-ttu-id="c291d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c291d-119">S_OK</span></span> 
  
> <span data-ttu-id="c291d-120">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c291d-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="c291d-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c291d-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c291d-122">Entweder die Option MAPI_UNICODE festgelegt wurde und MAPI unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und MAPI unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c291d-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c291d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c291d-123">Remarks</span></span>

<span data-ttu-id="c291d-124">Die **IMAPISupport::GetLastError** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="c291d-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="c291d-125">Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c291d-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c291d-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c291d-126">Notes to callers</span></span>

<span data-ttu-id="c291d-127">Sie können den Zeiger auf die Struktur **MAPIERROR** verwenden, wenn MAPI eine in der _LppMAPIError_ -Parameter stellt nur, wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="c291d-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="c291d-128">Manchmal MAPI kann nicht bestimmen, welche letzten Fehlers wurde oder es wurde keine weiteren Bericht zu dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="c291d-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="c291d-129">In diesem Fall gibt _LppMAPIError_ einen Zeiger stattdessen auf NULL.</span><span class="sxs-lookup"><span data-stu-id="c291d-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="c291d-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c291d-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="c291d-131">Um alle durch MAPI Arbeitsspeicher freizugeben, rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion für die zurückgegebene **MAPIERROR** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c291d-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c291d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c291d-132">See also</span></span>



[<span data-ttu-id="c291d-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c291d-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c291d-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c291d-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c291d-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c291d-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="c291d-136">Fehler Extended MAPI</span><span class="sxs-lookup"><span data-stu-id="c291d-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)


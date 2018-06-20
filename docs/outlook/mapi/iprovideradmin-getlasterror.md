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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f00418efa068ea81fab94605cbdfd139e24bb4a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792772"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="2d20a-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2d20a-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="2d20a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d20a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d20a-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält, die für den Anbieter Verwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2d20a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2d20a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d20a-106">Parameters</span></span>

 <span data-ttu-id="2d20a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2d20a-107">_hResult_</span></span>
  
> <span data-ttu-id="2d20a-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="2d20a-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="2d20a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d20a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2d20a-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="2d20a-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2d20a-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2d20a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2d20a-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2d20a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2d20a-113">Die Zeichenfolgen in der **MAPIERROR** zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="2d20a-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="2d20a-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="2d20a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2d20a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2d20a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2d20a-116">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="2d20a-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2d20a-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR ist** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d20a-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2d20a-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2d20a-118">Return value</span></span>

<span data-ttu-id="2d20a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d20a-119">S_OK</span></span> 
  
> <span data-ttu-id="2d20a-120">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d20a-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="2d20a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2d20a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2d20a-122">Entweder die Option MAPI_UNICODE festgelegt wurde und **GetLastError** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **GetLastError** nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d20a-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2d20a-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d20a-123">Remarks</span></span>

<span data-ttu-id="2d20a-124">Die **IProviderAdmin::GetLastError** -Methode stellt Informationen zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2d20a-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="2d20a-125">Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2d20a-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d20a-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="2d20a-126">Notes to callers</span></span>

<span data-ttu-id="2d20a-127">Der Struktur **MAPIERROR** können, wenn MAPI, bereitstellt, dass der Parameter _LppMAPIError_ auf zeigt nur, wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2d20a-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="2d20a-128">In einigen Fällen kann MAPI nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="2d20a-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2d20a-129">In diesem Fall wird ein Zeiger auf NULL stattdessen in _LppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d20a-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="2d20a-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Erweiterte Fehler verwenden](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2d20a-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d20a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d20a-131">See also</span></span>



[<span data-ttu-id="2d20a-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2d20a-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2d20a-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2d20a-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2d20a-134">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d20a-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


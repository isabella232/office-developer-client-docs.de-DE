---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9906cb9510716b3be11a1b8bcf12f06e73789445
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792166"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="b43b0-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b43b0-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="b43b0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b43b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b43b0-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, auf das Formular Factory-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="b43b0-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b43b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b43b0-106">Parameters</span></span>

 <span data-ttu-id="b43b0-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b43b0-107">_hResult_</span></span>
  
> <span data-ttu-id="b43b0-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="b43b0-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="b43b0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b43b0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b43b0-110">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="b43b0-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b43b0-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b43b0-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="b43b0-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b43b0-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b43b0-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="b43b0-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b43b0-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="b43b0-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b43b0-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b43b0-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b43b0-116">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="b43b0-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b43b0-117">Dieser Parameter kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b43b0-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b43b0-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b43b0-118">Return value</span></span>

<span data-ttu-id="b43b0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b43b0-119">S_OK</span></span> 
  
> <span data-ttu-id="b43b0-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b43b0-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b43b0-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b43b0-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b43b0-122">Entweder die Option MAPI_UNICODE festgelegt wurde und **GetLastError** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **GetLastError** nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b43b0-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b43b0-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b43b0-123">Remarks</span></span>

<span data-ttu-id="b43b0-124">Die **IMAPIFormFactory::GetLastError** -Methode stellt Informationen zu einem Aufruf der vorherigen-Methode, die nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b43b0-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="b43b0-125">Anrufer können die Benutzer einschließlich der Daten aus der **MAPIERROR** -Struktur in einem Dialogfeld mit ausführlichen Informationen zu dem Fehler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b43b0-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b43b0-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b43b0-126">Notes to callers</span></span>

<span data-ttu-id="b43b0-127">Sie können nutzen Sie die **MAPIERROR** auf die Struktur durch den Parameter _LppMAPIError_ gezeigt, wenn MAPI eine bereitstellt, nur wenn **GetLastError** gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b43b0-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b43b0-128">In einigen Fällen kann MAPI nicht ermitteln, was letzten Fehlers wurde oder nicht mehr zu dem Fehler gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="b43b0-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b43b0-129">In diesem Fall wird ein Zeiger auf NULL stattdessen in _LppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b43b0-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="b43b0-130">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Erweiterte Fehler verwenden](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b43b0-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b43b0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b43b0-131">See also</span></span>



[<span data-ttu-id="b43b0-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b43b0-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b43b0-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b43b0-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b43b0-134">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b43b0-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)


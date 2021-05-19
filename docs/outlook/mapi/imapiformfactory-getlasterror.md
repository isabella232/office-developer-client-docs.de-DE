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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417007"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="00022-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="00022-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="00022-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00022-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00022-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Form Factory-Objekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="00022-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="00022-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00022-106">Parameters</span></span>

 <span data-ttu-id="00022-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="00022-107">_hResult_</span></span>
  
> <span data-ttu-id="00022-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="00022-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="00022-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00022-109">_ulFlags_</span></span>
  
> <span data-ttu-id="00022-110">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="00022-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="00022-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="00022-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="00022-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00022-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="00022-113">Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="00022-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="00022-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="00022-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="00022-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="00022-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="00022-116">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="00022-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="00022-117">Dieser Parameter kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="00022-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00022-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00022-118">Return value</span></span>

<span data-ttu-id="00022-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="00022-119">S_OK</span></span> 
  
> <span data-ttu-id="00022-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="00022-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="00022-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="00022-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="00022-122">Entweder wurde das MAPI_UNICODE festgelegt, **und GetLastError** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, **und GetLastError** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="00022-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00022-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00022-123">Remarks</span></span>

<span data-ttu-id="00022-124">Die **IMAPIFormFactory::GetLastError-Methode** stellt Informationen zu einem vorherigen Methodenaufruf zur Verfügung, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="00022-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="00022-125">Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld eingeben.</span><span class="sxs-lookup"><span data-stu-id="00022-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00022-126">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="00022-126">Notes to callers</span></span>

<span data-ttu-id="00022-127">Sie können die **MAPIERROR-Struktur** verwenden, auf die der  _lppMAPIError-Parameter_ verweist, wenn MAPI nur dann einen angibt, wenn **GetLastError** S_OK.</span><span class="sxs-lookup"><span data-stu-id="00022-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="00022-128">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="00022-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="00022-129">In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00022-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="00022-130">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="00022-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00022-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00022-131">See also</span></span>



[<span data-ttu-id="00022-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="00022-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="00022-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00022-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00022-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00022-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)


---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421151"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="89987-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="89987-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="89987-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89987-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89987-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Steuerelementfehler der Schaltfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="89987-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="89987-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89987-106">Parameters</span></span>

 <span data-ttu-id="89987-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="89987-107">_hResult_</span></span>
  
> <span data-ttu-id="89987-108">[in] Ein Handle zum Fehlerwert, der im vorherigen Methodenaufruf generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="89987-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="89987-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89987-109">_ulFlags_</span></span>
  
> <span data-ttu-id="89987-110">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="89987-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="89987-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="89987-111">The following flag can be set:</span></span>
    
<span data-ttu-id="89987-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89987-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="89987-113">Die Zeichenfolgen in der **MAPIERROR-Struktur,** die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="89987-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="89987-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="89987-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="89987-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="89987-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="89987-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="89987-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="89987-117">Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn der Anbieter keine **MAPIERROR-Struktur** mit entsprechenden Informationen angeben kann.</span><span class="sxs-lookup"><span data-stu-id="89987-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89987-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89987-118">Return value</span></span>

<span data-ttu-id="89987-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="89987-119">S_OK</span></span> 
  
> <span data-ttu-id="89987-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="89987-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="89987-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89987-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89987-122">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="89987-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89987-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89987-123">Remarks</span></span>

<span data-ttu-id="89987-124">Dienstanbieter implementieren die **IMAPIControl::GetLastError-Methode,** um Informationen zu einem vorherigen Methodenaufruf zu liefern, der fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="89987-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="89987-125">MAPI kann Benutzern detaillierte Informationen zu dem Fehler geben, indem die Daten aus der **MAPIERROR-Struktur** in einer Nachricht oder einem Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89987-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="89987-126">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="89987-126">Notes to implementers</span></span>

<span data-ttu-id="89987-127">Sie benötigen nicht für jeden Fehler Informationen, die in die **MAPIERROR-Struktur** enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="89987-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="89987-128">Es ist möglicherweise nicht möglich, den vorherigen Fehler zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="89987-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="89987-129">Wenn Sie über Informationen verfügen, geben S_OK und die entsprechenden Daten in der **MAPIERROR-Struktur** zurück.</span><span class="sxs-lookup"><span data-stu-id="89987-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="89987-130">Wenn keine Informationen verfügbar sind, geben Sie S_OK und einen Zeiger auf NULL für den  _lppMAPIError-Parameter_ zurück.</span><span class="sxs-lookup"><span data-stu-id="89987-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="89987-131">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="89987-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89987-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89987-132">See also</span></span>



[<span data-ttu-id="89987-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="89987-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="89987-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="89987-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="89987-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89987-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)


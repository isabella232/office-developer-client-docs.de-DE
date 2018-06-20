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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2be5e40de6894b99d9de86423e99dd95a08bc04c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792066"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="fb652-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fb652-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="fb652-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb652-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb652-105">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Schaltfläche-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="fb652-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="fb652-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb652-106">Parameters</span></span>

 <span data-ttu-id="fb652-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="fb652-107">_hResult_</span></span>
  
> <span data-ttu-id="fb652-108">[in] Ein Handle für den Fehlerwert in der vorherigen Aufruf-Methode generiert.</span><span class="sxs-lookup"><span data-stu-id="fb652-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="fb652-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fb652-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fb652-110">[in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgen steuert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb652-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="fb652-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fb652-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fb652-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb652-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fb652-113">Die Zeichenfolgen in der **MAPIERROR** -Struktur zurückgegeben, die im Parameter _LppMAPIError_ sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fb652-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="fb652-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fb652-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="fb652-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="fb652-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="fb652-116">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="fb652-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="fb652-117">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn der Anbieter eine **MAPIERROR** -Struktur mit den entsprechenden Informationen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb652-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fb652-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fb652-118">Return value</span></span>

<span data-ttu-id="fb652-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb652-119">S_OK</span></span> 
  
> <span data-ttu-id="fb652-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fb652-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fb652-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fb652-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fb652-122">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="fb652-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb652-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb652-123">Remarks</span></span>

<span data-ttu-id="fb652-124">Dienstanbieter implementieren die **IMAPIControl::GetLastError** -Methode, um Informationen zu einem vorherigen Methodenaufruf angeben, die nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fb652-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="fb652-125">MAPI erhalten Benutzer detaillierte Informationen zu dem Fehler durch die Daten aus der **MAPIERROR** -Struktur in einer Nachricht oder Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb652-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fb652-126">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="fb652-126">Notes to implementers</span></span>

<span data-ttu-id="fb652-127">Sie müssen nicht die Informationen in der Struktur **MAPIERROR** für alle Fehler eingeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="fb652-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="fb652-128">Es möglicherweise nicht möglich, zu bestimmen, welche vorherigen Fehler.</span><span class="sxs-lookup"><span data-stu-id="fb652-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="fb652-129">Wenn Sie Informationen, kehren Sie S_OK und die entsprechenden Daten in der Struktur **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="fb652-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="fb652-130">Wenn keine Informationen verfügbar sind, werden S_OK und einen Zeiger auf NULL für den Parameter _LppMAPIError_ zurück.</span><span class="sxs-lookup"><span data-stu-id="fb652-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="fb652-131">Weitere Informationen über die **GetLastError** -Methode finden Sie unter [Extended MAPI-Fehler](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="fb652-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb652-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb652-132">See also</span></span>



[<span data-ttu-id="fb652-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="fb652-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="fb652-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fb652-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fb652-135">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb652-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

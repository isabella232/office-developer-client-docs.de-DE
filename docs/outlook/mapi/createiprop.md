---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406808"
---
# <a name="createiprop"></a><span data-ttu-id="d0412-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="d0412-103">CreateIProp</span></span>

  
  
<span data-ttu-id="d0412-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0412-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0412-105">Erstellt ein Eigenschaftsdatenobjekt, d. h. ein [IPropData-Objekt.](ipropdataimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d0412-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0412-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d0412-106">Header file:</span></span>  <br/> |<span data-ttu-id="d0412-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d0412-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d0412-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d0412-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0412-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d0412-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d0412-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d0412-110">Called by:</span></span>  <br/> |<span data-ttu-id="d0412-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d0412-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a><span data-ttu-id="d0412-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0412-112">Parameters</span></span>

 <span data-ttu-id="d0412-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d0412-113">_lpInterface_</span></span>
  
> <span data-ttu-id="d0412-114">[in] Zeiger auf einen Schnittstellenbezeichner (Interface Identifier, IID) für das Eigenschaftsdatenobjekt.</span><span class="sxs-lookup"><span data-stu-id="d0412-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="d0412-115">Der gültige Schnittstellenbezeichner wird IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="d0412-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="d0412-116">Das Übergeben von NULL im  _lpInterface-Parameter_ bewirkt auch, dass das im  _lppPropData-Parameter_ zurückgegebene Eigenschaftsdatenobjekt in die Standardschnittstelle für ein Eigenschaftsdatenobjekt übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="d0412-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="d0412-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d0412-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d0412-118">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0412-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d0412-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d0412-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d0412-120">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0412-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="d0412-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d0412-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d0412-122">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0412-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d0412-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="d0412-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="d0412-124">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="d0412-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="d0412-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="d0412-125">_lppPropData_</span></span>
  
> <span data-ttu-id="d0412-126">[out] Zeiger auf einen Zeiger auf das zurückgegebene Eigenschaftsdatenobjekt.</span><span class="sxs-lookup"><span data-stu-id="d0412-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0412-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0412-127">Return value</span></span>

<span data-ttu-id="d0412-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0412-128">S_OK</span></span> 
  
> <span data-ttu-id="d0412-129">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d0412-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d0412-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="d0412-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="d0412-131">Die angeforderte Schnittstelle wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0412-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0412-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0412-132">Remarks</span></span>

<span data-ttu-id="d0412-133">Die _Eingabeparameter lpAllocateBuffer,_ _lpAllocateMore_ und _lpFreeBuffer_ verweisen auf die [Funktionen MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d0412-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="d0412-134">Eine Clientanwendung, die **CreateIProp** aufruft, übergibt Zeiger an die einfach benannten #A0 . Ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er in seinem Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines-Methode](imapisupport-getmemallocroutines.md) abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="d0412-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  


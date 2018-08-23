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
ms.openlocfilehash: 8d6eb011e65ad44f4183eb5821697dcf2508032c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566880"
---
# <a name="createiprop"></a><span data-ttu-id="284be-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="284be-103">CreateIProp</span></span>

  
  
<span data-ttu-id="284be-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="284be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="284be-105">Erstellt eine Eigenschaft Datenobjekt, d. h., ein [IPropData](ipropdataimapiprop.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="284be-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="284be-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="284be-106">Header file:</span></span>  <br/> |<span data-ttu-id="284be-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="284be-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="284be-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="284be-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="284be-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="284be-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="284be-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="284be-110">Called by:</span></span>  <br/> |<span data-ttu-id="284be-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="284be-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="284be-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="284be-112">Parameters</span></span>

 <span data-ttu-id="284be-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="284be-113">_lpInterface_</span></span>
  
> <span data-ttu-id="284be-114">[in] Zeiger auf eine Schnittstellenbezeichner (IID) für die Daten Property-Objekt.</span><span class="sxs-lookup"><span data-stu-id="284be-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="284be-115">Der Bezeichner gültige Schnittstelle ist IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="284be-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="284be-116">Übergeben NULL im _LpInterface_ -Parameter wird auch das Eigenschaftenobjekt-Daten, die in der _LppPropData_ -Parameter in der standard-Benutzeroberfläche für ein Property-Datenobjekt umgewandelt werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="284be-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="284be-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="284be-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="284be-118">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="284be-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="284be-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="284be-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="284be-120">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="284be-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="284be-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="284be-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="284be-122">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="284be-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="284be-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="284be-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="284be-124">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="284be-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="284be-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="284be-125">_lppPropData_</span></span>
  
> <span data-ttu-id="284be-126">[out] Zeiger auf einen Zeiger auf das zurückgegebene Daten Eigenschaftenobjekt.</span><span class="sxs-lookup"><span data-stu-id="284be-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="284be-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="284be-127">Return value</span></span>

<span data-ttu-id="284be-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="284be-128">S_OK</span></span> 
  
> <span data-ttu-id="284be-129">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="284be-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="284be-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="284be-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="284be-131">Die angeforderte Schnittstelle wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="284be-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="284be-132">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="284be-132">Remarks</span></span>

<span data-ttu-id="284be-133">Die Eingabeparametern _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ zeigen die [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="284be-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="284be-134">Eine Clientanwendung Aufrufen **CreateIProp** übergibt Zeiger auf die MAPI-Funktionen, die nur mit dem Namen; Ein Dienstanbieter übergibt die Zeiger auf diese Funktionen, die es in seinem Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="284be-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  


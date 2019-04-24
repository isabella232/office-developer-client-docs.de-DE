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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333033"
---
# <a name="createiprop"></a><span data-ttu-id="c53c4-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="c53c4-103">CreateIProp</span></span>

  
  
<span data-ttu-id="c53c4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c53c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c53c4-105">Erstellt ein Property-Datenobjekt, also ein [IPropData](ipropdataimapiprop.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c53c4-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c53c4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c53c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="c53c4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="c53c4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c53c4-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c53c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c53c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c53c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c53c4-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c53c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="c53c4-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c53c4-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c53c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c53c4-112">Parameters</span></span>

 <span data-ttu-id="c53c4-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c53c4-113">_lpInterface_</span></span>
  
> <span data-ttu-id="c53c4-114">in Zeiger auf einen Schnittstellenbezeichner (IID) für das Eigenschaftendaten Objekt.</span><span class="sxs-lookup"><span data-stu-id="c53c4-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="c53c4-115">Der gültige Schnittstellenbezeichner ist IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="c53c4-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="c53c4-116">Das übergeben von NULL im _lpInterface_ -Parameter bewirkt außerdem, dass das im _lppPropData_ -Parameter zurückgegebene Property-Datenobjekt in die Standardschnittstelle für ein Datenobjekt der Eigenschaft umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="c53c4-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="c53c4-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c53c4-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c53c4-118">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c53c4-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c53c4-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="c53c4-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="c53c4-120">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c53c4-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="c53c4-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="c53c4-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c53c4-122">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c53c4-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c53c4-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="c53c4-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="c53c4-124">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="c53c4-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="c53c4-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="c53c4-125">_lppPropData_</span></span>
  
> <span data-ttu-id="c53c4-126">Out Zeiger auf einen Zeiger auf das zurückgegebene Eigenschaftendaten Objekt.</span><span class="sxs-lookup"><span data-stu-id="c53c4-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c53c4-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c53c4-127">Return value</span></span>

<span data-ttu-id="c53c4-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="c53c4-128">S_OK</span></span> 
  
> <span data-ttu-id="c53c4-129">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c53c4-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c53c4-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="c53c4-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="c53c4-131">Die angeforderte Schnittstelle wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c53c4-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c53c4-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c53c4-132">Remarks</span></span>

<span data-ttu-id="c53c4-133">Die _lpAllocateBuffer_-, _LpAllocateMore_-und _lpFreeBuffer_ -Eingabeparameter zeigen auf die [MAPIAllocateBuffer](mapiallocatebuffer.md)-, [MAPIAllocateMore](mapiallocatemore.md)-und [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c53c4-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="c53c4-134">Eine Clientanwendung, die **CreateIProp** aufruft, übergibt Zeiger auf die soeben benannten MAPI-Funktionen. ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er bei seinem Initialisierungsaufruf erhalten hat, oder wird mit einem Aufruf der [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c53c4-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  


---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427493"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="a6d69-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="a6d69-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="a6d69-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6d69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6d69-105">Markiert ein Objekt als unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="a6d69-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="a6d69-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6d69-106">Parameters</span></span>

 <span data-ttu-id="a6d69-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6d69-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a6d69-108">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a6d69-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a6d69-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="a6d69-109">_lpObject_</span></span>
  
> <span data-ttu-id="a6d69-110">in Ein Zeiger auf das Objekt, das ungültig werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6d69-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="a6d69-111">Die Schnittstelle des Objekts muss von **IUnknown**abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a6d69-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="a6d69-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="a6d69-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="a6d69-113">in Der aktuelle Verweiszähler des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6d69-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="a6d69-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="a6d69-114">_cMethods_</span></span>
  
> <span data-ttu-id="a6d69-115">in Die Anzahl der Methoden in der Vtable des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6d69-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6d69-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6d69-116">Return value</span></span>

<span data-ttu-id="a6d69-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6d69-117">S_OK</span></span> 
  
> <span data-ttu-id="a6d69-118">Das Objekt wurde erfolgreich als unbrauchbar gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="a6d69-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6d69-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6d69-119">Remarks</span></span>

<span data-ttu-id="a6d69-120">Die **IMAPISupport:: MakeInvalid** -Methode wird für alle Support-Objekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="a6d69-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="a6d69-121">Das Objekt, das ungültig werden soll, muss von der **IUnknown** -Schnittstelle oder von einer von **IUnknown**abgeleiteten Schnittstelle abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a6d69-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="a6d69-122">**MakeInvalid** markiert ein Objekt als unbrauchbar, indem die Vtable des Objekts durch eine Stub-Vtable mit ähnlicher Größe ersetzt wird, in der die Methoden **IUnknown:: AddRef** und **IUnknown:: Release** wie erwartet ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6d69-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="a6d69-123">Allerdings schlagen alle anderen Methoden fehl, wobei der Wert MAPI_E_INVALID_OBJECT zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6d69-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6d69-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a6d69-124">Notes to callers</span></span>

<span data-ttu-id="a6d69-125">Dienstanbieter und Nachrichtendienste rufen **MakeInvalid** in der Regel beim Herunterfahren auf.</span><span class="sxs-lookup"><span data-stu-id="a6d69-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="a6d69-126">**MakeInvalid** kann jedoch jederzeit aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a6d69-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="a6d69-127">Wenn ein Client beispielsweise ein Objekt freigibt, ohne einige seiner unter Objekte freizugeben, können Sie **MakeInvalid** sofort aufrufen, um diese unter Objekte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a6d69-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="a6d69-128">Sie müssen das Objekt besitzen, das Sie ungültig machen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6d69-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="a6d69-129">Sie muss mindestens 16 Bytes lang sein und mindestens drei Methoden in ihrer vtable aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a6d69-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="a6d69-130">Sie können **MakeInvalid** aufrufen und dann alle Aufgaben zum Herunterfahren ausführen, wie das Verwerfen zugeordneter Datenstrukturen, die in der Regel während der Freigabe eines Objekts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6d69-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="a6d69-131">Code zur Unterstützung des Objekts muss nicht im Arbeitsspeicher aufbewahrt werden, da MAPI den Arbeitsspeicher durch Aufrufen von [mapifreebufferfreigegeben](mapifreebuffer.md) freigibt und das Objekt dann frei gibt.</span><span class="sxs-lookup"><span data-stu-id="a6d69-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="a6d69-132">Sie können Ressourcen freigeben, **MakeInvalid**aufrufen und dann das Invalidated-Objekt ignorieren.</span><span class="sxs-lookup"><span data-stu-id="a6d69-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6d69-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d69-133">See also</span></span>



[<span data-ttu-id="a6d69-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a6d69-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a6d69-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6d69-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


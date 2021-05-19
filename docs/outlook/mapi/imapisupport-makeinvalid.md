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
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="80096-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="80096-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="80096-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80096-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80096-105">Markiert ein Objekt als nicht verwendbar.</span><span class="sxs-lookup"><span data-stu-id="80096-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="80096-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80096-106">Parameters</span></span>

 <span data-ttu-id="80096-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80096-107">_ulFlags_</span></span>
  
> <span data-ttu-id="80096-108">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="80096-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="80096-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="80096-109">_lpObject_</span></span>
  
> <span data-ttu-id="80096-110">[in] Ein Zeiger auf das zu ungültige Objekt.</span><span class="sxs-lookup"><span data-stu-id="80096-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="80096-111">Die Schnittstelle des Objekts muss von **IUnknown abgeleitet werden.**</span><span class="sxs-lookup"><span data-stu-id="80096-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="80096-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="80096-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="80096-113">[in] Die aktuelle Referenzanzahl des Objekts.</span><span class="sxs-lookup"><span data-stu-id="80096-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="80096-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="80096-114">_cMethods_</span></span>
  
> <span data-ttu-id="80096-115">[in] Die Anzahl der Methoden in der vtable des Objekts.</span><span class="sxs-lookup"><span data-stu-id="80096-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80096-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80096-116">Return value</span></span>

<span data-ttu-id="80096-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="80096-117">S_OK</span></span> 
  
> <span data-ttu-id="80096-118">Das Objekt wurde erfolgreich als nicht verwendbar gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="80096-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80096-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80096-119">Remarks</span></span>

<span data-ttu-id="80096-120">Die **IMAPISupport::MakeInvalid-Methode** wird für alle Supportobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="80096-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="80096-121">Das zu ungültige Objekt muss von der **IUnknown-Schnittstelle** oder von einer von **IUnknown** abgeleiteten Schnittstelle abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="80096-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="80096-122">**MakeInvalid** markiert ein Objekt als nicht verwendbar, indem die vtable des Objekts durch eine Stub-Vtable ähnlicher Größe ersetzt wird, bei der die **Methoden IUnknown::AddRef** und **IUnknown::Release** wie erwartet auftreten.</span><span class="sxs-lookup"><span data-stu-id="80096-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="80096-123">Bei allen anderen Methoden ist jedoch ein Fehler zu begehen, und der Wert wird MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="80096-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="80096-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="80096-124">Notes to callers</span></span>

<span data-ttu-id="80096-125">Dienstanbieter und Nachrichtendienste rufen **MakeInvalid** normalerweise zum Zeitpunkt des Herunterfahrens auf.</span><span class="sxs-lookup"><span data-stu-id="80096-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="80096-126">**MakeInvalid** kann jedoch jederzeit aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="80096-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="80096-127">Wenn ein Client beispielsweise ein Objekt freilässt, ohne einige seiner Unterobjekte frei zu geben, können Sie **MakeInvalid** sofort aufrufen, um diese Unterobjekte frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="80096-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="80096-128">Sie müssen das Objekt besitzen, das Sie ungültig zu machen versuchen.</span><span class="sxs-lookup"><span data-stu-id="80096-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="80096-129">Er muss mindestens 16 Byte lang sein und mindestens drei Methoden in seiner vtable enthalten.</span><span class="sxs-lookup"><span data-stu-id="80096-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="80096-130">Sie können **MakeInvalid** aufrufen und dann alle herunterfahrenden Aufgaben ausführen, z. B. das Verwerfen zugeordneter Datenstrukturen, die in der Regel während der Veröffentlichung eines Objekts durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="80096-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="80096-131">Code zur Unterstützung des Objekts muss nicht im Arbeitsspeicher gespeichert werden, da MAPI den Arbeitsspeicher durch aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) und dann das Objekt freilässt.</span><span class="sxs-lookup"><span data-stu-id="80096-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="80096-132">Sie können Ressourcen frei geben, **MakeInvalid aufrufen** und dann das ungültige Objekt ignorieren.</span><span class="sxs-lookup"><span data-stu-id="80096-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80096-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80096-133">See also</span></span>



[<span data-ttu-id="80096-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="80096-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="80096-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="80096-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 595d5fdba28634b038838921102d3125135452a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792374"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="4029b-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="4029b-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="4029b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4029b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4029b-105">Markiert ein Objekt als nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4029b-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="4029b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4029b-106">Parameters</span></span>

 <span data-ttu-id="4029b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4029b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4029b-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="4029b-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4029b-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="4029b-109">_lpObject_</span></span>
  
> <span data-ttu-id="4029b-110">[in] Ein Zeiger auf das Objekt, das ungültig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="4029b-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="4029b-111">Die Schnittstelle des Objekts muss von **IUnknown**abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4029b-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="4029b-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="4029b-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="4029b-113">[in] Das Objekt vorhanden Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="4029b-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="4029b-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="4029b-114">_cMethods_</span></span>
  
> <span data-ttu-id="4029b-115">[in] Die Anzahl der Methoden in der Vtable des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4029b-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4029b-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4029b-116">Return value</span></span>

<span data-ttu-id="4029b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="4029b-117">S_OK</span></span> 
  
> <span data-ttu-id="4029b-118">Das Objekt wurde erfolgreich als nicht verwendbar gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="4029b-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4029b-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4029b-119">Remarks</span></span>

<span data-ttu-id="4029b-120">Die **IMAPISupport::MakeInvalid** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="4029b-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="4029b-121">Das Objekt, das ungültig gemacht werden muss aus die **IUnknown** -Schnittstelle oder von einer Schnittstelle abgeleitet von **IUnknown**abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4029b-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="4029b-122">**MakeInvalid** markiert ein Objekt als nicht verwendbar durch Ersetzen des Objekts Vtable durch eine Stub Vtable ähnlicher Größe, in dem die **IUnknown:: AddRef** und **IUnknown** -Methoden wie erwartet ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4029b-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="4029b-123">Alle anderen Methoden Fehler jedoch auftreten, den Wert MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="4029b-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4029b-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4029b-124">Notes to callers</span></span>

<span data-ttu-id="4029b-125">Dienstanbieter und Message-Dienste in der Regel Aufrufen **MakeInvalid** Zeitpunkt zum Herunterfahren von.</span><span class="sxs-lookup"><span data-stu-id="4029b-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="4029b-126">**MakeInvalid** kann jedoch jederzeit aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4029b-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="4029b-127">Wenn ein Client ein Objekt ohne Freigabe einiger seiner Unterobjekte veröffentlicht, können Sie beispielsweise **MakeInvalid** sofort, um diese Unterobjekte release aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4029b-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="4029b-128">Sie müssen das Objekt verfügen, das Sie versuchen, die als ungültig zu erklären.</span><span class="sxs-lookup"><span data-stu-id="4029b-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="4029b-129">Es muss mindestens 16 Byte lang sein und mindestens drei Methoden in der Vtable haben.</span><span class="sxs-lookup"><span data-stu-id="4029b-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="4029b-130">Rufen Sie **MakeInvalid** und klicken Sie dann führt alle Herunterfahren, z. B. durch verwerfen zugehörigen Datenstrukturen, die während der Freigabe eines Objekts in der Regel erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4029b-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="4029b-131">Code, um das Objekt unterstützt muss nicht im Speicher aufbewahrt werden, da MAPI Speicher durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) freigibt, und das Objekt dann frei.</span><span class="sxs-lookup"><span data-stu-id="4029b-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="4029b-132">Ressourcen freizugeben, rufen Sie **MakeInvalid**, und klicken Sie dann das Objekt ungültig zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="4029b-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4029b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4029b-133">See also</span></span>



[<span data-ttu-id="4029b-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4029b-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4029b-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4029b-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


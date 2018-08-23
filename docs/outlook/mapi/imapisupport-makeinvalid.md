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
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570737"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="13856-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="13856-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="13856-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13856-105">Markiert ein Objekt als nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13856-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="13856-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13856-106">Parameters</span></span>

 <span data-ttu-id="13856-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13856-107">_ulFlags_</span></span>
  
> <span data-ttu-id="13856-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="13856-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="13856-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="13856-109">_lpObject_</span></span>
  
> <span data-ttu-id="13856-110">[in] Ein Zeiger auf das Objekt, das ungültig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="13856-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="13856-111">Die Schnittstelle des Objekts muss von **IUnknown**abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="13856-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="13856-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="13856-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="13856-113">[in] Das Objekt vorhanden Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="13856-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="13856-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="13856-114">_cMethods_</span></span>
  
> <span data-ttu-id="13856-115">[in] Die Anzahl der Methoden in der Vtable des Objekts.</span><span class="sxs-lookup"><span data-stu-id="13856-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13856-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="13856-116">Return value</span></span>

<span data-ttu-id="13856-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="13856-117">S_OK</span></span> 
  
> <span data-ttu-id="13856-118">Das Objekt wurde erfolgreich als nicht verwendbar gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="13856-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13856-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="13856-119">Remarks</span></span>

<span data-ttu-id="13856-120">Die **IMAPISupport::MakeInvalid** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="13856-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="13856-121">Das Objekt, das ungültig gemacht werden muss aus die **IUnknown** -Schnittstelle oder von einer Schnittstelle abgeleitet von **IUnknown**abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="13856-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="13856-122">**MakeInvalid** markiert ein Objekt als nicht verwendbar durch Ersetzen des Objekts Vtable durch eine Stub Vtable ähnlicher Größe, in dem die **IUnknown:: AddRef** und **IUnknown** -Methoden wie erwartet ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="13856-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="13856-123">Alle anderen Methoden Fehler jedoch auftreten, den Wert MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="13856-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="13856-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="13856-124">Notes to callers</span></span>

<span data-ttu-id="13856-125">Dienstanbieter und Message-Dienste in der Regel Aufrufen **MakeInvalid** Zeitpunkt zum Herunterfahren von.</span><span class="sxs-lookup"><span data-stu-id="13856-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="13856-126">**MakeInvalid** kann jedoch jederzeit aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="13856-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="13856-127">Wenn ein Client ein Objekt ohne Freigabe einiger seiner Unterobjekte veröffentlicht, können Sie beispielsweise **MakeInvalid** sofort, um diese Unterobjekte release aufrufen.</span><span class="sxs-lookup"><span data-stu-id="13856-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="13856-128">Sie müssen das Objekt verfügen, das Sie versuchen, die als ungültig zu erklären.</span><span class="sxs-lookup"><span data-stu-id="13856-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="13856-129">Es muss mindestens 16 Byte lang sein und mindestens drei Methoden in der Vtable haben.</span><span class="sxs-lookup"><span data-stu-id="13856-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="13856-130">Rufen Sie **MakeInvalid** und klicken Sie dann führt alle Herunterfahren, z. B. durch verwerfen zugehörigen Datenstrukturen, die während der Freigabe eines Objekts in der Regel erfolgt.</span><span class="sxs-lookup"><span data-stu-id="13856-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="13856-131">Code, um das Objekt unterstützt muss nicht im Speicher aufbewahrt werden, da MAPI Speicher durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md) freigibt, und das Objekt dann frei.</span><span class="sxs-lookup"><span data-stu-id="13856-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="13856-132">Ressourcen freizugeben, rufen Sie **MakeInvalid**, und klicken Sie dann das Objekt ungültig zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="13856-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13856-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13856-133">See also</span></span>



[<span data-ttu-id="13856-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="13856-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="13856-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="13856-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


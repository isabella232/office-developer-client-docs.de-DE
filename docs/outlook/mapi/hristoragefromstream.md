---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563923"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="bd9dc-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="bd9dc-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="bd9dc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd9dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd9dc-105">Ebenen eine **IStorage** -Schnittstelle auf **IStream** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd9dc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bd9dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd9dc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bd9dc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bd9dc-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="bd9dc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bd9dc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bd9dc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bd9dc-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="bd9dc-110">Called by:</span></span>  <br/> |<span data-ttu-id="bd9dc-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="bd9dc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="bd9dc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd9dc-112">Parameters</span></span>

 <span data-ttu-id="bd9dc-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="bd9dc-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="bd9dc-114">[in] Zeiger auf die **IUnknown** -Objekt **IStream**implementieren.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="bd9dc-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bd9dc-115">_lpInterface_</span></span>
  
> <span data-ttu-id="bd9dc-116">[in] Zeiger auf der Benutzeroberfläche IID (Identifier) für das Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="bd9dc-117">Eines der folgenden Werte im _LpInterface_ -Parameter übergeben werden kann: NULL, IID_IStream oder IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="bd9dc-118">Übergeben von NULL in _LpInterface_ ist identisch mit der Übergabe IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="bd9dc-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bd9dc-119">_ulFlags_</span></span>
  
> <span data-ttu-id="bd9dc-120">[in] Bitmaske aus Flags, die steuert, wie das Objekt ist relativ zu der Stream erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="bd9dc-121">Die Standardeinstellung ist STGSTRM_RESET, die ermöglicht des Zugriffs nur-Lese-Speicher und startet ihn an der Position 0 (null) des Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="bd9dc-122">Die folgenden Kennzeichen können eine beliebige Kombination außer festgelegt werden, wie bereits erwähnt:</span><span class="sxs-lookup"><span data-stu-id="bd9dc-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="bd9dc-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="bd9dc-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="bd9dc-124">Erstellt ein neues Speicherobjekt für das Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="bd9dc-125">Dieses Kennzeichen können nicht festgelegt werden, wenn das Flag STGSTRM_RESET festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="bd9dc-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="bd9dc-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="bd9dc-127">Startet Speicher an der aktuellen Position des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="bd9dc-128">Dieses Kennzeichen können nicht festgelegt werden, wenn das Flag STGSTRM_RESET festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="bd9dc-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bd9dc-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="bd9dc-130">Ermöglicht es dem aufrufenden Dienstanbieter, in der zurückgegebene Speicher zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="bd9dc-131">Dieses Kennzeichen können nicht festgelegt werden, wenn das Flag STGSTRM_RESET festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="bd9dc-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="bd9dc-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="bd9dc-133">Startet Speicher an Position 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bd9dc-133">Starts storage at position zero.</span></span> <span data-ttu-id="bd9dc-134">Dieses Kennzeichen können nicht festgelegt werden, wenn alle anderen Kennzeichen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="bd9dc-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="bd9dc-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="bd9dc-136">[out] Zeiger auf einen Zeiger auf das zurückgegebene **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bd9dc-137">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bd9dc-137">Return value</span></span>

<span data-ttu-id="bd9dc-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd9dc-138">S_OK</span></span> 
  
> <span data-ttu-id="bd9dc-139">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd9dc-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd9dc-140">Remarks</span></span>

<span data-ttu-id="bd9dc-141">Nachricht speichern-Anbieter unterstützen die **HrIStorageFromStream** -Funktion mit der **IStorage** -Schnittstelle für Anlagen.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="bd9dc-142">Speicheranbieter müssen die **IStream** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="bd9dc-143">**HrIStorageFromStream** stellt die **IStorage** -Schnittstelle für das **IStream** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="bd9dc-144">Es ist möglich, eine **ILockBytes** oder eine **IStream** -Schnittstelle in _LpUnkIn_übergeben.</span><span class="sxs-lookup"><span data-stu-id="bd9dc-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  


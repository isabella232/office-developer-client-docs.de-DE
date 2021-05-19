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
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416832"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="03709-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="03709-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="03709-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03709-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03709-105">**Überschichtt eine IStorage-Schnittstelle** auf ein **IStream-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="03709-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03709-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="03709-106">Header file:</span></span>  <br/> |<span data-ttu-id="03709-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="03709-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="03709-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="03709-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="03709-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="03709-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="03709-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="03709-110">Called by:</span></span>  <br/> |<span data-ttu-id="03709-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="03709-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="03709-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="03709-112">Parameters</span></span>

 <span data-ttu-id="03709-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="03709-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="03709-114">[in] Zeiger auf das **IUnknown-Objekt,** das **IStream implementieren soll.**</span><span class="sxs-lookup"><span data-stu-id="03709-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="03709-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="03709-115">_lpInterface_</span></span>
  
> <span data-ttu-id="03709-116">[in] Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) für das Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03709-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="03709-117">Jeder der folgenden Werte kann im  _lpInterface-Parameter_ übergeben werden: NULL, IID_IStream oder IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="03709-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="03709-118">Das Übergeben von NULL in  _lpInterface_ ist identisch mit dem Übergeben IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="03709-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="03709-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03709-119">_ulFlags_</span></span>
  
> <span data-ttu-id="03709-120">[in] Bitmaske von Flags, die steuert, wie das Speicherobjekt relativ zum Datenstrom erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03709-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="03709-121">Die Standardeinstellung ist STGSTRM_RESET, die dem Speicherobjekt schreibgeschützten Zugriff gewährt und an Position 0 des Datenstroms startet.</span><span class="sxs-lookup"><span data-stu-id="03709-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="03709-122">Die folgenden Flags können in beliebiger Kombination festgelegt werden, außer wie erwähnt:</span><span class="sxs-lookup"><span data-stu-id="03709-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="03709-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="03709-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="03709-124">Erstellt ein neues Speicherobjekt für das Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03709-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="03709-125">Dieses Flag kann nicht festgelegt werden, wenn STGSTRM_RESET festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03709-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="03709-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="03709-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="03709-127">Startet den Speicher an der aktuellen Position des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="03709-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="03709-128">Dieses Flag kann nicht festgelegt werden, wenn STGSTRM_RESET festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03709-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="03709-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="03709-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="03709-130">Ermöglicht dem aufrufenden Dienstanbieter das Schreiben in den zurückgegebenen Speicher.</span><span class="sxs-lookup"><span data-stu-id="03709-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="03709-131">Dieses Flag kann nicht festgelegt werden, wenn STGSTRM_RESET festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03709-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="03709-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="03709-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="03709-133">Startet den Speicher an Position 0.</span><span class="sxs-lookup"><span data-stu-id="03709-133">Starts storage at position zero.</span></span> <span data-ttu-id="03709-134">Dieses Flag kann nicht festgelegt werden, wenn ein anderes Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03709-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="03709-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="03709-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="03709-136">[out] Zeiger auf einen Zeiger auf das zurückgegebene **IStorage-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="03709-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="03709-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03709-137">Return value</span></span>

<span data-ttu-id="03709-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="03709-138">S_OK</span></span> 
  
> <span data-ttu-id="03709-139">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="03709-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03709-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03709-140">Remarks</span></span>

<span data-ttu-id="03709-141">Nachrichtenspeicheranbieter unterstützen die **HrIStorageFromStream-Funktion** mithilfe der **IStorage-Schnittstelle** für Anlagen.</span><span class="sxs-lookup"><span data-stu-id="03709-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="03709-142">Store müssen die **IStream-Schnittstelle** implementieren.</span><span class="sxs-lookup"><span data-stu-id="03709-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="03709-143">**HrIStorageFromStream** stellt die **IStorage-Schnittstelle** für das **IStream-Objekt** bereit.</span><span class="sxs-lookup"><span data-stu-id="03709-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="03709-144">Es ist möglich, entweder ein **ILockBytes** oder eine **IStream-Schnittstelle** in _lpUnkIn zu übergeben._</span><span class="sxs-lookup"><span data-stu-id="03709-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  


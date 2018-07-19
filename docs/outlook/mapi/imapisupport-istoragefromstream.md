---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792376"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="9eb17-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="9eb17-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="9eb17-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9eb17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9eb17-105">Zugriff auf einen Datenstrom ein Speicherobjekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="9eb17-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="9eb17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eb17-106">Parameters</span></span>

 <span data-ttu-id="9eb17-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="9eb17-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="9eb17-108">[in] Ein Zeiger auf ein Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="9eb17-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9eb17-109">_lpInterface_</span></span>
  
> <span data-ttu-id="9eb17-110">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, für den Zugriff auf das _LpUnkIn_Streams auf darstellt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="9eb17-111">Eines der folgenden Werte sind gültig: IID_IStream, IID_ILockBytes, oder **null**, gibt an, dass die [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Schnittstelle zum Zugriff auf den Stream verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9eb17-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="9eb17-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9eb17-112">_ulFlags_</span></span>
  
> <span data-ttu-id="9eb17-113">[in] Eine Bitmaske aus Flags, die steuert, wie das Speicherobjekt ist relativ zu der Stream-Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9eb17-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="9eb17-114">Standardmäßig wird der Speicher mit Schreibschutz erstellt und der Stream beginnt an der Position 0 (null) im Speicher.</span><span class="sxs-lookup"><span data-stu-id="9eb17-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="9eb17-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9eb17-115">The following flags can be set:</span></span>
    
<span data-ttu-id="9eb17-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="9eb17-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="9eb17-117">Ein neues Speicherobjekt sollten für das Stream-Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9eb17-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="9eb17-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="9eb17-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="9eb17-119">Das Speicherobjekt sollte an der aktuellen Position des Datenstroms beginnen.</span><span class="sxs-lookup"><span data-stu-id="9eb17-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="9eb17-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9eb17-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="9eb17-121">Der Aufrufer sollte Lese-/Schreibberechtigung für das zurückgegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="9eb17-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="9eb17-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="9eb17-123">Das Speicherobjekt sollte an Position 0 (null) beginnen.</span><span class="sxs-lookup"><span data-stu-id="9eb17-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="9eb17-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="9eb17-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="9eb17-125">[out] Ein Zeiger auf einen Zeiger auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9eb17-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9eb17-126">Return value</span></span>

<span data-ttu-id="9eb17-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="9eb17-127">S_OK</span></span> 
  
> <span data-ttu-id="9eb17-128">Das Objekt wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9eb17-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eb17-129">Remarks</span></span>

<span data-ttu-id="9eb17-130">Die **IMAPISupport::IStorageFromStream** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="9eb17-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="9eb17-131">Dienstanbieter Aufrufen **IStorageFromStream** zum Erstellen eines Speicherobjekts für bestimmte Eigenschaften zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9eb17-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="9eb17-132">Dienstanbieter, die ihre eigene Implementierung der Schnittstelle [IStorage](http://msdn.microsoft.com/de-de/library/aa380015%28VS.85%29.aspx) haben, müssen nicht **IStorageFromStream**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9eb17-132">Service providers that have their own implementation of the [IStorage](http://msdn.microsoft.com/de-de/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="9eb17-133">Erstelltes **IStorageFromStream** Speicherobjekt ruft der Stream [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) -Methode, um erhöht den Referenzzähler und dann die dekrementiert die Anzahl der, wenn der Speicher freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9eb17-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9eb17-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9eb17-134">Notes to callers</span></span>

<span data-ttu-id="9eb17-135">Wenn die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der Objekte aufgerufen wird, um eine Eigenschaft mit der **IStorage** -Schnittstelle zu öffnen, führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="9eb17-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="9eb17-136">Öffnen Sie ein Stream-Objekt mit Lese-/Schreibberechtigung für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9eb17-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="9eb17-137">Markieren Sie den Eigenschaftenstream intern als Speicherobjekt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="9eb17-138">Rufen Sie **IStorageFromStream** um ein Speicherobjekt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9eb17-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="9eb17-139">Ein Zeiger auf dieses Speicherobjekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9eb17-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="9eb17-140">Wenn Sie zusätzliche Schnittstellen, die das Objekt verwenden implementieren, erstellen Sie ein Objekt, das das Speicherobjekt umbrochen wird, und Implementieren einer höheren Ebene [QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9eb17-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="9eb17-141">Lassen Sie keine Eigenschaft mit der **IStream** -Schnittstelle geöffnet werden soll, wenn sie mit **IStorage**erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9eb17-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="9eb17-142">Lassen Sie eine Eigenschaft mit der **IStorage** -Schnittstelle geöffnet werden soll, wenn sie mit **IStream**erstellt wurde dagegen nicht zu.</span><span class="sxs-lookup"><span data-stu-id="9eb17-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="9eb17-143">Mit einer Ausnahme für die **IStreamDocfile** -Oberfläche verwenden, um ein Speicherobjekt aus einem Container in einen anderen stream akzeptabel ist, aber der IID_IStreamDocfile Schnittstellenbezeichner muss in der **OpenProperty** Methode _übergeben werden LpInterface _Parameter.</span><span class="sxs-lookup"><span data-stu-id="9eb17-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9eb17-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9eb17-144">See also</span></span>



[<span data-ttu-id="9eb17-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9eb17-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="9eb17-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9eb17-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


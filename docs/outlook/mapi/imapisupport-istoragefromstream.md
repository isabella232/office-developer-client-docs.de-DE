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
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316587"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="b8517-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="b8517-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="b8517-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8517-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8517-105">Implementiert ein Speicherobjekt für den Zugriff auf einen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="b8517-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="b8517-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8517-106">Parameters</span></span>

 <span data-ttu-id="b8517-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="b8517-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="b8517-108">[in] Ein Zeiger auf ein Streamobjekt.</span><span class="sxs-lookup"><span data-stu-id="b8517-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="b8517-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b8517-109">_lpInterface_</span></span>
  
> <span data-ttu-id="b8517-110">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Datenstrom verwendet werden soll, auf den _lpUnkIn verweist._</span><span class="sxs-lookup"><span data-stu-id="b8517-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="b8517-111">Jeder der folgenden Werte ist gültig: IID_IStream, IID_ILockBytes oder **Null**, was angibt, dass die [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) für den Zugriff auf den Datenstrom verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8517-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="b8517-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8517-112">_ulFlags_</span></span>
  
> <span data-ttu-id="b8517-113">[in] Eine Bitmaske mit Flags, die steuert, wie das Speicherobjekt relativ zum Streamobjekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8517-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="b8517-114">Standardmäßig wird der Speicher mit schreibgeschützten Zugriff erstellt, und der Datenstrom beginnt an Position 0 im Speicher.</span><span class="sxs-lookup"><span data-stu-id="b8517-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="b8517-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b8517-115">The following flags can be set:</span></span>
    
<span data-ttu-id="b8517-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="b8517-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="b8517-117">Ein neues Speicherobjekt sollte für das Streamobjekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8517-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="b8517-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="b8517-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="b8517-119">Das Speicherobjekt sollte an der aktuellen Position des Datenstroms beginnen.</span><span class="sxs-lookup"><span data-stu-id="b8517-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="b8517-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b8517-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="b8517-121">Der Aufrufer sollte über Lese-/Schreibberechtigungen für das zurückgegebene Speicherobjekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="b8517-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="b8517-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="b8517-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="b8517-123">Das Speicherobjekt sollte an Position 0 beginnen.</span><span class="sxs-lookup"><span data-stu-id="b8517-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="b8517-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="b8517-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="b8517-125">[out] Ein Zeiger auf einen Zeiger auf das Speicherobjekt.</span><span class="sxs-lookup"><span data-stu-id="b8517-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8517-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8517-126">Return value</span></span>

<span data-ttu-id="b8517-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8517-127">S_OK</span></span> 
  
> <span data-ttu-id="b8517-128">Das Speicherobjekt wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8517-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8517-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8517-129">Remarks</span></span>

<span data-ttu-id="b8517-130">Die **IMAPISupport::IStorageFromStream-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8517-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="b8517-131">Dienstanbieter rufen **IStorageFromStream auf,** um ein Speicherobjekt zum Öffnen bestimmter Eigenschaften zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8517-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="b8517-132">Dienstanbieter, die über eine eigene Implementierung der [IStorage-Schnittstelle](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) verfügen, müssen **IStorageFromStream nicht aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="b8517-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="b8517-133">Das von **IStorageFromStream** erstellte Speicherobjekt ruft die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) des Datenstroms auf, um die Referenzanzahl zu erhöhen und die Anzahl dann zu dekrementieren, wenn der Speicher freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b8517-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b8517-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b8517-134">Notes to callers</span></span>

<span data-ttu-id="b8517-135">Wenn die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) eines Ihrer Objekte aufgerufen wird, um eine Eigenschaft mit der **IStorage-Schnittstelle** zu öffnen, führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="b8517-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="b8517-136">Öffnen Sie ein Stream-Objekt mit Lese-/Schreibberechtigung für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b8517-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="b8517-137">Markieren Sie den Eigenschaftendatenstrom intern als Speicherobjekt.</span><span class="sxs-lookup"><span data-stu-id="b8517-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="b8517-138">Rufen **Sie IStorageFromStream auf,** um ein Speicherobjekt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b8517-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="b8517-139">Gibt einen Zeiger auf dieses Speicherobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b8517-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="b8517-140">Wenn Sie zusätzliche Schnittstellen implementieren, die das Speicherobjekt verwenden, erstellen Sie ein Objekt, das das Speicherobjekt umschließt, und implementieren Sie eine [höhere IUnknown::QueryInterface-Methode.](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8517-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="b8517-141">Lassen Sie nicht zu, dass eine Eigenschaft mit der **IStream-Schnittstelle** geöffnet wird, wenn sie mit **IStorage erstellt wurde.**</span><span class="sxs-lookup"><span data-stu-id="b8517-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="b8517-142">Lassen Sie dagegen nicht zu, dass eine Eigenschaft mit der **IStorage-Schnittstelle** geöffnet wird, wenn sie mit **IStream erstellt wurde.**</span><span class="sxs-lookup"><span data-stu-id="b8517-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="b8517-143">Mit einer Ausnahme ist es akzeptabel, die **IStreamDocfile-Schnittstelle** zum Streamen eines Speicherobjekts von einem Container in einen anderen zu verwenden, aber der IID_IStreamDocfile-Schnittstellenbezeichner muss im _lpInterface-Parameter_ der **OpenProperty-Methode** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8517-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8517-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8517-144">See also</span></span>



[<span data-ttu-id="b8517-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="b8517-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="b8517-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8517-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


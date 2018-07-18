---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e9d9ca56a877c0106c76242fe97ce43321e62e08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792673"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="10f2e-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="10f2e-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="10f2e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10f2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10f2e-105">Öffnet einen Ordner oder Message-Objekt und gibt einen Zeiger auf das Objekt, das Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="10f2e-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="10f2e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10f2e-106">Parameters</span></span>

 <span data-ttu-id="10f2e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="10f2e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="10f2e-108">[in] Die Größe des Eintrags-ID, die auf das durch den Parameter _LpEntryID_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="10f2e-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="10f2e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="10f2e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="10f2e-110">[in] Ein Zeiger auf die Adresse des Eintrags-ID des Objekts Ordner oder eine Nachricht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="10f2e-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="10f2e-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="10f2e-111">_lpInterface_</span></span>
  
> <span data-ttu-id="10f2e-112">[in] Ein Zeiger auf der Benutzeroberfläche IID (Identifier) für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="10f2e-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="10f2e-113">Übergeben von NULL gibt an, dass das Objekt in der standard-Benutzeroberfläche für ein solches Objekt umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="10f2e-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="10f2e-114">Der Parameter _LpInterface_ kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="10f2e-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="10f2e-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="10f2e-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="10f2e-116">[in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="10f2e-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="10f2e-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="10f2e-117">The following flags can be set:</span></span>
    
<span data-ttu-id="10f2e-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="10f2e-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="10f2e-119">Das Objekt sollte mit den maximalen Berechtigungen für den Benutzer und die maximale Clientberechtigungen zulässigen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="10f2e-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="10f2e-120">Wenn der Client über Lese-/Schreibberechtigung verfügt, wird das Objekt beispielsweise mit Lese-/Schreibzugriff geöffnet. Wenn der Client nur-Lese-Berechtigung verfügt, wird das Objekt mit Leseberechtigung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="10f2e-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="10f2e-121">Der Client kann die Berechtigungsstufe Abrufen der **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="10f2e-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="10f2e-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="10f2e-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="10f2e-123">Der Aufruf ist zulässig, erfolgreich ausgeführt werden kann, auch wenn das zugrunde liegende Objekt nicht an die aufrufende Anwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="10f2e-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="10f2e-124">Wenn das Objekt nicht verfügbar ist, kann ein nachfolgender Aufruf für das Objekt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="10f2e-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="10f2e-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="10f2e-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="10f2e-126">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="10f2e-126">Requests read/write permission.</span></span> <span data-ttu-id="10f2e-127">Standardmäßig werden Objekte mit Leseberechtigung erstellt, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="10f2e-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="10f2e-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="10f2e-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="10f2e-129">[out] Ein Zeiger auf den Typ des Objekts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="10f2e-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="10f2e-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="10f2e-130">_lppUnk_</span></span>
  
> <span data-ttu-id="10f2e-131">[out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="10f2e-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10f2e-132">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="10f2e-132">Return value</span></span>

<span data-ttu-id="10f2e-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="10f2e-133">S_OK</span></span> 
  
> <span data-ttu-id="10f2e-134">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="10f2e-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10f2e-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10f2e-135">Remarks</span></span>

<span data-ttu-id="10f2e-136">MAPI-Aufrufen die **IMSLogon::OpenEntry** -Methode, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="10f2e-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="10f2e-137">MAPI übergibt die Eintrags-ID des Objekts zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="10f2e-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="10f2e-138">Der Nachricht Speicheranbieter sollte einen Zeiger zurückgegeben, der die weiteren Zugriff auf das Objekt im _LppUnk_ -Parameter angegebene ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="10f2e-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="10f2e-139">Bevor MAPI **IMSLogon::OpenEntry**aufruft, bestimmt zunächst, dass die angegebenen Nachricht oder Ordner Eintrags-ID eine durch diese Nachricht Speicheranbieter registrierten übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="10f2e-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="10f2e-140">Weitere Informationen dazu, wie Anbieter Eintragsbezeichner registrieren finden Sie unter [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="10f2e-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="10f2e-141">**IMSLogon::OpenEntry** ist identisch mit der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode des Message Store-Objekts, mit der Ausnahme, dass der Client nicht **IMSLogon::OpenEntry**aufgerufen wird. MAPI-Aufrufen **IMSLogon::OpenEntry** bei der Verarbeitung einer **IMAPISession::OpenEntry** -Methode.</span><span class="sxs-lookup"><span data-stu-id="10f2e-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="10f2e-142">Objekte, die mithilfe von **IMSLogon::OpenEntry** geöffnet werden sollte behandelt genau wie Speichern von Objekten, die mit der Meldung geöffnet-Objekt. Insbesondere sollten Objekte, die mithilfe dieses Anrufs geöffnet ungültig gemacht werden, wenn das Store-Nachrichtenspeicherobjekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10f2e-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10f2e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10f2e-143">See also</span></span>



[<span data-ttu-id="10f2e-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="10f2e-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="10f2e-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="10f2e-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="10f2e-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10f2e-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)


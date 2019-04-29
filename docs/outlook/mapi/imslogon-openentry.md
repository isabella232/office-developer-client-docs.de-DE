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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416300"
---
# <a name="imslogonopenentry"></a><span data-ttu-id="41fa5-103">IMSLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="41fa5-103">IMSLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="41fa5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41fa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41fa5-105">Öffnet ein Folder-oder Message-Objekt und gibt einen Zeiger auf das Objekt zurück, um weiteren Zugriff zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="41fa5-105">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="41fa5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41fa5-106">Parameters</span></span>

 <span data-ttu-id="41fa5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="41fa5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="41fa5-108">in Die Größe der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="41fa5-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="41fa5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="41fa5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="41fa5-110">in Ein Zeiger auf die Adresse der Eintrags-ID des zu öffnenden Folder-oder Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="41fa5-110">[in] A pointer to the address of the entry identifier of the folder or message object to open.</span></span> 
    
 <span data-ttu-id="41fa5-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="41fa5-111">_lpInterface_</span></span>
  
> <span data-ttu-id="41fa5-112">in Ein Zeiger auf die Schnittstellen-ID (IID) für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="41fa5-112">[in] A pointer to the interface identifier (IID) for the object.</span></span> <span data-ttu-id="41fa5-113">Übergeben von NULL gibt an, dass das Objekt für ein solches Objekt in die Standardschnittstelle umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="41fa5-113">Passing NULL indicates that the object is cast to the standard interface for such an object.</span></span> <span data-ttu-id="41fa5-114">Der _lpInterface_ -Parameter kann auch auf einen Bezeichner für eine entsprechende Schnittstelle für das Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="41fa5-114">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="41fa5-115">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="41fa5-115">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="41fa5-116">in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="41fa5-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="41fa5-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="41fa5-117">The following flags can be set:</span></span>
    
<span data-ttu-id="41fa5-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="41fa5-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="41fa5-119">Das Objekt sollte mit den maximal zulässigen Berechtigungen für den Benutzer und den maximalen Client Anwendungsberechtigungen geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="41fa5-119">The object should be opened with the maximum permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="41fa5-120">Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, wird das Objekt mit Lese-/Schreibzugriff geöffnet; Wenn der Client schreibgeschützte Berechtigung hat, wird das Objekt mit Leseberechtigung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="41fa5-120">For example, if the client has read/write permission, the object is opened with read/write permission; if the client has read-only permission, the object is opened with read-only permission.</span></span> <span data-ttu-id="41fa5-121">Der Client kann die Berechtigungsstufe abrufen, indem er die **PR_ACCESS_LEVEL** ([pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="41fa5-121">The client can retrieve the permission level by getting the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="41fa5-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="41fa5-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="41fa5-123">Der Aufruf kann auch dann erfolgreich ausgeführt werden, wenn das zugrunde liegende Objekt für die aufrufende Anwendung nicht zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="41fa5-123">The call is allowed to succeed even if the underlying object is not available to the calling application.</span></span> <span data-ttu-id="41fa5-124">Wenn das Objekt nicht verfügbar ist, kann bei einem nachfolgenden Aufruf des Objekts ein Fehler zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41fa5-124">If the object is not available, a subsequent call to the object might return an error.</span></span>
    
<span data-ttu-id="41fa5-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="41fa5-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="41fa5-126">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="41fa5-126">Requests read/write permission.</span></span> <span data-ttu-id="41fa5-127">Standardmäßig werden Objekte mit Leseberechtigung erstellt, und Clients sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibzugriff erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="41fa5-127">By default, objects are created with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="41fa5-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="41fa5-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="41fa5-129">Out Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="41fa5-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="41fa5-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="41fa5-130">_lppUnk_</span></span>
  
> <span data-ttu-id="41fa5-131">Out Ein Zeiger auf den Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="41fa5-131">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41fa5-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41fa5-132">Return value</span></span>

<span data-ttu-id="41fa5-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="41fa5-133">S_OK</span></span> 
  
> <span data-ttu-id="41fa5-134">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="41fa5-134">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41fa5-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41fa5-135">Remarks</span></span>

<span data-ttu-id="41fa5-136">MAPI Ruft die **IMSLogon:: OpenEntry** -Methode auf, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="41fa5-136">MAPI calls the **IMSLogon::OpenEntry** method to open a folder or a message in a message store.</span></span> <span data-ttu-id="41fa5-137">MAPI übergibt die Eintrags-ID des zu öffnenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="41fa5-137">MAPI passes in the entry identifier of the object to open.</span></span> <span data-ttu-id="41fa5-138">Der Nachrichtenspeicher Anbieter sollte einen Zeiger zurückgeben, der einen weiteren Zugriff auf das im _lppUnk_ -Parameter angegebene Objekt ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="41fa5-138">The message store provider should return a pointer that enables further access to the object specified in the  _lppUnk_ parameter.</span></span> 
  
<span data-ttu-id="41fa5-139">Bevor MAPI **IMSLogon:: OpenEntry**aufruft, bestimmt es zunächst, ob der angegebene Nachricht-oder Ordnereintrags Bezeichner einem von diesem Nachrichtenspeicher Anbieter registrierten entspricht.</span><span class="sxs-lookup"><span data-stu-id="41fa5-139">Before MAPI calls **IMSLogon::OpenEntry**, it first determines that the given message or folder entry identifier matches one registered by this message store provider.</span></span> <span data-ttu-id="41fa5-140">Weitere Informationen dazu, wie Speicheranbieter Eintrags-IDs registrieren, finden Sie unter [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="41fa5-140">For more information about how store providers register entry identifiers, see [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
  
 <span data-ttu-id="41fa5-141">**IMSLogon:: OpenEntry** ist identisch mit der [IMsgStore:: OpenEntry](imsgstore-openentry.md) -Methode des Nachrichtenspeicher Objekts, es sei denn, der Client ruft **IMSLogon:: OpenEntry**; MAPI ruft **IMSLogon:: OpenEntry** auf, wenn es eine **IMAPISession:: OpenEntry** -Methode verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="41fa5-141">**IMSLogon::OpenEntry** is identical to the [IMsgStore::OpenEntry](imsgstore-openentry.md) method of the message store object, except that the client does not call **IMSLogon::OpenEntry**; MAPI calls **IMSLogon::OpenEntry** when it processes an **IMAPISession::OpenEntry** method.</span></span> <span data-ttu-id="41fa5-142">Objekte, die mit **IMSLogon:: OpenEntry** geöffnet werden, sollten genau wie Objekte behandelt werden, die mit dem Nachrichtenspeicherobjekt geöffnet wurden; insbesondere werden Objekte, die mit diesem Aufruf geöffnet werden, beim Freigeben des Nachrichtenspeicher Objekts für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="41fa5-142">Objects opened by using **IMSLogon::OpenEntry** should be treated exactly the same as objects opened by using the message store object; in particular, objects opened by using this call should be invalidated when the message store object is released.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41fa5-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41fa5-143">See also</span></span>



[<span data-ttu-id="41fa5-144">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="41fa5-144">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="41fa5-145">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="41fa5-145">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="41fa5-146">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41fa5-146">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)


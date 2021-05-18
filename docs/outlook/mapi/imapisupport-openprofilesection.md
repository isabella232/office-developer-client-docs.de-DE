---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411386"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="b438f-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="b438f-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="b438f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b438f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b438f-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="b438f-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="b438f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b438f-106">Parameters</span></span>

 <span data-ttu-id="b438f-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="b438f-107">_lpUid_</span></span>
  
> <span data-ttu-id="b438f-108">[in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den zu öffnenden Profilabschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b438f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="b438f-109">Wenn Sie NULL für den  _lpUid-Parameter übergeben,_ wird der Profilabschnitt des Anrufers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b438f-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="b438f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b438f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b438f-111">[in] Eine Bitmaske mit Flags, die steuert, wie der Profilabschnitt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b438f-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="b438f-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b438f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b438f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b438f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b438f-114">Ermöglicht **openProfileSection,** erfolgreich zurückzukehren, möglicherweise bevor der Profilabschnitt vollständig für den Aufrufer zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="b438f-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="b438f-115">Wenn auf den Profilabschnitt nicht zugegriffen werden kann, kann ein nachfolgender Objektaufruf zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="b438f-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="b438f-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b438f-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b438f-117">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="b438f-117">Requests read/write permission.</span></span> <span data-ttu-id="b438f-118">Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="b438f-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="b438f-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="b438f-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="b438f-120">[out] Ein Zeiger auf einen Zeiger auf den geöffneten Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b438f-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b438f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b438f-121">Return value</span></span>

<span data-ttu-id="b438f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b438f-122">S_OK</span></span> 
  
> <span data-ttu-id="b438f-123">Der Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b438f-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="b438f-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b438f-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b438f-125">Es wurde versucht, einen schreibgeschützten Profilabschnitt zu ändern oder auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="b438f-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="b438f-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b438f-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b438f-127">Der in  _lpEntryID_ übergebenen Eintrags-ID ist kein Profilabschnitt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b438f-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="b438f-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="b438f-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="b438f-129">Reservierte oder nicht unterstützte Flags wurden verwendet, und daher wurde der Vorgang nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b438f-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b438f-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b438f-130">Remarks</span></span>

<span data-ttu-id="b438f-131">Die **IMAPISupport::OpenProfileSection-Methode** wird für alle Supportobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="b438f-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="b438f-132">Dienstanbieter und Nachrichtendienste rufen **OpenProfileSection auf,** um einen Profilabschnitt zu öffnen und einen Zeiger auf die **IProfSect-Schnittstellenimplementierung** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b438f-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b438f-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b438f-133">Notes to callers</span></span>

 <span data-ttu-id="b438f-134">**OpenProfileSection** öffnet Profilabschnitte als schreibgeschützt, es sei denn, Sie legen das MAPI_MODIFY im  _ulFlags-Parameter_ ein, und Ihre Berechtigung ist ausreichend.</span><span class="sxs-lookup"><span data-stu-id="b438f-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="b438f-135">Das Festlegen dieses Kennzeichens garantiert keine Lese-/Schreibberechtigung. Die Ihnen erteilten Berechtigungen hängen von Ihrer Zugriffsebene und dem Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="b438f-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="b438f-136">Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profilabschnitt als schreibgeschützt zu öffnen, wird MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="b438f-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="b438f-137">Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profilabschnitt als Lese-/Schreibzugriff zu öffnen, wird der Profilabschnitt erstellt und der **IProfSect-Zeiger** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b438f-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b438f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b438f-138">See also</span></span>



[<span data-ttu-id="b438f-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b438f-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="b438f-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b438f-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="b438f-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b438f-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b438f-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b438f-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


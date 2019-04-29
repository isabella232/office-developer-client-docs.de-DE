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
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="9b86c-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="9b86c-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="9b86c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b86c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b86c-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="9b86c-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="9b86c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b86c-106">Parameters</span></span>

 <span data-ttu-id="9b86c-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="9b86c-107">_lpUid_</span></span>
  
> <span data-ttu-id="9b86c-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den zu öffnenden Profil Abschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b86c-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="9b86c-109">Durch das Übergeben von NULL für den Parameter _lpUid_ wird der Profil Abschnitt des Anrufers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9b86c-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="9b86c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b86c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9b86c-111">in Eine Bitmaske von Flags, die die Art des Öffnens des Profil Abschnitts steuert.</span><span class="sxs-lookup"><span data-stu-id="9b86c-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="9b86c-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9b86c-112">The following flags can be set:</span></span>
    
<span data-ttu-id="9b86c-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9b86c-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9b86c-114">Ermöglicht es **OpenProfileSection** , erfolgreich zurückzugeben, möglicherweise bevor der Profil Abschnitt vollständig für den Aufrufer zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="9b86c-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="9b86c-115">Wenn der Profil Abschnitt nicht zugänglich ist, kann durch einen nachfolgenden Objektaufruf zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="9b86c-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="9b86c-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9b86c-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9b86c-117">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="9b86c-117">Requests read/write permission.</span></span> <span data-ttu-id="9b86c-118">Standardmäßig werden Objekte als schreibgeschützt geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass die Berechtigung "Lese-/Schreibzugriff" erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b86c-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="9b86c-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="9b86c-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="9b86c-120">Out Ein Zeiger auf einen Zeiger auf den geöffneten Profil Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="9b86c-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b86c-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b86c-121">Return value</span></span>

<span data-ttu-id="9b86c-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b86c-122">S_OK</span></span> 
  
> <span data-ttu-id="9b86c-123">Der Profil Abschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9b86c-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="9b86c-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9b86c-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9b86c-125">Es wurde versucht, einen schreibgeschützten Profil Abschnitt zu ändern oder auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9b86c-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="9b86c-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9b86c-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9b86c-127">Der Eintrags-ID, die in _lpEntryID_übergeben wurde, ist kein Profil Abschnitt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9b86c-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="9b86c-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9b86c-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="9b86c-129">ReServierte oder nicht unterstützte Flags wurden verwendet, daher wurde der Vorgang nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9b86c-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b86c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b86c-130">Remarks</span></span>

<span data-ttu-id="9b86c-131">Die **IMAPISupport:: OpenProfileSection** -Methode wird für alle Support-Objekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="9b86c-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="9b86c-132">Dienstanbieter und Nachrichtendienste rufen **OpenProfileSection** auf, um einen Profil Abschnitt zu öffnen und einen Zeiger auf die **IProfSect** -Schnittstellenimplementierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b86c-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b86c-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9b86c-133">Notes to callers</span></span>

 <span data-ttu-id="9b86c-134">**OpenProfileSection** öffnet Profilabschnitte als schreibgeschützt, es sei denn, Sie legen das MAPI_MODIFY-Flag im _ulFlags_ -Parameter fest, und ihre Berechtigung genügt.</span><span class="sxs-lookup"><span data-stu-id="9b86c-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="9b86c-135">Das Festlegen dieses Kennzeichens garantiert keine Lese-/Schreibzugriff; die Berechtigungen, die Ihnen erteilt werden, hängen von ihrer Zugriffsebene und dem Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="9b86c-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="9b86c-136">Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profil Abschnitt als schreibgeschützt zu öffnen, wird MAPI_E_NOT_FOUND zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b86c-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="9b86c-137">Wenn **OpenProfileSection** versucht, einen nicht vorhandenen Profil Abschnitt als Lese-/Schreibzugriff zu öffnen, erstellt er den profile-Abschnitt und gibt den **IProfSect** -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="9b86c-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b86c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b86c-138">See also</span></span>



[<span data-ttu-id="9b86c-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b86c-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="9b86c-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9b86c-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="9b86c-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9b86c-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9b86c-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b86c-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


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
ms.openlocfilehash: 2e1f546d33d4781f60df56b12fce437d1e7bd675
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588223"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="97614-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="97614-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="97614-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97614-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="97614-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="97614-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97614-106">Parameters</span></span>

 <span data-ttu-id="97614-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="97614-107">_lpUid_</span></span>
  
> <span data-ttu-id="97614-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die identifiziert den Profilabschnitt geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97614-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="97614-109">Übergeben NULL für den Parameter _LpUid_ wird des Anrufers Profilabschnitt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="97614-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="97614-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97614-110">_ulFlags_</span></span>
  
> <span data-ttu-id="97614-111">[in] Eine Bitmaske aus Flags, die steuert, wie im Profilabschnitt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="97614-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="97614-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="97614-112">The following flags can be set:</span></span>
    
<span data-ttu-id="97614-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="97614-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="97614-114">Ermöglicht **"OpenProfileSection"** zurückgegeben wurde, ist möglicherweise vor dem Profil Abschnitt vollständig mit dem Anrufer zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="97614-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="97614-115">Wenn der Profilabschnitt nicht möglich ist, kann nachfolgende Objekt Anrufen ein Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="97614-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="97614-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="97614-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="97614-117">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="97614-117">Requests read/write permission.</span></span> <span data-ttu-id="97614-118">In der Standardeinstellung Objekte werden als schreibgeschützt geöffnet, und Anrufer sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="97614-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="97614-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="97614-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="97614-120">[out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt geöffnete.</span><span class="sxs-lookup"><span data-stu-id="97614-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="97614-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="97614-121">Return value</span></span>

<span data-ttu-id="97614-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="97614-122">S_OK</span></span> 
  
> <span data-ttu-id="97614-123">Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="97614-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="97614-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="97614-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="97614-125">Es wurde versucht, einen Profilabschnitt schreibgeschützt ändern oder auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="97614-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="97614-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="97614-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="97614-127">Es ist kein Profilabschnitt _LpEntryID_übergebenen Eintrags-ID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="97614-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="97614-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="97614-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="97614-129">Reservierte oder nicht unterstützte Flags verwendet wurden und daher der Vorgang konnte nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="97614-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97614-130">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="97614-130">Remarks</span></span>

<span data-ttu-id="97614-131">Die **IMAPISupport::OpenProfileSection** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="97614-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="97614-132">Rufen **"OpenProfileSection"** zum Öffnen eines Abschnitts Profil und Abrufen eines Zeigers auf seine Implementierung **IProfSect** Dienstanbieter und Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="97614-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="97614-133">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="97614-133">Notes to callers</span></span>

 <span data-ttu-id="97614-134">**"OpenProfileSection"** öffnet Profil Abschnitte mit Schreibschutz, es sei denn, Sie die Kennzeichen MAPI_MODIFY im _UlFlags_ -Parameter festgelegt und die Berechtigung ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="97614-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="97614-135">Wenn Sie dieses Flag garantiert nicht Lese-/Schreibberechtigung. die Berechtigungen, die Sie erteilt werden, hängt von Ihrer Zugriffsebene und das Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="97614-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="97614-136">Wenn **"OpenProfileSection"** versucht, einen nicht vorhandenen Profilabschnitt im schreibgeschützten Modus zu öffnen, wird die MAPI_E_NOT_FOUND zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97614-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="97614-137">Wenn **"OpenProfileSection"** versucht, einen nicht vorhandenen Profilabschnitt mit Lese-/Schreibzugriff zu öffnen, Profilabschnitt erstellt und gibt den **IProfSect** Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="97614-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97614-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97614-138">See also</span></span>



[<span data-ttu-id="97614-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97614-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="97614-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="97614-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="97614-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="97614-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="97614-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="97614-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


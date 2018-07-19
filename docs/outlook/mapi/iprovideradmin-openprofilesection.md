---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 276a2bd84156e9b396df71f51130e6704ad7c7fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792784"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="ec3d0-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ec3d0-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="ec3d0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec3d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec3d0-105">Öffnet einen Profilabschnitt aus dem aktuellen Profil, und gibt einen [IProfSect](iprofsectimapiprop.md) Zeiger für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="ec3d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec3d0-106">Parameters</span></span>

 <span data-ttu-id="ec3d0-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="ec3d0-107">_lpUID_</span></span>
  
> <span data-ttu-id="ec3d0-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Profilabschnitt geöffnet werden enthält.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="ec3d0-109">Clients müssen nicht NULL für den _LpUID_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="ec3d0-110">Dienstanbieter können NULL, um die **MAPIUID** abzurufen, beim Aufruf aus ihrer Nachricht Service Entry Point Funktionen übergeben.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="ec3d0-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ec3d0-111">_lpInterface_</span></span>
  
> <span data-ttu-id="ec3d0-112">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="ec3d0-113">Bei Übergabe von NULL erzeugt Profilabschnitt Standardschnittstelle (**IProfSect**) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="ec3d0-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec3d0-114">_ulFlags_</span></span>
  
> <span data-ttu-id="ec3d0-115">[in] Eine Bitmaske aus Flags, die steuert, wie im Profilabschnitt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="ec3d0-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ec3d0-116">The following flags can be set:</span></span>
    
<span data-ttu-id="ec3d0-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ec3d0-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ec3d0-118">Ermöglicht **"OpenProfileSection"** erfolgreich, möglicherweise beendet, vor dem Profilabschnitt vollständig mit dem Anrufer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="ec3d0-119">Wenn im Profilabschnitt nicht verfügbar ist, kann die nachfolgenden Aufrufen es ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="ec3d0-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ec3d0-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ec3d0-121">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-121">Requests read/write permission.</span></span> <span data-ttu-id="ec3d0-122">Standardmäßig werden Objekte mit Leseberechtigung geöffnet, und Anrufer sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="ec3d0-123">Clients sind Lese-/Schreibberechtigung für Anbieter von Abschnitten des Profils nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="ec3d0-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ec3d0-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="ec3d0-125">Ermöglicht den Zugriff auf alle Abschnitte Profil, auch die einzelnen Dienstanbieter Besitz.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="ec3d0-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="ec3d0-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="ec3d0-127">[out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec3d0-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec3d0-128">Return value</span></span>

<span data-ttu-id="ec3d0-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec3d0-129">S_OK</span></span> 
  
> <span data-ttu-id="ec3d0-130">Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="ec3d0-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ec3d0-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ec3d0-132">Es wurde versucht, einen Profilabschnitt schreibgeschützt ändern oder auf ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="ec3d0-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ec3d0-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ec3d0-134">Abschnitt angeforderten Profile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec3d0-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec3d0-135">Remarks</span></span>

<span data-ttu-id="ec3d0-136">Die **IProviderAdmin::OpenProfileSection** -Methode öffnet einen Profilabschnitt, aktivieren den Anrufer zum Lesen von Informationen aus und Schreiben Sie möglicherweise Informationen in das aktive Profil.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="ec3d0-137">Clients können keine Profil Abschnitte öffnen, zu die Anbieter mithilfe der Methode **"OpenProfileSection"** gehören.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="ec3d0-138">Mehrere Clients oder Dienstanbieter können gleichzeitig einen Profilabschnitt mit Leseberechtigung öffnen.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="ec3d0-139">Wenn ein Profilabschnitt mit Lese-/Schreibzugriff geöffnet ist, können jedoch keine anderen Aufrufe vorgenommen werden, den Abschnitt, unabhängig von der Art von Access zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="ec3d0-140">Wenn ein Profilabschnitt mit Leseberechtigung geöffnet ist, wird ein nachfolgender Aufruf von Lese-/Schreibberechtigung für anfordern mit MAPI_E_NO_ACCESS fehl.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="ec3d0-141">Wenn ein Abschnitt mit Lese-/Schreibzugriff geöffnet ist, wird ein nachfolgender Aufruf Leseberechtigung anfordern auch fehl.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ec3d0-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ec3d0-142">Notes to callers</span></span>

<span data-ttu-id="ec3d0-143">Wenn Sie, die anfordern **"OpenProfileSection"** öffnen Sie einen nicht vorhandenen Profilabschnitt, indem Sie in _UlFlags_ MAPI_MODIFY übergeben, und eine unbekannte **MAPIUID** in _LpUID_, Profilabschnitt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="ec3d0-144">Wenn Sie anfordern, dass **"OpenProfileSection"** einen nicht vorhandenen Abschnitt mit Lesezugriff zu öffnen, wird die MAPI_E_NOT_FOUND zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec3d0-145">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="ec3d0-145">MFCMAPI reference</span></span>

<span data-ttu-id="ec3d0-146">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec3d0-147">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ec3d0-147">**File**</span></span>|<span data-ttu-id="ec3d0-148">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ec3d0-148">**Function**</span></span>|<span data-ttu-id="ec3d0-149">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ec3d0-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec3d0-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ec3d0-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ec3d0-151">"OpenProfileSection"</span><span class="sxs-lookup"><span data-stu-id="ec3d0-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="ec3d0-152">MFCMAPI (engl.) verwendet die **IProviderAdmin::OpenProfileSection** -Methode, um einen Profilabschnitt aus dem aktuellen Profil zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ec3d0-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec3d0-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec3d0-153">See also</span></span>



[<span data-ttu-id="ec3d0-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec3d0-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ec3d0-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ec3d0-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="ec3d0-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ec3d0-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ec3d0-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec3d0-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="ec3d0-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ec3d0-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


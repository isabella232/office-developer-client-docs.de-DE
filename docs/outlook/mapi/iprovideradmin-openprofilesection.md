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
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405660"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="14eae-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="14eae-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="14eae-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14eae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14eae-105">Öffnet einen Profil Abschnitt aus dem aktuellen Profil und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="14eae-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="14eae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14eae-106">Parameters</span></span>

 <span data-ttu-id="14eae-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="14eae-107">_lpUID_</span></span>
  
> <span data-ttu-id="14eae-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu öffnenden Profil Abschnitt enthält.</span><span class="sxs-lookup"><span data-stu-id="14eae-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="14eae-109">Clients dürfen keinen NULL-Wert für den _lpUID_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="14eae-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="14eae-110">Dienstanbieter können NULL zum Abrufen der **MAPIUID** -Funktion, wenn Sie über Ihre Message-Dienst-Einstiegspunkt-Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14eae-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="14eae-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="14eae-111">_lpInterface_</span></span>
  
> <span data-ttu-id="14eae-112">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den profile-Abschnitt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14eae-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="14eae-113">Übergeben von NULL Ergebnisse in der Profil Abschnitt Standardschnittstelle (**IProfSect**) wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14eae-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="14eae-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14eae-114">_ulFlags_</span></span>
  
> <span data-ttu-id="14eae-115">in Eine Bitmaske von Flags, die die Art des Öffnens des Profil Abschnitts steuert.</span><span class="sxs-lookup"><span data-stu-id="14eae-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="14eae-116">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="14eae-116">The following flags can be set:</span></span>
    
<span data-ttu-id="14eae-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="14eae-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="14eae-118">Ermöglicht es **OpenProfileSection** , erfolgreich zurückzugeben, möglicherweise, bevor der Profil Abschnitt vollständig für den Aufrufer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="14eae-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="14eae-119">Wenn der profile-Abschnitt nicht verfügbar ist, kann durch einen nachfolgenden Aufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="14eae-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="14eae-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="14eae-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="14eae-121">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="14eae-121">Requests read/write permission.</span></span> <span data-ttu-id="14eae-122">Standardmäßig werden Objekte mit Schreibschutz Berechtigung geöffnet, und Anrufer sollten nicht unter der Annahme arbeiten, dass die Berechtigung "Lese-/Schreibzugriff" erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="14eae-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="14eae-123">Clients dürfen keine Lese-/Schreibzugriff auf Anbieter Abschnitte des Profils haben.</span><span class="sxs-lookup"><span data-stu-id="14eae-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="14eae-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="14eae-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="14eae-125">Ermöglicht den Zugriff auf alle Profilabschnitte, auch im Besitz einzelner Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="14eae-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="14eae-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="14eae-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="14eae-127">Out Ein Zeiger auf einen Zeiger auf den Profil Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="14eae-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14eae-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14eae-128">Return value</span></span>

<span data-ttu-id="14eae-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="14eae-129">S_OK</span></span> 
  
> <span data-ttu-id="14eae-130">Der Profil Abschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="14eae-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="14eae-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="14eae-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="14eae-132">Es wurde versucht, einen schreibgeschützten Profil Abschnitt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="14eae-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="14eae-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="14eae-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="14eae-134">Der angeforderte Profil Abschnitt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="14eae-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14eae-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14eae-135">Remarks</span></span>

<span data-ttu-id="14eae-136">Mit der **IProviderAdmin:: OpenProfileSection** -Methode wird ein Profil Abschnitt geöffnet, in dem der Aufrufer Informationen lesen und möglicherweise Informationen in das aktive Profil schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="14eae-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="14eae-137">Clients können Profilabschnitte, die zu Anbietern gehören, nicht mithilfe der **OpenProfileSection** -Methode öffnen.</span><span class="sxs-lookup"><span data-stu-id="14eae-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="14eae-138">Mehrere Clients oder Dienstanbieter können gleichzeitig einen Profil Abschnitt mit Leseberechtigung öffnen.</span><span class="sxs-lookup"><span data-stu-id="14eae-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="14eae-139">Wenn jedoch ein Profil Abschnitt mit Lese-/Schreibzugriff geöffnet ist, können keine weiteren Aufrufe zum Öffnen des Abschnitts ausgeführt werden, unabhängig von der Art des Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="14eae-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="14eae-140">Wenn ein Profil Abschnitt mit schreibgeschützter Berechtigung geöffnet ist, schlägt ein nachfolgendes Aufrufen der Berechtigung Lese-/Schreibzugriff mit MAPI_E_NO_ACCESS fehl.</span><span class="sxs-lookup"><span data-stu-id="14eae-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="14eae-141">Wenn ein Abschnitt mit Lese-/Schreibzugriff-Berechtigung geöffnet ist, tritt ebenfalls ein Fehler bei einem nachfolgenden Aufruf der Berechtigung Read-Only auf.</span><span class="sxs-lookup"><span data-stu-id="14eae-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="14eae-142">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="14eae-142">Notes to callers</span></span>

<span data-ttu-id="14eae-143">Wenn Sie anfordern, dass **OpenProfileSection** einen nicht vorhandenen Profil Abschnitt öffnet, indem Sie MAPI_MODIFY in _ulFlags_ und eine unbekannte **MAPIUID** in _lpUID_übergeben, wird der profile-Abschnitt erstellt.</span><span class="sxs-lookup"><span data-stu-id="14eae-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="14eae-144">Wenn Sie **OpenProfileSection** einen nicht vorhandenen Abschnitt mit Schreibschutz Berechtigung öffnen möchten, wird MAPI_E_NOT_FOUND zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14eae-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="14eae-145">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="14eae-145">MFCMAPI reference</span></span>

<span data-ttu-id="14eae-146">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14eae-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="14eae-147">**Datei**</span><span class="sxs-lookup"><span data-stu-id="14eae-147">**File**</span></span>|<span data-ttu-id="14eae-148">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="14eae-148">**Function**</span></span>|<span data-ttu-id="14eae-149">**Comment**</span><span class="sxs-lookup"><span data-stu-id="14eae-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14eae-150">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="14eae-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="14eae-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="14eae-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="14eae-152">MFCMAPI verwendet die **IProviderAdmin:: OpenProfileSection** -Methode, um einen Profil Abschnitt aus dem aktuellen Profil zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="14eae-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14eae-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14eae-153">See also</span></span>



[<span data-ttu-id="14eae-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14eae-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="14eae-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="14eae-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="14eae-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="14eae-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="14eae-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14eae-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="14eae-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="14eae-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


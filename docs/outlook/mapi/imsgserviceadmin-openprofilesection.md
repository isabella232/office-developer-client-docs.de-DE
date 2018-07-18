---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792601"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="592af-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="592af-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="592af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="592af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="592af-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="592af-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="592af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="592af-106">Parameters</span></span>

 <span data-ttu-id="592af-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="592af-107">_lpUID_</span></span>
  
> <span data-ttu-id="592af-108">Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die im Profilabschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="592af-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="592af-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="592af-109">_lpInterface_</span></span>
  
> <span data-ttu-id="592af-110">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="592af-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="592af-111">Bei Übergabe von NULL erzeugt einen Zeiger auf die standard-Schnittstelle im Parameter _LppProfSect_ zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="592af-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="592af-112">Die standard-Schnittstelle für einen Profilabschnitt ist **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="592af-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="592af-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="592af-113">_ulFlags_</span></span>
  
> <span data-ttu-id="592af-114">[in] Eine Bitmaske der Flags, die Steuerung des Zugriffs auf die Benutzerprofildienst-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="592af-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="592af-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="592af-115">The following flags can be set:</span></span>
    
<span data-ttu-id="592af-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="592af-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="592af-117">Ermöglicht **"OpenProfileSection"** zurückgegeben wurde, ist möglicherweise vor dem Profil Abschnitt an den aufrufenden Client vollständig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="592af-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="592af-118">Wenn im Profilabschnitt nicht verfügbar ist, kann die nachfolgenden Aufrufen es ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="592af-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="592af-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="592af-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="592af-120">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="592af-120">Requests read/write permission.</span></span> <span data-ttu-id="592af-121">In der Standardeinstellung Profil Abschnitte mit Leseberechtigung geöffnet sind, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="592af-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="592af-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="592af-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="592af-123">Ermöglicht den Zugriff auf alle Abschnitte Profil, auch die einzelnen Dienstanbieter Besitz.</span><span class="sxs-lookup"><span data-stu-id="592af-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="592af-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="592af-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="592af-125">[out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="592af-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="592af-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="592af-126">Return value</span></span>

<span data-ttu-id="592af-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="592af-127">S_OK</span></span> 
  
> <span data-ttu-id="592af-128">Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="592af-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="592af-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="592af-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="592af-130">Es wurde versucht, Zugriff auf einen Profil für den Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="592af-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="592af-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="592af-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="592af-132">Abschnitt angeforderten Profile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="592af-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="592af-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="592af-133">Remarks</span></span>

<span data-ttu-id="592af-134">Die **IMsgServiceAdmin::OpenProfileSection** -Methode öffnet einen Profilabschnitt, ein Objekt, das die [IProfSect](iprofsectimapiprop.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="592af-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="592af-135">Profil Abschnitte dienen zum Lesen von Informationen aus und Schreiben von Informationen in das Sitzungsprofil.</span><span class="sxs-lookup"><span data-stu-id="592af-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="592af-136">**"OpenProfileSection"** kann nicht verwendet werden, öffnen Sie Profil Abschnitte Besitz einzelne-Dienstanbieter, es sei denn, MAPI_FORCE_ACCESS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="592af-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="592af-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="592af-137">Notes to callers</span></span>

<span data-ttu-id="592af-138">Mehrere Clients können mit Leseberechtigung Profile-Abschnitt öffnen, jedoch nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="592af-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="592af-139">Wenn ein anderer Client einen Profilabschnitt öffnen hat, dass Sie versuchen, die durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY öffnen, schlägt der Aufruf fehl MAPI_E_NO_ACCESS zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="592af-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="592af-140">Ein Vorgang zum schreibgeschützt öffnen schlägt fehl, wenn im Abschnitt zum Schreiben geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="592af-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="592af-141">Sie können einen Profilabschnitt erstellen, durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY und eine nicht vorhandene [MAPIUID](mapiuid.md) Struktur im _LpUID_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="592af-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="592af-142">Stellen Sie sicher, dass Sie MAPI_MODIFY angeben.</span><span class="sxs-lookup"><span data-stu-id="592af-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="592af-143">Wenn Sie die _LpUID_ So zeigen Sie auf eine nicht vorhandene **MAPIUID** festgelegt, und Verwenden der Standardzugriffsmodus schreibgeschützten **"OpenProfileSection"** festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl.</span><span class="sxs-lookup"><span data-stu-id="592af-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="592af-144">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="592af-144">MFCMAPI reference</span></span>

<span data-ttu-id="592af-145">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="592af-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="592af-146">**Datei**</span><span class="sxs-lookup"><span data-stu-id="592af-146">**File**</span></span>|<span data-ttu-id="592af-147">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="592af-147">**Function**</span></span>|<span data-ttu-id="592af-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="592af-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="592af-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="592af-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="592af-150">"OpenProfileSection"</span><span class="sxs-lookup"><span data-stu-id="592af-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="592af-151">MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::OpenProfileSection** -Methode, um einen Profilabschnitt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="592af-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="592af-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="592af-152">See also</span></span>



[<span data-ttu-id="592af-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="592af-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="592af-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="592af-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="592af-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="592af-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="592af-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="592af-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="592af-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="592af-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="592af-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="592af-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


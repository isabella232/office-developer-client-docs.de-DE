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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437112"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="8abaa-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8abaa-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="8abaa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8abaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8abaa-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="8abaa-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="8abaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8abaa-106">Parameters</span></span>

 <span data-ttu-id="8abaa-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="8abaa-107">_lpUID_</span></span>
  
> <span data-ttu-id="8abaa-108">Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Profil Abschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8abaa-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="8abaa-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8abaa-109">_lpInterface_</span></span>
  
> <span data-ttu-id="8abaa-110">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den profile-Abschnitt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8abaa-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="8abaa-111">Das übergeben von NULL führt zu einem Zeiger auf die Standardschnittstelle, die im _lppProfSect_ -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8abaa-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="8abaa-112">Die Standardschnittstelle für einen Profil Abschnitt ist **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="8abaa-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="8abaa-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8abaa-113">_ulFlags_</span></span>
  
> <span data-ttu-id="8abaa-114">in Eine Bitmaske von Flags, die den Zugriff auf den Profil Abschnitt steuern.</span><span class="sxs-lookup"><span data-stu-id="8abaa-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="8abaa-115">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8abaa-115">The following flags can be set:</span></span>
    
<span data-ttu-id="8abaa-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8abaa-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8abaa-117">Ermöglicht die erfolgreiche Rückgabe von **OpenProfileSection** , möglicherweise bevor der Profil Abschnitt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8abaa-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="8abaa-118">Wenn der profile-Abschnitt nicht verfügbar ist, kann durch einen nachfolgenden Aufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8abaa-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="8abaa-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8abaa-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8abaa-120">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="8abaa-120">Requests read/write permission.</span></span> <span data-ttu-id="8abaa-121">Standardmäßig werden Profilabschnitte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="8abaa-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="8abaa-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8abaa-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="8abaa-123">Ermöglicht den Zugriff auf alle Profilabschnitte, auch im Besitz einzelner Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8abaa-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="8abaa-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="8abaa-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="8abaa-125">Out Ein Zeiger auf einen Zeiger auf den Profil Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="8abaa-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8abaa-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8abaa-126">Return value</span></span>

<span data-ttu-id="8abaa-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8abaa-127">S_OK</span></span> 
  
> <span data-ttu-id="8abaa-128">Der Profil Abschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8abaa-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="8abaa-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8abaa-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8abaa-130">Es wurde versucht, auf einen Profil Abschnitt zuzugreifen, für den der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="8abaa-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="8abaa-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8abaa-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8abaa-132">Der angeforderte Profil Abschnitt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8abaa-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8abaa-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8abaa-133">Remarks</span></span>

<span data-ttu-id="8abaa-134">Die **IMsgServiceAdmin:: OpenProfileSection** -Methode öffnet einen Profil Abschnitt, ein Objekt, das die [IProfSect](iprofsectimapiprop.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8abaa-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="8abaa-135">Profilabschnitte dienen zum Lesen von Informationen und zum Schreiben von Informationen in das Sitzungsprofil.</span><span class="sxs-lookup"><span data-stu-id="8abaa-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="8abaa-136">**OpenProfileSection** kann nicht zum Öffnen von Profil Abschnitten verwendet werden, die einzelnen Dienstanbietern gehören, es sei denn, MAPI_FORCE_ACCESS wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="8abaa-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8abaa-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="8abaa-137">Notes to callers</span></span>

<span data-ttu-id="8abaa-138">Mehrere Clients können einen Profil Abschnitt mit Schreibschutz Berechtigung Öffnen, aber nur ein Client kann einen Profil Abschnitt mit Berechtigung zum Lesen/Schreiben öffnen.</span><span class="sxs-lookup"><span data-stu-id="8abaa-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="8abaa-139">Wenn ein anderer Client einen Profil Abschnitt geöffnet hat, den Sie durch Aufrufen von **OpenProfileSection** mit dem MAPI_MODIFY-Flag-Satz öffnen, schlägt der Aufruf fehl, und es wird MAPI_E_NO_ACCESS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8abaa-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="8abaa-140">Ein schreibgeschützter Öffnungsvorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8abaa-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="8abaa-141">Sie können einen Profil Abschnitt erstellen, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flag und einer nicht vorhandenen [MAPIUID](mapiuid.md) -Struktur im _lpUID_ -Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8abaa-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="8abaa-142">Stellen Sie sicher, dass Sie MAPI_MODIFY angeben.</span><span class="sxs-lookup"><span data-stu-id="8abaa-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="8abaa-143">Wenn Sie _lpUID_ so festlegen, dass auf ein nicht vorhandenes **MAPIUID** und **OpenProfileSection** auf den Standardzugriffs Modus schreibgeschützt festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl.</span><span class="sxs-lookup"><span data-stu-id="8abaa-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8abaa-144">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8abaa-144">MFCMAPI reference</span></span>

<span data-ttu-id="8abaa-145">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8abaa-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8abaa-146">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8abaa-146">**File**</span></span>|<span data-ttu-id="8abaa-147">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8abaa-147">**Function**</span></span>|<span data-ttu-id="8abaa-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8abaa-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8abaa-149">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="8abaa-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8abaa-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8abaa-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="8abaa-151">MFCMAPI verwendet die **IMsgServiceAdmin:: OpenProfileSection** -Methode, um einen Profil Abschnitt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8abaa-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8abaa-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8abaa-152">See also</span></span>



[<span data-ttu-id="8abaa-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8abaa-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8abaa-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8abaa-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="8abaa-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8abaa-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="8abaa-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8abaa-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8abaa-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8abaa-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="8abaa-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8abaa-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


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
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="d158d-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d158d-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="d158d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d158d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d158d-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="d158d-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="d158d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d158d-106">Parameters</span></span>

 <span data-ttu-id="d158d-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d158d-107">_lpUID_</span></span>
  
> <span data-ttu-id="d158d-108">Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den Profilabschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d158d-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="d158d-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d158d-109">_lpInterface_</span></span>
  
> <span data-ttu-id="d158d-110">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d158d-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="d158d-111">Das Übergeben von NULL führt dazu, dass ein Zeiger auf die Standardschnittstelle im  _lppProfSect-Parameter zurückgegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="d158d-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="d158d-112">Die Standardschnittstelle für einen Profilabschnitt ist **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="d158d-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="d158d-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d158d-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d158d-114">[in] Eine Bitmaske mit Flags, die den Zugriff auf den Profilabschnitt steuert.</span><span class="sxs-lookup"><span data-stu-id="d158d-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="d158d-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d158d-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d158d-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d158d-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d158d-117">Ermöglicht **openProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d158d-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="d158d-118">Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler zur Folge haben.</span><span class="sxs-lookup"><span data-stu-id="d158d-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="d158d-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d158d-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d158d-120">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="d158d-120">Requests read/write permission.</span></span> <span data-ttu-id="d158d-121">Standardmäßig werden Profilabschnitte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="d158d-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="d158d-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d158d-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="d158d-123">Ermöglicht den Zugriff auf alle Profilabschnitte, auch die, die im Besitz einzelner Dienstanbieter sind.</span><span class="sxs-lookup"><span data-stu-id="d158d-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="d158d-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="d158d-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="d158d-125">[out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d158d-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d158d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d158d-126">Return value</span></span>

<span data-ttu-id="d158d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="d158d-127">S_OK</span></span> 
  
> <span data-ttu-id="d158d-128">Der Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d158d-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="d158d-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d158d-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d158d-130">Es wurde versucht, auf einen Profilabschnitt zu zugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="d158d-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="d158d-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d158d-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d158d-132">Der angeforderte Profilabschnitt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d158d-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d158d-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d158d-133">Remarks</span></span>

<span data-ttu-id="d158d-134">Die **IMsgServiceAdmin::OpenProfileSection-Methode** öffnet einen Profilabschnitt, ein Objekt, das die [IProfSect-Schnittstelle](iprofsectimapiprop.md) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d158d-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="d158d-135">Profilabschnitte werden zum Lesen von Informationen aus dem Sitzungsprofil und zum Schreiben von Informationen in das Sitzungsprofil verwendet.</span><span class="sxs-lookup"><span data-stu-id="d158d-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="d158d-136">**OpenProfileSection** kann nicht zum Öffnen von Profilabschnitten verwendet werden, die im Besitz einzelner Dienstanbieter sind, es sei denn, MAPI_FORCE_ACCESS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d158d-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d158d-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d158d-137">Notes to callers</span></span>

<span data-ttu-id="d158d-138">Mehrere Clients können einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen, aber nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung öffnen.</span><span class="sxs-lookup"><span data-stu-id="d158d-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="d158d-139">Wenn ein anderer Client einen Profilabschnitt geöffnet hat, den Sie öffnen möchten, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flagsatz aufrufen, wird beim Aufruf ein Fehler ausgeführt, und MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="d158d-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="d158d-140">Ein schreibgeschützter offener Vorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d158d-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="d158d-141">Sie können einen Profilabschnitt erstellen, indem **Sie OpenProfileSection** mit dem flag MAPI_MODIFY und einer nicht vorhandenen [MAPIUID-Struktur](mapiuid.md) im  _lpUID-Parameter_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d158d-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="d158d-142">Stellen Sie sicher, dass Sie MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d158d-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="d158d-143">Wenn Sie  _lpUID_ so festlegen, dass sie auf eine nicht vorhandene **MAPIUID** zeigt und **OpenProfileSection** auf den Standardzugriffsmodus schreibgeschützt festgelegt ist, wird beim Aufruf ein Fehler MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="d158d-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d158d-144">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d158d-144">MFCMAPI reference</span></span>

<span data-ttu-id="d158d-145">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d158d-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d158d-146">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d158d-146">**File**</span></span>|<span data-ttu-id="d158d-147">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d158d-147">**Function**</span></span>|<span data-ttu-id="d158d-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d158d-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d158d-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d158d-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d158d-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d158d-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="d158d-151">MFCMAPI verwendet die **IMsgServiceAdmin::OpenProfileSection-Methode,** um einen Profilabschnitt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d158d-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d158d-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d158d-152">See also</span></span>



[<span data-ttu-id="d158d-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d158d-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d158d-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d158d-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="d158d-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d158d-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="d158d-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d158d-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d158d-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d158d-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="d158d-158">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d158d-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568189"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="58529-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="58529-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="58529-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58529-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff.</span><span class="sxs-lookup"><span data-stu-id="58529-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="58529-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58529-106">Parameters</span></span>

 <span data-ttu-id="58529-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="58529-107">_lpUID_</span></span>
  
> <span data-ttu-id="58529-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die im Profilabschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="58529-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="58529-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="58529-109">_lpInterface_</span></span>
  
> <span data-ttu-id="58529-110">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle zum Zugreifen auf den Profilabschnitt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58529-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="58529-111">Übergeben von NULL bewirkt, dass den Parameter _LppProfSect_ auf einen Zeiger auf das Profilabschnitt Standardschnittstelle, **IProfSect**zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="58529-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="58529-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58529-112">_ulFlags_</span></span>
  
> <span data-ttu-id="58529-113">[in] Eine Bitmaske der Flags, die Steuerung des Zugriffs auf die Benutzerprofildienst-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="58529-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="58529-114">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="58529-114">The following flags can be set:</span></span>
    
<span data-ttu-id="58529-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="58529-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="58529-116">Ermöglicht **"OpenProfileSection"** zurückgegeben wurde, ist möglicherweise vor dem Profil Abschnitt an den aufrufenden Client vollständig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58529-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="58529-117">Wenn der Profilabschnitt nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="58529-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="58529-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="58529-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="58529-119">Ermöglicht den Zugriff auf ein Profilabschnitt, der nicht an den Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="58529-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="58529-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="58529-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="58529-121">Anfragen Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="58529-121">Requests read/write permission.</span></span> <span data-ttu-id="58529-122">In der Standardeinstellung Profil Abschnitte mit Leseberechtigung geöffnet sind, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="58529-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="58529-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="58529-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="58529-124">[out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="58529-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58529-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="58529-125">Return value</span></span>

<span data-ttu-id="58529-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="58529-126">S_OK</span></span> 
  
> <span data-ttu-id="58529-127">Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="58529-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="58529-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="58529-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="58529-129">Es wurde versucht, Zugriff auf einen Profil für den Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="58529-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="58529-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="58529-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="58529-131">Abschnitt angeforderten Profile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="58529-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58529-132">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="58529-132">Remarks</span></span>

<span data-ttu-id="58529-133">Die **IMAPISession::OpenProfileSection** -Methode öffnet eine Benutzerprofilabschnitt oder ein Objekt, das die **IProfSect** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58529-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="58529-134">Profil Abschnitte dienen zum Lesen von Informationen aus und Schreiben von Informationen in das Sitzungsprofil.</span><span class="sxs-lookup"><span data-stu-id="58529-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="58529-135">Sie können **"OpenProfileSection"** Profil Abschnitte öffnen, einzelne eigenen Dienstanbieter, es sei denn, Sie MAPI_FORCE_ACCESS im _UlFlags_ -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="58529-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="58529-136">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="58529-136">Notes to callers</span></span>

<span data-ttu-id="58529-137">Mehrere Clients können mit Leseberechtigung Profile-Abschnitt öffnen, jedoch nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="58529-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="58529-138">Wenn ein anderer Client einen Profilabschnitt öffnen hat, dass Sie versuchen, die durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY öffnen, schlägt der Aufruf fehl MAPI_E_NO_ACCESS zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="58529-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="58529-139">Ein Vorgang zum schreibgeschützt öffnen schlägt fehl, wenn im Abschnitt zum Schreiben geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="58529-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="58529-140">Sie können einen Profilabschnitt erstellen, durch Aufrufen von **"OpenProfileSection"** mit dem Flag MAPI_MODIFY und eine nicht vorhandene **MAPIUID** Struktur im _LpUID_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="58529-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="58529-141">Stellen Sie sicher, dass Sie MAPI_MODIFY angeben.</span><span class="sxs-lookup"><span data-stu-id="58529-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="58529-142">Wenn Sie die _LpUID_ So zeigen Sie auf eine nicht vorhandene **MAPIUID** festgelegt, und Verwenden der Standardzugriffsmodus schreibgeschützten **"OpenProfileSection"** festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl.</span><span class="sxs-lookup"><span data-stu-id="58529-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58529-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58529-143">See also</span></span>



[<span data-ttu-id="58529-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58529-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="58529-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="58529-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="58529-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="58529-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="58529-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="58529-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


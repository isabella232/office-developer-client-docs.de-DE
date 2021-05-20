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
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439919"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="29670-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="29670-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="29670-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29670-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29670-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="29670-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="29670-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29670-106">Parameters</span></span>

 <span data-ttu-id="29670-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="29670-107">_lpUID_</span></span>
  
> <span data-ttu-id="29670-108">[in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den Profilabschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="29670-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="29670-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="29670-109">_lpInterface_</span></span>
  
> <span data-ttu-id="29670-110">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Profilabschnitt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29670-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="29670-111">Durch Übergeben von NULL gibt  _der lppProfSect-Parameter_ einen Zeiger auf die Standardschnittstelle des Profilabschnitts zurück, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="29670-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="29670-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29670-112">_ulFlags_</span></span>
  
> <span data-ttu-id="29670-113">[in] Eine Bitmaske mit Flags, die den Zugriff auf den Profilabschnitt steuert.</span><span class="sxs-lookup"><span data-stu-id="29670-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="29670-114">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="29670-114">The following flags can be set:</span></span>
    
<span data-ttu-id="29670-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="29670-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="29670-116">Ermöglicht **openProfileSection** die erfolgreiche Rückgabe, möglicherweise bevor der Profilabschnitt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="29670-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="29670-117">Wenn der Profilabschnitt nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="29670-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="29670-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="29670-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="29670-119">Ermöglicht den Zugriff auf einen Profilabschnitt, der nicht zum Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="29670-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="29670-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="29670-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="29670-121">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="29670-121">Requests read/write permission.</span></span> <span data-ttu-id="29670-122">Standardmäßig werden Profilabschnitte mit schreibgeschützter Berechtigung geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="29670-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="29670-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="29670-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="29670-124">[out] Ein Zeiger auf einen Zeiger auf den Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="29670-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29670-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29670-125">Return value</span></span>

<span data-ttu-id="29670-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="29670-126">S_OK</span></span> 
  
> <span data-ttu-id="29670-127">Der Profilabschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="29670-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="29670-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="29670-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="29670-129">Es wurde versucht, auf einen Profilabschnitt zu zugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="29670-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="29670-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="29670-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="29670-131">Der angeforderte Profilabschnitt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="29670-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29670-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29670-132">Remarks</span></span>

<span data-ttu-id="29670-133">Die **IMAPISession::OpenProfileSection-Methode** öffnet einen Profilabschnitt oder ein Objekt, das die **IProfSect-Schnittstelle** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29670-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="29670-134">Profilabschnitte werden zum Lesen von Informationen aus dem Sitzungsprofil und zum Schreiben von Informationen in das Sitzungsprofil verwendet.</span><span class="sxs-lookup"><span data-stu-id="29670-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="29670-135">Sie können **OpenProfileSection** nicht zum Öffnen von Profilabschnitten verwenden, die einzelne Dienstanbieter besitzen, es sei denn, Sie geben MAPI_FORCE_ACCESS  _ulFlags-Parameter_ an.</span><span class="sxs-lookup"><span data-stu-id="29670-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="29670-136">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="29670-136">Notes to callers</span></span>

<span data-ttu-id="29670-137">Mehrere Clients können einen Profilabschnitt mit schreibgeschützter Berechtigung öffnen, aber nur ein Client kann einen Profilabschnitt mit Lese-/Schreibberechtigung öffnen.</span><span class="sxs-lookup"><span data-stu-id="29670-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="29670-138">Wenn ein anderer Client einen Profilabschnitt geöffnet hat, den Sie öffnen möchten, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flagsatz aufrufen, wird beim Aufruf ein Fehler ausgeführt, und MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="29670-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="29670-139">Ein schreibgeschützter offener Vorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="29670-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="29670-140">Sie können einen Profilabschnitt erstellen, indem **Sie OpenProfileSection** mit dem flag MAPI_MODIFY und einer nicht vorhandenen **MAPIUID-Struktur** im  _lpUID-Parameter_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29670-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="29670-141">Stellen Sie sicher, dass Sie MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="29670-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="29670-142">Wenn Sie  _lpUID_ so festlegen, dass sie auf eine nicht vorhandene **MAPIUID** zeigt und **OpenProfileSection** auf den Standardzugriffsmodus schreibgeschützt festgelegt ist, wird beim Aufruf ein Fehler MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="29670-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="29670-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29670-143">See also</span></span>



[<span data-ttu-id="29670-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29670-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="29670-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="29670-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="29670-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="29670-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="29670-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29670-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


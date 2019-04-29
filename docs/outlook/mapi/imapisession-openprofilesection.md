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
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="0a181-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0a181-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="0a181-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a181-105">Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück.</span><span class="sxs-lookup"><span data-stu-id="0a181-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="0a181-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a181-106">Parameters</span></span>

 <span data-ttu-id="0a181-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0a181-107">_lpUID_</span></span>
  
> <span data-ttu-id="0a181-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Profil Abschnitt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0a181-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="0a181-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0a181-109">_lpInterface_</span></span>
  
> <span data-ttu-id="0a181-110">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den profile-Abschnitt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a181-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="0a181-111">Durch das Übergeben von NULL wird der _lppProfSect_ -Parameter zum Zurückgeben eines Zeigers auf die Standardschnittstelle des Profil Abschnitts **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="0a181-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="0a181-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0a181-112">_ulFlags_</span></span>
  
> <span data-ttu-id="0a181-113">in Eine Bitmaske von Flags, die den Zugriff auf den Profil Abschnitt steuern.</span><span class="sxs-lookup"><span data-stu-id="0a181-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="0a181-114">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0a181-114">The following flags can be set:</span></span>
    
<span data-ttu-id="0a181-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0a181-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0a181-116">Ermöglicht die erfolgreiche Rückgabe von **OpenProfileSection** , möglicherweise bevor der Profil Abschnitt vollständig für den aufrufenden Client verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0a181-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="0a181-117">Wenn der profile-Abschnitt nicht verfügbar ist, kann ein nachfolgendes aufrufen einen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="0a181-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0a181-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0a181-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="0a181-119">Ermöglicht den Zugriff auf einen Profil Abschnitt, der nicht zum Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="0a181-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="0a181-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0a181-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0a181-121">Fordert Lese-/Schreibzugriff-Berechtigung an.</span><span class="sxs-lookup"><span data-stu-id="0a181-121">Requests read/write permission.</span></span> <span data-ttu-id="0a181-122">Standardmäßig werden Profilabschnitte mit Schreibschutz Berechtigung geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="0a181-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="0a181-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="0a181-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="0a181-124">Out Ein Zeiger auf einen Zeiger auf den Profil Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="0a181-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0a181-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a181-125">Return value</span></span>

<span data-ttu-id="0a181-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a181-126">S_OK</span></span> 
  
> <span data-ttu-id="0a181-127">Der Profil Abschnitt wurde erfolgreich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0a181-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="0a181-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0a181-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0a181-129">Es wurde versucht, auf einen Profil Abschnitt zuzugreifen, für den der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0a181-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="0a181-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0a181-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0a181-131">Der angeforderte Profil Abschnitt ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0a181-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a181-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a181-132">Remarks</span></span>

<span data-ttu-id="0a181-133">Die **IMAPISession:: OpenProfileSection** -Methode öffnet einen Profil Abschnitt oder ein Objekt, das die **IProfSect** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a181-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="0a181-134">Profilabschnitte dienen zum Lesen von Informationen und zum Schreiben von Informationen in das Sitzungsprofil.</span><span class="sxs-lookup"><span data-stu-id="0a181-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="0a181-135">Sie können **OpenProfileSection** nicht verwenden, um Profilabschnitte zu öffnen, die einzelne Dienstanbieter besitzen, es sei denn, Sie geben MAPI_FORCE_ACCESS im _ulFlags_ -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="0a181-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0a181-136">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0a181-136">Notes to callers</span></span>

<span data-ttu-id="0a181-137">Mehrere Clients können einen Profil Abschnitt mit Schreibschutz Berechtigung Öffnen, aber nur ein Client kann einen Profil Abschnitt mit Berechtigung zum Lesen/Schreiben öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a181-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="0a181-138">Wenn ein anderer Client einen Profil Abschnitt geöffnet hat, den Sie durch Aufrufen von **OpenProfileSection** mit dem MAPI_MODIFY-Flag-Satz öffnen, schlägt der Aufruf fehl, und es wird MAPI_E_NO_ACCESS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a181-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="0a181-139">Ein schreibgeschützter Öffnungsvorgang schlägt fehl, wenn der Abschnitt zum Schreiben geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="0a181-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="0a181-140">Sie können einen Profil Abschnitt erstellen, indem Sie **OpenProfileSection** mit dem MAPI_MODIFY-Flag und einer nicht vorhandenen **MAPIUID** -Struktur im _lpUID_ -Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a181-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="0a181-141">Stellen Sie sicher, dass Sie MAPI_MODIFY angeben.</span><span class="sxs-lookup"><span data-stu-id="0a181-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="0a181-142">Wenn Sie _lpUID_ so festlegen, dass auf ein nicht vorhandenes **MAPIUID** und **OpenProfileSection** auf den Standardzugriffs Modus schreibgeschützt festgelegt ist, schlägt der Aufruf mit MAPI_E_NOT_FOUND fehl.</span><span class="sxs-lookup"><span data-stu-id="0a181-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a181-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a181-143">See also</span></span>



[<span data-ttu-id="0a181-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a181-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="0a181-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0a181-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="0a181-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0a181-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0a181-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a181-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


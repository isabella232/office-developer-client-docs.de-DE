---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792745"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="22f44-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="22f44-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="22f44-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22f44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22f44-105">Kopiert ein Profil.</span><span class="sxs-lookup"><span data-stu-id="22f44-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="22f44-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22f44-106">Parameters</span></span>

 <span data-ttu-id="22f44-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="22f44-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="22f44-108">[in] Ein Zeiger auf den Namen des Profils zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="22f44-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="22f44-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="22f44-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="22f44-110">[in] Ein Zeiger auf das Kennwort für das zu kopierende Profil.</span><span class="sxs-lookup"><span data-stu-id="22f44-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="22f44-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="22f44-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="22f44-112">[in] Ein Zeiger auf den neuen Namen der kopierten Profil.</span><span class="sxs-lookup"><span data-stu-id="22f44-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="22f44-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="22f44-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="22f44-114">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="22f44-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="22f44-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22f44-115">_ulFlags_</span></span>
  
> <span data-ttu-id="22f44-116">[in] Eine Bitmaske aus Flags, die steuert, wie das Profil kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="22f44-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="22f44-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="22f44-117">The following flags can be set:</span></span>
    
<span data-ttu-id="22f44-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="22f44-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="22f44-119">Zeigt ein Dialogfeld an, die der Benutzer für das korrekte Kennwort des Profils kopieren kann.</span><span class="sxs-lookup"><span data-stu-id="22f44-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="22f44-120">Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22f44-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22f44-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22f44-121">Return value</span></span>

<span data-ttu-id="22f44-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="22f44-122">S_OK</span></span> 
  
> <span data-ttu-id="22f44-123">Das Profil wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="22f44-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="22f44-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="22f44-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="22f44-125">Der neue Profilname ist identisch mit der eines vorhandenen Profils.</span><span class="sxs-lookup"><span data-stu-id="22f44-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="22f44-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="22f44-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="22f44-127">Das Kennwort für das zu kopierende Profil ist falsch, und ein Dialogfeld konnte nicht angezeigt werden, die dem Benutzer das korrekte Kennwort anfordern, da MAPI_DIALOG im _UlFlags_ -Parameter nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="22f44-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="22f44-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="22f44-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="22f44-129">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="22f44-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="22f44-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="22f44-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="22f44-131">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="22f44-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22f44-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22f44-132">Remarks</span></span>

<span data-ttu-id="22f44-133">Mit dem **IProfAdmin::CopyProfile** -Methode wird eine Kopie des Profils, auf die _LpszOldProfileName_, unter dem Namen mit _LpszNewProfileName_gezeigt.</span><span class="sxs-lookup"><span data-stu-id="22f44-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="22f44-134">Kopieren eines Profils bewirkt, dass die Kopie mit das gleiche Kennwort wie das Original.</span><span class="sxs-lookup"><span data-stu-id="22f44-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="22f44-135">Der Name der ursprünglichen Profil, das Kennwort und die Kopie kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="22f44-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="22f44-136">Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="22f44-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="22f44-137">Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="22f44-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="22f44-138">Profil Kennwörter werden auf allen Betriebssystemen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22f44-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="22f44-139">Unter Betriebssystemen, die keine für Profil Kennwörter Unterstützung, kann _LpszOldPassword_ NULL oder einen Zeiger auf eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="22f44-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="22f44-140">Wenn _LpszOldPassword_ auf NULL festgelegt ist, das Profil zu kopierenden erfordert ein Kennwort und das Flag MAPI_DIALOG festgelegt ist. Dialogfeld, in dem der Benutzer das Kennwort angeben, kann wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22f44-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="22f44-141">Wenn ein Kennwort erforderlich ist, aber _LpszOldPassword_ auf NULL festgelegt ist, und das Flag MAPI_DIALOG nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED zurück.</span><span class="sxs-lookup"><span data-stu-id="22f44-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22f44-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22f44-142">See also</span></span>



[<span data-ttu-id="22f44-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22f44-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


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
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437238"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="6b1eb-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="6b1eb-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="6b1eb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b1eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b1eb-105">Kopiert ein Profil.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6b1eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b1eb-106">Parameters</span></span>

 <span data-ttu-id="6b1eb-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="6b1eb-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="6b1eb-108">[in] Ein Zeiger auf den Namen des zu kopierende Profils.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="6b1eb-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="6b1eb-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="6b1eb-110">[in] Ein Zeiger auf das Kennwort des zu kopierende Profils.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="6b1eb-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="6b1eb-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="6b1eb-112">[in] Ein Zeiger auf den neuen Namen des kopierten Profils.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="6b1eb-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6b1eb-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6b1eb-114">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="6b1eb-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b1eb-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6b1eb-116">[in] Eine Bitmaske mit Flags, die steuert, wie das Profil kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="6b1eb-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6b1eb-117">The following flags can be set:</span></span>
    
<span data-ttu-id="6b1eb-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6b1eb-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6b1eb-119">Zeigt ein Dialogfeld an, in dem der Benutzer zum richtigen Kennwort des zu kopierenden Profils aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="6b1eb-120">Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b1eb-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b1eb-121">Return value</span></span>

<span data-ttu-id="6b1eb-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b1eb-122">S_OK</span></span> 
  
> <span data-ttu-id="6b1eb-123">Das Profil wurde erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="6b1eb-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="6b1eb-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="6b1eb-125">Der neue Profilname ist identisch mit dem eines vorhandenen Profils.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="6b1eb-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="6b1eb-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="6b1eb-127">Das Kennwort für das zu kopierende Profil ist falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzugeben, da MAPI_DIALOG nicht im  _ulFlags-Parameter festgelegt_ wurde.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="6b1eb-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6b1eb-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6b1eb-129">Das angegebene Profil ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="6b1eb-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6b1eb-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6b1eb-131">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b1eb-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b1eb-132">Remarks</span></span>

<span data-ttu-id="6b1eb-133">Die **IProfAdmin::CopyProfile-Methode** erstellt eine Kopie des Profils, auf das _von lpszOldProfileName_ verwiesen wird, und gibt ihm den Namen, auf den _lpszNewProfileName verweist._</span><span class="sxs-lookup"><span data-stu-id="6b1eb-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="6b1eb-134">Beim Kopieren eines Profils bleibt die Kopie mit demselben Kennwort wie das Original erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="6b1eb-135">Der Name des ursprünglichen Profils, sein Kennwort und die Kopie können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="6b1eb-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="6b1eb-136">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="6b1eb-137">Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="6b1eb-138">Profilkennwörter werden nicht auf allen Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="6b1eb-139">Auf Betriebssystemen, die keine Profilkennwörter unterstützen,  _kann lpszOldPassword_ NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="6b1eb-140">Wenn  _lpszOldPassword_ auf NULL festgelegt ist, erfordert das zu kopierende Profil ein Kennwort, und das MAPI_DIALOG ist festgelegt. Ein Dialogfeld, in dem der Benutzer zur Eingabe des Kennworts aufgefordert wird, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="6b1eb-141">Wenn ein Kennwort erforderlich ist,  _lpszOldPassword_ jedoch auf NULL festgelegt ist und das MAPI_DIALOG nicht festgelegt ist, gibt **CopyProfile** MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="6b1eb-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b1eb-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b1eb-142">See also</span></span>



[<span data-ttu-id="6b1eb-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b1eb-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


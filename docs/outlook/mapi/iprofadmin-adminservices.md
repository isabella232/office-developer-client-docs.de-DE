---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309597"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="a0c6d-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="a0c6d-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="a0c6d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0c6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0c6d-105">Ermöglicht den Zugriff auf ein Nachrichtendienst-Verwaltungsobjekt zum vornehmen von Änderungen an den Nachrichtendiensten in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="a0c6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0c6d-106">Parameters</span></span>

 <span data-ttu-id="a0c6d-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="a0c6d-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="a0c6d-108">in Ein Zeiger auf den Namen des zu ändernden Profils.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="a0c6d-109">Der _lpszProfileName_ -Parameter darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="a0c6d-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="a0c6d-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="a0c6d-111">in Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="a0c6d-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a0c6d-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="a0c6d-113">in Ein Handle des übergeordneten Fensters für alle von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a0c6d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0c6d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="a0c6d-115">in Eine Bitmaske von Flags, die das Abrufen des Nachrichtendienst-Verwaltungsobjekts steuert.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="a0c6d-116">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a0c6d-116">The following flags can be set:</span></span>
    
<span data-ttu-id="a0c6d-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a0c6d-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a0c6d-118">Ermöglicht die Anzeige einer Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="a0c6d-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0c6d-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a0c6d-120">Der Profilname ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="a0c6d-121">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Name im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="a0c6d-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="a0c6d-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="a0c6d-123">Out Ein Zeiger auf einen Zeiger auf ein Nachrichtendienst-Verwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0c6d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0c6d-124">Return value</span></span>

<span data-ttu-id="a0c6d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0c6d-125">S_OK</span></span> 
  
> <span data-ttu-id="a0c6d-126">Das Nachrichtendienst-Verwaltungsobjekt wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="a0c6d-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="a0c6d-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="a0c6d-128">Das angegebene Profil ist nicht vorhanden, oder das Kennwort war falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzufordern, da MAPI_DIALOG in _ulFlags_nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="a0c6d-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a0c6d-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a0c6d-130">Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0c6d-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0c6d-131">Remarks</span></span>

<span data-ttu-id="a0c6d-132">Die **IProfAdmin:: AdminServices** -Methode ermöglicht den Zugriff auf ein Nachrichtendienst-Verwaltungsobjekt, um Konfigurationsänderungen an den Nachrichtendiensten in einem Profil vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="a0c6d-133">Der _lpszPassword_ -Parameter muss NULL oder ein Zeiger auf eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0c6d-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="a0c6d-134">Notes to callers</span></span>

<span data-ttu-id="a0c6d-135">Obwohl Sie einen [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Zeiger abrufen können, indem Sie entweder diese Methode oder [IMAPISession:: AdminServices](imapisession-adminservices.md)aufrufen, rufen Sie **IProfAdmin:: AdminServices** auf, wenn Sie streng einen Konfigurations Client haben und keine Messagingfunktionen anbieten.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="a0c6d-136">**IProfAdmin:: AdminServices** erstellt kein Sitzungsobjekt und lädt keine Dienstanbieter, wodurch die Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="a0c6d-137">Sie können **IProfAdmin:: AdminServices** nicht zum Erstellen eines Profils verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="a0c6d-138">Daher müssen Sie ein vorhandenes gültiges Profil in _lpszProfileName_angeben.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="a0c6d-139">Wenn das angegebene Profil nicht vorhanden ist, gibt **IProfAdmin:: ADMINSERVICES** MAPI_E_LOGON_FAILED zurück.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="a0c6d-140">Der Name des Profils kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="a0c6d-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="a0c6d-141">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und der Unterstrich.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="a0c6d-142">Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a0c6d-143">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a0c6d-143">MFCMAPI reference</span></span>

<span data-ttu-id="a0c6d-144">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a0c6d-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a0c6d-145">**File**</span></span>|<span data-ttu-id="a0c6d-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a0c6d-146">**Function**</span></span>|<span data-ttu-id="a0c6d-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a0c6d-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0c6d-148">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="a0c6d-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="a0c6d-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="a0c6d-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="a0c6d-150">MFCMAPI verwendet die **IProfAdmin:: AdminServices** -Methode, um ein Nachrichtendienst-Verwaltungsobjekt für das ausgewählte Profil zum Hinzufügen von Diensten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a0c6d-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0c6d-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0c6d-151">See also</span></span>



[<span data-ttu-id="a0c6d-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="a0c6d-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="a0c6d-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0c6d-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="a0c6d-154">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a0c6d-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


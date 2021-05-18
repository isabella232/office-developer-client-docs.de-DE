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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422082"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="1b8da-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="1b8da-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="1b8da-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b8da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b8da-105">Bietet Zugriff auf ein Nachrichtendienstverwaltungsobjekt zum Vornehmen von Änderungen an den Nachrichtendiensten in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="1b8da-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="1b8da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b8da-106">Parameters</span></span>

 <span data-ttu-id="1b8da-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1b8da-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1b8da-108">[in] Ein Zeiger auf den Namen des zu ändernde Profils.</span><span class="sxs-lookup"><span data-stu-id="1b8da-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="1b8da-109">Der  _lpszProfileName-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1b8da-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="1b8da-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="1b8da-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="1b8da-111">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="1b8da-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="1b8da-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1b8da-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="1b8da-113">[in] Ein Handle des übergeordneten Fensters für alle Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1b8da-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="1b8da-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b8da-114">_ulFlags_</span></span>
  
> <span data-ttu-id="1b8da-115">[in] Eine Bitmaske mit Flags, die den Abruf des Nachrichtendienstverwaltungsobjekts steuert.</span><span class="sxs-lookup"><span data-stu-id="1b8da-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="1b8da-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1b8da-116">The following flags can be set:</span></span>
    
<span data-ttu-id="1b8da-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1b8da-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="1b8da-118">Aktiviert die Anzeige einer Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1b8da-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="1b8da-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b8da-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1b8da-120">Der Profilname ist im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="1b8da-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="1b8da-121">Wenn das MAPI_UNICODE nicht festgelegt ist, ist der Name im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="1b8da-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="1b8da-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="1b8da-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="1b8da-123">[out] Ein Zeiger auf einen Zeiger auf ein Nachrichtendienstverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1b8da-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b8da-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b8da-124">Return value</span></span>

<span data-ttu-id="1b8da-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b8da-125">S_OK</span></span> 
  
> <span data-ttu-id="1b8da-126">Das Nachrichtendienstverwaltungsobjekt wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b8da-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="1b8da-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="1b8da-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="1b8da-128">Das angegebene Profil ist nicht vorhanden, oder das Kennwort war falsch, und dem Benutzer konnte kein Dialogfeld angezeigt werden, um das richtige Kennwort anzugeben, da MAPI_DIALOG nicht in  _ulFlags_ festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1b8da-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="1b8da-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1b8da-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1b8da-130">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="1b8da-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1b8da-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b8da-131">Remarks</span></span>

<span data-ttu-id="1b8da-132">Die **IProfAdmin::AdminServices-Methode** bietet Zugriff auf ein Nachrichtendienstverwaltungsobjekt zum Vornehmen von Konfigurationsänderungen an den Nachrichtendiensten in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="1b8da-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="1b8da-133">Der  _lpszPassword-Parameter_ muss NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein.</span><span class="sxs-lookup"><span data-stu-id="1b8da-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b8da-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1b8da-134">Notes to callers</span></span>

<span data-ttu-id="1b8da-135">Obwohl Sie einen [IMsgServiceAdmin-Zeiger](imsgserviceadminiunknown.md) abrufen können, indem Sie entweder diese Methode oder [IMAPISession::AdminServices](imapisession-adminservices.md)aufrufen, rufen Sie **IProfAdmin::AdminServices** auf, wenn Sie nur über einen Konfigurationsclient verfügen und keine Messagingfeatures anbieten.</span><span class="sxs-lookup"><span data-stu-id="1b8da-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="1b8da-136">**IProfAdmin::AdminServices** erstellt kein Sitzungsobjekt und geladen keine Dienstanbieter, wodurch die Leistung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="1b8da-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="1b8da-137">Sie können **IProfAdmin::AdminServices** nicht zum Erstellen eines Profils verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b8da-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="1b8da-138">Daher müssen Sie ein vorhandenes gültiges Profil in _lpszProfileName angeben._</span><span class="sxs-lookup"><span data-stu-id="1b8da-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="1b8da-139">Wenn das angegebene Profil nicht vorhanden ist, gibt **IProfAdmin::AdminServices** MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="1b8da-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="1b8da-140">Der Name des Profils kann bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="1b8da-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="1b8da-141">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="1b8da-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="1b8da-142">Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="1b8da-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b8da-143">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1b8da-143">MFCMAPI reference</span></span>

<span data-ttu-id="1b8da-144">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1b8da-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b8da-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1b8da-145">**File**</span></span>|<span data-ttu-id="1b8da-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1b8da-146">**Function**</span></span>|<span data-ttu-id="1b8da-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1b8da-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b8da-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1b8da-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="1b8da-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="1b8da-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="1b8da-150">MFCMAPI verwendet die **IProfAdmin::AdminServices-Methode,** um ein Nachrichtendienstverwaltungsobjekt für das ausgewählte Profil zum Hinzufügen von Diensten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1b8da-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b8da-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b8da-151">See also</span></span>



[<span data-ttu-id="1b8da-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="1b8da-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="1b8da-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b8da-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="1b8da-154">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1b8da-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


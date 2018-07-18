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
ms.openlocfilehash: 7566bb075c2ef9903b5a376fd90f209c8683c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792757"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="fcfff-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="fcfff-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="fcfff-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fcfff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fcfff-105">Bietet Zugriff auf ein Objekt "Message" Service Administration für die Änderung der Nachrichtendienste in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="fcfff-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="fcfff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcfff-106">Parameters</span></span>

 <span data-ttu-id="fcfff-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="fcfff-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="fcfff-108">[in] Ein Zeiger auf den Namen des Profils geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcfff-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="fcfff-109">Der Parameter _LpszProfileName_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="fcfff-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="fcfff-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="fcfff-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="fcfff-111">[in] Immer NULL.</span><span class="sxs-lookup"><span data-stu-id="fcfff-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="fcfff-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fcfff-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="fcfff-113">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fcfff-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="fcfff-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fcfff-114">_ulFlags_</span></span>
  
> <span data-ttu-id="fcfff-115">[in] Eine Bitmaske aus Flags, die das Abrufen des Message Service Administration-Objekts steuert.</span><span class="sxs-lookup"><span data-stu-id="fcfff-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="fcfff-116">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fcfff-116">The following flags can be set:</span></span>
    
<span data-ttu-id="fcfff-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="fcfff-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="fcfff-118">Ermöglicht die Anzeige einer Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="fcfff-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="fcfff-119">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fcfff-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fcfff-120">Der Name der Benutzerprofildienst wird im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fcfff-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="fcfff-121">Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fcfff-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="fcfff-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="fcfff-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="fcfff-123">[out] Ein Zeiger auf einen Zeiger auf ein Objekt "Message" Service-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="fcfff-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcfff-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="fcfff-124">Return value</span></span>

<span data-ttu-id="fcfff-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcfff-125">S_OK</span></span> 
  
> <span data-ttu-id="fcfff-126">Das Objekt "Message" Service Administration wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcfff-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="fcfff-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="fcfff-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="fcfff-128">Das angegebene Profil ist nicht vorhanden, oder das Kennwort war falsch und ein Dialogfeld konnte nicht angezeigt werden, die dem Benutzer das korrekte Kennwort anfordern, da MAPI_DIALOG in _UlFlags_nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fcfff-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="fcfff-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="fcfff-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="fcfff-130">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fcfff-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fcfff-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcfff-131">Remarks</span></span>

<span data-ttu-id="fcfff-132">Die **IProfAdmin::AdminServices** -Methode ermöglicht den Zugriff auf ein Objekt "Message" Service Administration für die Änderung der Konfiguration der Nachrichtendienste in einem Profil.</span><span class="sxs-lookup"><span data-stu-id="fcfff-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="fcfff-133">Der Parameter _LpszPassword_ muss NULL oder einen Zeiger auf eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fcfff-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fcfff-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="fcfff-134">Notes to callers</span></span>

<span data-ttu-id="fcfff-135">Obwohl Sie einen Zeiger [IMsgServiceAdmin](imsgserviceadminiunknown.md) durch Aufrufen dieser Methode oder [IMAPISession::AdminServices](imapisession-adminservices.md)abrufen können, rufen Sie **IProfAdmin::AdminServices** , wenn Sie unbedingt einen Konfiguration-Client und keine Messagingfeatures bieten.</span><span class="sxs-lookup"><span data-stu-id="fcfff-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="fcfff-136">**IProfAdmin::AdminServices** erstellt ein Session-Objekt keine und lädt keine Dienstanbieter, die Leistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="fcfff-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="fcfff-137">Sie können keine **IProfAdmin::AdminServices** verwenden Sie zum Erstellen eines Profils.</span><span class="sxs-lookup"><span data-stu-id="fcfff-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="fcfff-138">Daher müssen Sie ein vorhandenes Profil gültiges in _LpszProfileName_angeben.</span><span class="sxs-lookup"><span data-stu-id="fcfff-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="fcfff-139">Wenn das angegebene Profil nicht vorhanden ist, gibt **IProfAdmin::AdminServices** MAPI_E_LOGON_FAILED zurück.</span><span class="sxs-lookup"><span data-stu-id="fcfff-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="fcfff-140">Der Name des Profils kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="fcfff-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="fcfff-141">Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="fcfff-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="fcfff-142">Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="fcfff-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="fcfff-143">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="fcfff-143">MFCMAPI reference</span></span>

<span data-ttu-id="fcfff-144">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fcfff-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fcfff-145">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fcfff-145">**File**</span></span>|<span data-ttu-id="fcfff-146">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fcfff-146">**Function**</span></span>|<span data-ttu-id="fcfff-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fcfff-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcfff-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fcfff-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="fcfff-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="fcfff-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="fcfff-150">MFCMAPI (engl.) wird die **IProfAdmin::AdminServices** -Methode verwendet, um eine Nachricht Service Administration-Objekt für das ausgewählte Profil Dienste hinzufügen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fcfff-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcfff-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcfff-151">See also</span></span>



[<span data-ttu-id="fcfff-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="fcfff-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="fcfff-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcfff-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="fcfff-154">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fcfff-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


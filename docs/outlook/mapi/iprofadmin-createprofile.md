---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404400"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="c393e-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="c393e-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="c393e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c393e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c393e-105">Erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="c393e-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c393e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c393e-106">Parameters</span></span>

 <span data-ttu-id="c393e-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="c393e-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="c393e-108">[in] Ein Zeiger auf den Namen des neuen Profils.</span><span class="sxs-lookup"><span data-stu-id="c393e-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="c393e-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="c393e-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="c393e-110">[in] Ein Zeiger auf das Kennwort des neuen Profils.</span><span class="sxs-lookup"><span data-stu-id="c393e-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="c393e-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c393e-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="c393e-112">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c393e-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="c393e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c393e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="c393e-114">[in] Eine Bitmaske mit Flags, die steuert, wie das Profil erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c393e-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="c393e-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c393e-115">The following flags can be set:</span></span>
    
<span data-ttu-id="c393e-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="c393e-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="c393e-117">MAPI sollte das neue Profil mit den Nachrichtendiensten auffüllen, die im Abschnitt [Standarddienste] der Datei Mapisvc.inf enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c393e-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="c393e-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c393e-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="c393e-119">Die Konfigurationseigenschaftsblätter der einzelnen Anbieter in den zu hinzufügende Nachrichtendiensten können angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c393e-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c393e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c393e-120">Return value</span></span>

<span data-ttu-id="c393e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c393e-121">S_OK</span></span> 
  
> <span data-ttu-id="c393e-122">Das neue Profil wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="c393e-122">The new profile was created.</span></span>
    
<span data-ttu-id="c393e-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c393e-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c393e-124">Das angegebene neue Profil ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c393e-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c393e-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c393e-125">Remarks</span></span>

<span data-ttu-id="c393e-126">Die **IProfAdmin::CreateProfile-Methode** erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="c393e-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c393e-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c393e-127">Notes to callers</span></span>

<span data-ttu-id="c393e-128">Sie können **CreateProfile zur** Installationszeit der Anwendung oder jederzeit während einer Sitzung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c393e-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="c393e-129">Wenn diese Methode bei der Installation aufgerufen wird, stammen viele der Konfigurationseinstellungen aus der Konfigurationsdatei Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="c393e-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="c393e-130">Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen vom Benutzer, der über eine Reihe von Eigenschaftenblättern aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="c393e-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="c393e-131">Wenn das MAPI_DEFAULT_SERVICES im  _ulFlags-Parameter_ festgelegt ist, ruft **CreateProfile** die Nachrichtendienst-Einstiegspunktfunktion für jeden Nachrichtendienst im Abschnitt [Standarddienste] in der Datei Mapisvc.inf auf.</span><span class="sxs-lookup"><span data-stu-id="c393e-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="c393e-132">Jede Nachrichtendienst-Einstiegspunktfunktion wird aufgerufen, wenn der  _ulContext-Parameter_ auf MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="c393e-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="c393e-133">Wenn sowohl die MAPI_DIALOG als auch MAPI_DEFAULT_SERVICES festgelegt sind, werden die Werte in den  _Parametern ulUIParam_ und  _ulFlags_ ebenfalls an die Einstiegspunktfunktion des Nachrichtendiensts übergeben.</span><span class="sxs-lookup"><span data-stu-id="c393e-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="c393e-134">Die Nachrichtendienst-Einstiegspunktfunktionen werden nur aufgerufen, nachdem dem Profil alle verfügbaren Informationen aus der Datei Mapisvc.inf hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c393e-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="c393e-135">Der Name des neuen Profils und sein Kennwort können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="c393e-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="c393e-136">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="c393e-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="c393e-137">Eingebettete Leerzeichen, jedoch keine führenden oder nachgestellten Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="c393e-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="c393e-138">Der  _lpszPassword-Parameter_ muss NULL oder ein Zeiger auf eine Zeichenfolge mit null Länge sein.</span><span class="sxs-lookup"><span data-stu-id="c393e-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c393e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c393e-139">See also</span></span>



[<span data-ttu-id="c393e-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="c393e-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="c393e-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="c393e-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="c393e-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c393e-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c393e-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c393e-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


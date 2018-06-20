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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a15561a6f3af35c1c7c2285bb6252e6400e0e8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792751"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="b7100-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="b7100-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="b7100-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7100-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7100-105">Erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="b7100-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b7100-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7100-106">Parameters</span></span>

 <span data-ttu-id="b7100-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="b7100-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="b7100-108">[in] Ein Zeiger auf den Namen des neuen Profils.</span><span class="sxs-lookup"><span data-stu-id="b7100-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="b7100-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="b7100-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="b7100-110">[in] Ein Zeiger auf das Kennwort für das neue Profil.</span><span class="sxs-lookup"><span data-stu-id="b7100-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="b7100-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b7100-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="b7100-112">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b7100-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="b7100-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7100-113">_ulFlags_</span></span>
  
> <span data-ttu-id="b7100-114">[in] Eine Bitmaske aus Flags, die steuert, wie das Profil erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b7100-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="b7100-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b7100-115">The following flags can be set:</span></span>
    
<span data-ttu-id="b7100-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="b7100-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="b7100-117">MAPI sollte das neue Profil mit den Diensten Nachricht aufgefüllt, die in der die Datei "Mapisvc.inf" im Abschnitt [Default Services] enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b7100-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="b7100-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b7100-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b7100-119">Konfigurationsblätter-Eigenschaft der einzelnen die Rollenanbieter in der Nachrichtendienste hinzugefügt werden soll, können angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7100-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b7100-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b7100-120">Return value</span></span>

<span data-ttu-id="b7100-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7100-121">S_OK</span></span> 
  
> <span data-ttu-id="b7100-122">Das neue Profil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7100-122">The new profile was created.</span></span>
    
<span data-ttu-id="b7100-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b7100-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b7100-124">Das angegebene neue Profil ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b7100-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7100-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7100-125">Remarks</span></span>

<span data-ttu-id="b7100-126">Die **IProfAdmin::CreateProfile** -Methode erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="b7100-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7100-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b7100-127">Notes to callers</span></span>

<span data-ttu-id="b7100-128">Sie können **CreateProfile** bei der Installation oder können Sie jederzeit während einer Sitzung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b7100-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="b7100-129">Bei der Installation diese Methode aufgerufen wird, werden viele der Konfigurationseinstellungen für die aus der Konfigurationsdatei Mapisvc.inf Vordergrund angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7100-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="b7100-130">Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen der Benutzer, der durch eine Reihe von Eigenschaftenseiten aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="b7100-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="b7100-131">Wenn das Flag MAPI_DEFAULT_SERVICES im _UlFlags_ -Parameter festgelegt ist, ruft **CreateProfile** die Nachricht Service Eintrag-Funktion für jeden Nachrichtendienst im Abschnitt [Default Services] in der Datei "Mapisvc.inf".</span><span class="sxs-lookup"><span data-stu-id="b7100-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="b7100-132">Jede Nachricht Service Eintrag Point-Funktion wird mit der _UlContext_ -Parameter auf MSG_SERVICE_CREATE aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b7100-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="b7100-133">Wenn die MAPI_DIALOG und die MAPI_DEFAULT_SERVICES Flags festgelegt sind, werden die Werte in den _UlUIParam_ und _UlFlags_ auch an die Nachricht Service Eintrag-Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="b7100-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="b7100-134">Die Nachricht Service Entry Point-Funktionen werden aufgerufen, nur, nachdem alle verfügbaren Informationen aus der Datei "Mapisvc.inf" auf das Profil hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7100-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="b7100-135">Der Name der dem neuen Profil und das zugehörige Kennwort kann bis zu 64 Zeichen lang sein und kann die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="b7100-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="b7100-136">Alle alphanumerischen Zeichen, einschließlich Akzent-Zeichen und das Unterstrichzeichen.</span><span class="sxs-lookup"><span data-stu-id="b7100-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="b7100-137">Leerzeichen, jedoch nicht führende oder nachfolgende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="b7100-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="b7100-138">Der Parameter _LpszPassword_ muss NULL oder einen Zeiger auf eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b7100-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7100-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7100-139">See also</span></span>



[<span data-ttu-id="b7100-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="b7100-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="b7100-141">IMsgServiceAdmin:: CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="b7100-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="b7100-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="b7100-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="b7100-143">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7100-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


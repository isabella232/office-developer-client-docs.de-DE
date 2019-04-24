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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317115"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="6aa46-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="6aa46-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="6aa46-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6aa46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6aa46-105">Erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="6aa46-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6aa46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6aa46-106">Parameters</span></span>

 <span data-ttu-id="6aa46-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6aa46-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6aa46-108">in Ein Zeiger auf den Namen des neuen Profils.</span><span class="sxs-lookup"><span data-stu-id="6aa46-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="6aa46-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="6aa46-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="6aa46-110">in Ein Zeiger auf das Kennwort des neuen Profils.</span><span class="sxs-lookup"><span data-stu-id="6aa46-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="6aa46-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6aa46-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="6aa46-112">in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="6aa46-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="6aa46-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6aa46-113">_ulFlags_</span></span>
  
> <span data-ttu-id="6aa46-114">in Eine Bitmaske von Flags, die die Erstellung des Profils steuert.</span><span class="sxs-lookup"><span data-stu-id="6aa46-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="6aa46-115">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6aa46-115">The following flags can be set:</span></span>
    
<span data-ttu-id="6aa46-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="6aa46-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="6aa46-117">MAPI sollte das neue Profil mit den Nachrichtendiensten auffüllen, die im Abschnitt [Default Services] der Datei MAPISVC. inf enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6aa46-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="6aa46-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6aa46-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6aa46-119">Die Konfigurationseigenschaften Blätter der einzelnen Anbieter in den Nachrichtendiensten, die hinzugefügt werden sollen, können angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6aa46-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6aa46-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6aa46-120">Return value</span></span>

<span data-ttu-id="6aa46-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6aa46-121">S_OK</span></span> 
  
> <span data-ttu-id="6aa46-122">Das neue Profil wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="6aa46-122">The new profile was created.</span></span>
    
<span data-ttu-id="6aa46-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6aa46-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6aa46-124">Das angegebene neue Profil ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6aa46-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6aa46-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6aa46-125">Remarks</span></span>

<span data-ttu-id="6aa46-126">Die **IProfAdmin::** CreateProfile-Methode erstellt ein neues Profil.</span><span class="sxs-lookup"><span data-stu-id="6aa46-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6aa46-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6aa46-127">Notes to callers</span></span>

<span data-ttu-id="6aa46-128">Sie können **CreateProfile** während der Anwendungsinstallation oder zu einem beliebigen Zeitpunkt während einer Sitzung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6aa46-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="6aa46-129">Wenn diese Methode zur Installation aufgerufen wird, stammen viele Konfigurationseinstellungen aus der Konfigurationsdatei MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="6aa46-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="6aa46-130">Wenn diese Methode während einer aktiven Sitzung aufgerufen wird, stammen die Einstellungen vom Benutzer, der durch eine Reihe von Eigenschaftenblättern dazu aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="6aa46-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="6aa46-131">Wenn das MAPI_DEFAULT_SERVICES-Flag im Parameter _ulFlags_ festgelegt ist, ruft CreateProfile die Entry Point-Funktion des Nachrichtendiensts für jeden Nachrichtendienst im Abschnitt [Default Services] in der Datei MAPISVC. inf auf. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6aa46-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="6aa46-132">Jede Nachrichtendienst-Einstiegspunktfunktion wird aufgerufen, wobei der _ulContext_ -Parameter auf MSG_SERVICE_CREATE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6aa46-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="6aa46-133">Wenn sowohl die MAPI_DIALOG-als auch die MAPI_DEFAULT_SERVICES-Flags festgelegt werden, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ ebenfalls an die Einstiegspunktfunktion des Nachrichtendiensts übergeben.</span><span class="sxs-lookup"><span data-stu-id="6aa46-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="6aa46-134">Die Nachrichtendienst-Einstiegspunktfunktionen werden nur aufgerufen, nachdem dem Profil alle verfügbaren Informationen aus der Datei MAPISVC. inf hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="6aa46-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="6aa46-135">Der Name des neuen Profils und sein Kennwort können bis zu 64 Zeichen lang sein und die folgenden Zeichen enthalten:</span><span class="sxs-lookup"><span data-stu-id="6aa46-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="6aa46-136">Alle alphanumerischen Zeichen, einschließlich Akzentzeichen und der Unterstrich.</span><span class="sxs-lookup"><span data-stu-id="6aa46-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="6aa46-137">Eingebettete Leerzeichen, aber keine führenden oder nachstehenden Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6aa46-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="6aa46-138">Der _lpszPassword_ -Parameter muss NULL oder ein Zeiger auf eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="6aa46-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6aa46-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6aa46-139">See also</span></span>



[<span data-ttu-id="6aa46-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="6aa46-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="6aa46-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="6aa46-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="6aa46-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="6aa46-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="6aa46-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6aa46-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


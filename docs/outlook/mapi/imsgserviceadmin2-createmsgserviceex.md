---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410182"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="c8dfe-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="c8dfe-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="c8dfe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8dfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8dfe-105">Fügt dem aktuellen Profil einen Nachrichtendienst hinzu und gibt die neu hinzugefügte Dienst-UID zurück.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="c8dfe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8dfe-106">Parameters</span></span>

 <span data-ttu-id="c8dfe-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="c8dfe-107">_lpszService_</span></span>
  
> <span data-ttu-id="c8dfe-108">in Ein Zeiger auf den Namen des hinzuzufügenden Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="c8dfe-109">Dieser Nachrichtendienst Name muss im Abschnitt **[Dienste]** der Datei MapiSvc. inf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="c8dfe-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="c8dfe-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="c8dfe-111">in Ein Zeiger auf den Anzeigenamen des hinzuzufügenden Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="c8dfe-112">Der Parameter _lpszDisplayName_ wird ignoriert, wenn der Nachrichtendienst die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Datei MapiSvc. inf festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="c8dfe-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c8dfe-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="c8dfe-114">in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="c8dfe-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8dfe-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c8dfe-116">in Eine Bitmaske von Flags, die die Installation des Nachrichtendiensts steuert.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="c8dfe-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c8dfe-117">The following flags can be set:</span></span>
    
<span data-ttu-id="c8dfe-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8dfe-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="c8dfe-119">Die Parameter lpszService und lpszDisplayName sollten in LPWSTR umgewandelt und als Unicode-Zeichenfolgen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="c8dfe-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="c8dfe-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="c8dfe-121">Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem, basierend auf verschiedenen Umständen und Kriterien, häufig, dass diese Aktion einen Neustart von Outlook erfordert.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="c8dfe-122">Wenn das SERVICE_NO_RESTART_WARNING-Flag nicht enthalten ist und die Benutzeroberfläche basierend auf den SERVICE_UI_ALWAYS-und SERVICE_UI_ALLOWED-Flags zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung "Sie müssen Outlook neu starten für Diese Änderungen werden wirksam. "</span><span class="sxs-lookup"><span data-stu-id="c8dfe-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="c8dfe-123">Mit dem SERVICE_NO_RESTART_WARNING-Flag wird die Anzeige der Warnmeldung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="c8dfe-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="c8dfe-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="c8dfe-125">Die Benutzeroberfläche der Nachrichtendienst Konfiguration ist bei Bedarf zulässig.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="c8dfe-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="c8dfe-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="c8dfe-127">Der Nachrichtendienst zeigt das zugehörige Konfigurationseigenschaften Fenster an.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="c8dfe-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="c8dfe-128">_lpuidService_</span></span>
  
> <span data-ttu-id="c8dfe-129">Out Der Zeiger auf die UID des hinzugefügten Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8dfe-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8dfe-130">Return value</span></span>

<span data-ttu-id="c8dfe-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8dfe-131">S_OK</span></span>
  
> <span data-ttu-id="c8dfe-132">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c8dfe-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c8dfe-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="c8dfe-134">Der Name des Nachrichtendiensts befindet sich nicht im Abschnitt **[Dienste]** von MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8dfe-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8dfe-135">Remarks</span></span>

<span data-ttu-id="c8dfe-136">Mit der **IMsgServiceAdmin2:: CreateMsgServiceEx** -Methode wird dem aktuellen Profil ein Nachrichtendienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="c8dfe-137">**CreateMsgServiceEx** Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="c8dfe-138">Wenn das SERVICE_UI_ALLOWED-Flag im Parameter _ulFlags_ festgelegt ist, kann der zu installierende Nachrichtendienst ein Eigenschaftenfenster anzeigen, das es dem Benutzer ermöglicht, seine Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="c8dfe-139">Die Datei MapiSvc. inf enthält die Liste der Anbieter, aus denen sich ein Nachrichtendienst zusammensetzen, und die jeweiligen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="c8dfe-140">**CreateMsgServiceEx** erstellt zunächst einen neuen Profil Abschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc. inf in das Profil, sodass für jeden Anbieter neue Abschnitte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="c8dfe-141">Nachdem alle Informationen aus MapiSvc. inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts, **MSGSERVICEENTRY**, mit dem MSG_SERVICE_CREATE-Wert aufgerufen, der im Parameter _ulContext_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="c8dfe-142">Wenn das SERVICE_UI_ALLOWED-Flag im _ulFlags_ -Parameter der **CreateMsgServiceEx** -Methode festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="c8dfe-143">Dienstanbieter sollten Ihre Konfigurationseigenschaften Blätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8dfe-144">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c8dfe-144">Notes to callers</span></span>

<span data-ttu-id="c8dfe-145">Wenn das Argument **CreateMsgServiceEx** _lpuidService_ nicht NULL ist, wird die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft des Nachrichtendiensts, der dem Profil hinzugefügt wurde, in der **GUID** zurückgegeben, auf die es zeigt.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="c8dfe-146">Übergeben Sie den Wert der **PR_SERVICE_UID** -Eigenschaft im _lpuidService_ -Parameter an die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode, um den Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="c8dfe-147">Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt MAPI_UNICODE nicht und schlägt fehl, wenn Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c8dfe-148">Die IMsgServiceAdmin2-Schnittstelle wird durch das gleiche Objekt verfügbar gemacht, das die IMsgServiceAdmin-Schnittstelle implementiert, und ist in der Outlook-Implementierung des MAPI-Subsystems seit Outlook 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8dfe-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="c8dfe-149">Die IID ist wie folgt definiert: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> der _ulFlags_ -SERVICE_NO_RESTART_WARNING ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie ihn mithilfe des folgenden Werts zu Ihrem Code hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="c8dfe-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8dfe-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8dfe-150">See also</span></span>



[<span data-ttu-id="c8dfe-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="c8dfe-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="c8dfe-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c8dfe-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


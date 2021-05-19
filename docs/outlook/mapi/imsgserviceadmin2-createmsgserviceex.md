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
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="32268-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="32268-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="32268-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32268-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32268-105">Fügt dem aktuellen Profil einen Nachrichtendienst hinzu und gibt die neu hinzugefügte Dienst-UID zurück.</span><span class="sxs-lookup"><span data-stu-id="32268-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="32268-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32268-106">Parameters</span></span>

 <span data-ttu-id="32268-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="32268-107">_lpszService_</span></span>
  
> <span data-ttu-id="32268-108">[in] Ein Zeiger auf den Namen des hinzuzufügende Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="32268-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="32268-109">Dieser Nachrichtendienstname muss im **Abschnitt [Dienste]** der Datei MapiSvc.inf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="32268-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="32268-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="32268-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="32268-111">[in] Ein Zeiger auf den Anzeigenamen des hinzuzufügende Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="32268-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="32268-112">Der  _lpszDisplayName-Parameter_ wird ignoriert, wenn der Nachrichtendienst die **eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in der Datei MapiSvc.inf festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="32268-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="32268-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="32268-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="32268-114">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="32268-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="32268-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32268-115">_ulFlags_</span></span>
  
> <span data-ttu-id="32268-116">[in] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtendienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="32268-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="32268-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="32268-117">The following flags can be set:</span></span>
    
<span data-ttu-id="32268-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="32268-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="32268-119">Die Parameter lpszService und lpszDisplayName sollten in LPWSTR umvertiert und als Unicode-Zeichenfolgen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="32268-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="32268-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="32268-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="32268-121">Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem basierend auf verschiedenen Umständen und Kriterien häufig, dass diese Aktion einen Neustart von Outlook erfordert.</span><span class="sxs-lookup"><span data-stu-id="32268-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="32268-122">Wenn das SERVICE_NO_RESTART_WARNING-Flag nicht enthalten ist und die Benutzeroberfläche – basierend auf den SERVICE_UI_ALWAYS- und SERVICE_UI_ALLOWED-Flags – zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung "Sie müssen Outlook neu starten, damit diese Änderungen wirksam werden."</span><span class="sxs-lookup"><span data-stu-id="32268-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="32268-123">Durch das SERVICE_NO_RESTART_WARNING wird die Anzeige dieser Warnmeldung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="32268-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="32268-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="32268-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="32268-125">Die Benutzeroberfläche für die Nachrichtendienstkonfiguration ist bei Bedarf zulässig.</span><span class="sxs-lookup"><span data-stu-id="32268-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="32268-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="32268-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="32268-127">Der Nachrichtendienst zeigt sein Konfigurationseigenschaftsblatt an.</span><span class="sxs-lookup"><span data-stu-id="32268-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="32268-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="32268-128">_lpuidService_</span></span>
  
> <span data-ttu-id="32268-129">[out] Der Zeiger auf die UID des hinzugefügten Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="32268-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32268-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32268-130">Return value</span></span>

<span data-ttu-id="32268-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="32268-131">S_OK</span></span>
  
> <span data-ttu-id="32268-132">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="32268-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="32268-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="32268-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="32268-134">Der Name des Nachrichtendiensts befindet sich nicht im **Abschnitt [Dienste]** von MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="32268-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="32268-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32268-135">Remarks</span></span>

<span data-ttu-id="32268-136">Die **IMsgServiceAdmin2::CreateMsgServiceEx-Methode** fügt dem aktuellen Profil einen Nachrichtendienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="32268-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="32268-137">**CreateMsgServiceEx** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="32268-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="32268-138">Wenn das SERVICE_UI_ALLOWED im  _ulFlags-Parameter_ festgelegt ist, kann der zu installierende Nachrichtendienst ein Eigenschaftenblatt anzeigen, mit dem der Benutzer seine Einstellungen konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="32268-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="32268-139">Die Datei MapiSvc.inf enthält die Liste der Anbieter, aus der ein Nachrichtendienst besteht, und die Jeweiligen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="32268-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="32268-140">**CreateMsgServiceEx** erstellt zunächst einen neuen Profilabschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc.inf in das Profil, wodurch neue Abschnitte für jeden Anbieter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="32268-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="32268-141">Nachdem alle Informationen aus MapiSvc.inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts **MSGSERVICEENTRY** mit dem im  _ulContext-Parameter_ festgelegten MSG_SERVICE_CREATE aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="32268-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="32268-142">Wenn das SERVICE_UI_ALLOWED-Flag im _ulFlags-Parameter_ der **CreateMsgServiceEx-Methode** festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="32268-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="32268-143">Dienstanbieter sollten ihre Konfigurationseigenschaftsblätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="32268-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="32268-144">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="32268-144">Notes to callers</span></span>

<span data-ttu-id="32268-145">Wenn das **Argument CreateMsgServiceEx** _lpuidService_ nicht NULL ist, wird die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft des Nachrichtendiensts, der dem Profil hinzugefügt wurde, in der **GUID** zurückgegeben, auf die es verweist.</span><span class="sxs-lookup"><span data-stu-id="32268-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="32268-146">Übergeben Sie den Wert der **PR_SERVICE_UID-Eigenschaft** im  _lpuidService-Parameter_ an die [IMsgServiceAdmin::ConfigureMsgService-Methode,](imsgserviceadmin-configuremsgservice.md) um den Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="32268-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="32268-147">Die Microsoft Outlook 2010 des MAPI-Subsystems unterstützt keine MAPI_UNICODE und führt bei Verwendung zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="32268-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="32268-148">Die IMsgServiceAdmin2-Schnittstelle wird von demselben Objekt verfügbar gemacht, das die IMsgServiceAdmin-Schnittstelle implementiert, und steht seit Outlook 2003 mithilfe der Implementierung des MAPI-Subsystems von Outlook zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="32268-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="32268-149">Die IID ist wie folgt definiert: >> Die `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);` _ulFlags_ SERVICE_NO_RESTART_WARNING ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe des folgenden Werts hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="32268-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32268-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32268-150">See also</span></span>



[<span data-ttu-id="32268-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="32268-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="32268-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="32268-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


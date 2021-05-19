---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434977"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="1d56f-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="1d56f-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="1d56f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d56f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d56f-105">Veraltet: Die Verwendung von [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="1d56f-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="1d56f-106">Fügt dem aktuellen Profil einen Nachrichtendienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d56f-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="1d56f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d56f-107">Parameters</span></span>

 <span data-ttu-id="1d56f-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="1d56f-108">_lpszService_</span></span>
  
> <span data-ttu-id="1d56f-109">[in] Ein Zeiger auf den Namen des hinzuzufügende Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="1d56f-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="1d56f-110">Dieser Nachrichtendienstname muss im **Abschnitt [Dienste]** der Datei MapiSvc.inf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d56f-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="1d56f-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="1d56f-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="1d56f-112">[in] Ein Zeiger auf den Anzeigenamen des hinzuzufügende Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="1d56f-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="1d56f-113">Der  _lpszDisplayName-Parameter_ wird ignoriert, wenn der Nachrichtendienst die **eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in der Datei MapiSvc.inf festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="1d56f-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="1d56f-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1d56f-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="1d56f-115">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1d56f-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="1d56f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d56f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1d56f-117">[in] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtendienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="1d56f-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="1d56f-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1d56f-118">The following flags can be set:</span></span>
    
<span data-ttu-id="1d56f-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d56f-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1d56f-120">Die Parameter lpszService und lpszDisplayName sollten in LPWSTR umvertiert und als Unicode-Zeichenfolgen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d56f-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="1d56f-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="1d56f-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="1d56f-122">Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem basierend auf verschiedenen Umständen und Kriterien häufig, dass für diese Aktion ein Neustart der Outlook.</span><span class="sxs-lookup"><span data-stu-id="1d56f-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="1d56f-123">Wenn das SERVICE_NO_RESTART_WARNING-Flag nicht enthalten ist und die Benutzeroberfläche – basierend auf den SERVICE_UI_ALWAYS- und SERVICE_UI_ALLOWED-Flags – zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung "Sie müssen Outlook neu starten, damit diese Änderungen wirksam werden."</span><span class="sxs-lookup"><span data-stu-id="1d56f-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="1d56f-124">Durch das SERVICE_NO_RESTART_WARNING wird die Anzeige dieser Warnmeldung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="1d56f-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="1d56f-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="1d56f-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="1d56f-126">Die Benutzeroberfläche für die Nachrichtendienstkonfiguration ist bei Bedarf zulässig.</span><span class="sxs-lookup"><span data-stu-id="1d56f-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="1d56f-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="1d56f-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="1d56f-128">Der Nachrichtendienst zeigt sein Konfigurationseigenschaftsblatt an.</span><span class="sxs-lookup"><span data-stu-id="1d56f-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d56f-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d56f-129">Return value</span></span>

<span data-ttu-id="1d56f-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d56f-130">S_OK</span></span> 
  
> <span data-ttu-id="1d56f-131">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1d56f-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1d56f-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1d56f-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1d56f-133">Der Name des Nachrichtendiensts befindet sich nicht im **Abschnitt [Dienste]** von MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="1d56f-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1d56f-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d56f-134">Remarks</span></span>

<span data-ttu-id="1d56f-135">Die **IMsgServiceAdmin::CreateMsgService-Methode** fügt dem aktuellen Profil einen Nachrichtendienst hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d56f-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="1d56f-136">**CreateMsgService ruft** die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1d56f-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="1d56f-137">Wenn das SERVICE_UI_ALLOWED im  _ulFlags-Parameter_ festgelegt ist, kann der zu installierende Nachrichtendienst ein Eigenschaftenblatt anzeigen, damit der Benutzer seine Einstellungen konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="1d56f-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="1d56f-138">Die Datei MapiSvc.inf enthält die Liste der Anbieter, aus der ein Nachrichtendienst besteht, und die Jeweiligen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d56f-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="1d56f-139">**CreateMsgService** erstellt zunächst einen neuen Profilabschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc.inf in das Profil, wodurch neue Abschnitte für jeden Anbieter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d56f-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="1d56f-140">Nachdem alle Informationen aus MapiSvc.inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts mit dem wert MSG_SERVICE_CREATE im  _ulContext-Parameter_ aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d56f-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="1d56f-141">Wenn das SERVICE_UI_ALLOWED im _ulFlags-Parameter_ der **CreateMsgService-Methode** festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1d56f-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="1d56f-142">Dienstanbieter sollten ihre Konfigurationseigenschaftsblätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="1d56f-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1d56f-143">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1d56f-143">Notes to callers</span></span>

 <span data-ttu-id="1d56f-144">**CreateMsgService** gibt die [MAPIUID-Struktur](mapiuid.md) für den Nachrichtendienst, der dem Profil hinzugefügt wurde, nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="1d56f-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="1d56f-145">Verwenden Sie das folgende Verfahren, um die **MAPIUID** für den erstellten Nachrichtendienst abzurufen:</span><span class="sxs-lookup"><span data-stu-id="1d56f-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="1d56f-146">Rufen Sie [die IMsgServiceAdmin::GetMsgServiceTable-Methode](imsgserviceadmin-getmsgservicetable.md) auf, um die Nachrichtendienstverwaltungstabelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d56f-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="1d56f-147">Suchen Sie die Zeile, die den Nachrichtendienst darstellt, indem Sie eine Einschränkung für die Tabelle **setzen,** die der PR_SERVICE_NAME ([PidTagServiceName](pidtagservicename-canonical-property.md)) -Eigenschaft mit dem Namen des Nachrichtendiensts entspricht.</span><span class="sxs-lookup"><span data-stu-id="1d56f-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="1d56f-148">Rufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) -Eigenschaft des Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="1d56f-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="1d56f-149">Übergeben Sie den Wert der **PR_SERVICE_UID-Eigenschaft** im  _lpUid-Parameter_ an die [IMsgServiceAdmin::ConfigureMsgService-Methode,](imsgserviceadmin-configuremsgservice.md) um den Dienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1d56f-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="1d56f-150">Die Microsoft Outlook 2010 des MAPI-Subsystems unterstützt keine MAPI_UNICODE und führt bei Verwendung zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="1d56f-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1d56f-151">Die  _ulFlags SERVICE_NO_RESTART_WARNING-Datei_ ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe des folgenden Werts hinzufügen: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="1d56f-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d56f-152">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1d56f-152">MFCMAPI reference</span></span>

<span data-ttu-id="1d56f-153">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1d56f-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d56f-154">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1d56f-154">**File**</span></span>|<span data-ttu-id="1d56f-155">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1d56f-155">**Function**</span></span>|<span data-ttu-id="1d56f-156">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1d56f-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d56f-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1d56f-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1d56f-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="1d56f-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="1d56f-159">MFCMAPI verwendet die **IMsgServiceAdmin::CreateMsgService-Methode,** um einem Profil einen Dienst hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d56f-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d56f-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d56f-160">See also</span></span>



[<span data-ttu-id="1d56f-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d56f-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="1d56f-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1d56f-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


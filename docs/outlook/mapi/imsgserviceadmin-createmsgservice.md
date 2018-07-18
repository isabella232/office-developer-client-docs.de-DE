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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e0bdd7108bacd17134592ac05ba71510fde76d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792634"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="6f175-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="6f175-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="6f175-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f175-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f175-105">Veraltet: Die Verwendung von [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6f175-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="6f175-106">Fügt einen Nachrichtendienst zum aktuellen Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="6f175-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="6f175-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f175-107">Parameters</span></span>

 <span data-ttu-id="6f175-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="6f175-108">_lpszService_</span></span>
  
> <span data-ttu-id="6f175-109">[in] Ein Zeiger auf den Namen des Diensts Nachricht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f175-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="6f175-110">Diese Meldung Dienstname muss in der die Datei "MapiSvc.inf" im Abschnitt **[Services]** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f175-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="6f175-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="6f175-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="6f175-112">[in] Ein Zeiger auf den Anzeigenamen des Diensts Nachricht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f175-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="6f175-113">Der Parameter _LpszDisplayName_ wird ignoriert, wenn der Message-Dienst die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Datei "MapiSvc.inf" festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f175-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="6f175-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6f175-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="6f175-115">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="6f175-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="6f175-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f175-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6f175-117">[in] Eine Bitmaske aus Flags, die steuert, wie der Nachrichtendienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6f175-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="6f175-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6f175-118">The following flags can be set:</span></span>
    
<span data-ttu-id="6f175-119">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f175-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="6f175-120">Die LpszService und die LpszDisplayName-Parameter sollte in LPWSTR umgewandelt und als Unicode-Zeichenfolgen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="6f175-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="6f175-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="6f175-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="6f175-122">Beim Hinzufügen eines neuen Nachricht-Diensts auf das Profil, bestimmt das MAPI-Subsystem, basierend auf verschiedenen Umständen und Kriterien, häufig, dass diese Aktion einen Neustart von Outlook erfordert.</span><span class="sxs-lookup"><span data-stu-id="6f175-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="6f175-123">Wenn das Flag SERVICE_NO_RESTART_WARNING ist nicht mit inbegriffen und Benutzeroberfläche zulässig - basierend auf die Flags SERVICE_UI_ALWAYS und SERVICE_UI_ALLOWED - und mindestens einen Prozess das aktuelle Profil angemeldet ist, gibt diese Funktion die Nachricht "müssen Sie Outlook neu starten diese Änderungen wirksam werden."</span><span class="sxs-lookup"><span data-stu-id="6f175-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="6f175-124">Das Flag SERVICE_NO_RESTART_WARNING einschließlich unterdrückt die Anzeige dieser Warnung Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6f175-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="6f175-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="6f175-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="6f175-126">Die Konfiguration des Dienstes ist Benutzeroberfläche zulässig, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f175-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="6f175-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="6f175-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="6f175-128">Die Messagingdiensts zeigt das Eigenschaftenfenster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6f175-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6f175-129">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6f175-129">Return value</span></span>

<span data-ttu-id="6f175-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f175-130">S_OK</span></span> 
  
> <span data-ttu-id="6f175-131">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="6f175-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6f175-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6f175-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6f175-133">Der Dienstname Nachricht ist nicht in der MapiSvc.inf im Abschnitt **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="6f175-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6f175-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f175-134">Remarks</span></span>

<span data-ttu-id="6f175-135">Die **IMsgServiceAdmin:: CreateMsgService** -Methode wird das aktuelle Profil ein Messagingdiensts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f175-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="6f175-136">**CreateMsgService** Ruft die Messagingdiensts Eintrag Point-Funktion, um alle dienstspezifische Konfigurationsaufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f175-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="6f175-137">Wenn das Flag SERVICE_UI_ALLOWED im _UlFlags_ -Parameter festgelegt ist, kann der Message-Dienst installiert wird ein Eigenschaftenblatt zum Aktivieren des Benutzers so konfigurieren Sie ihre Einstellungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f175-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="6f175-138">Die Datei "MapiSvc.inf" enthält die Liste der Anbieter, die eine Message Service und die Eigenschaften für jede bilden.</span><span class="sxs-lookup"><span data-stu-id="6f175-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="6f175-139">**CreateMsgService** zuerst erstellt einen neuen Profilabschnitt für den Dienst und kopiert alle Informationen für den betreffenden Dienst aus der Datei "MapiSvc.inf" in das Profil neue Abschnitte für jeden Anbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f175-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="6f175-140">Nachdem alle Informationen aus MapiSvc.inf kopiert wurde, wird die Messagingdiensts Eintrag Point-Funktion mit dem Wert MSG_SERVICE_CREATE im _UlContext_ -Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6f175-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="6f175-141">Wenn das Flag SERVICE_UI_ALLOWED in die **CreateMsgService** -Methode _UlFlags_ Parameter festgelegt ist, werden die Werte in den _UlUIParam_ und _UlFlags_ auch übergeben, wenn die Messagingdiensts Eintrag Point-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6f175-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="6f175-142">Dienstanbieter sollte ihre Konfiguration Eigenschaftenseiten angezeigt werden, damit Benutzer den Nachrichtendienst konfigurieren zu können.</span><span class="sxs-lookup"><span data-stu-id="6f175-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6f175-143">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6f175-143">Notes to callers</span></span>

 <span data-ttu-id="6f175-144">**CreateMsgService** gibt keine [MAPIUID](mapiuid.md) -Struktur für den Dienst zurück, das dem Profil hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f175-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="6f175-145">Verwenden Sie zum Abrufen der **MAPIUID** für den Nachrichtendienst erstellten die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="6f175-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="6f175-146">Rufen Sie die [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) -Methode, um die Nachricht Service Administration-Tabelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f175-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="6f175-147">Suchen Sie die Zeile, die den Dienst durch eine Einschränkung für die Tabelle, die die **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))-Eigenschaft mit dem Namen des Diensts Nachricht entspricht platzieren darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f175-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="6f175-148">Rufen Sie den Dienst **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="6f175-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="6f175-149">Übergeben Sie den Wert der Eigenschaft **PR_SERVICE_UID** im _LpUid_ -Parameter an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode zum Konfigurieren des Diensts.</span><span class="sxs-lookup"><span data-stu-id="6f175-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="6f175-150">Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt keine Parameter MAPI_UNICODE und schlägt fehl, wenn sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f175-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6f175-151">_UlFlags_ SERVICE_NO_RESTART_WARNING möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mit dem folgenden Wert hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="6f175-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6f175-152">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="6f175-152">MFCMAPI reference</span></span>

<span data-ttu-id="6f175-153">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6f175-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6f175-154">**Datei**</span><span class="sxs-lookup"><span data-stu-id="6f175-154">**File**</span></span>|<span data-ttu-id="6f175-155">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="6f175-155">**Function**</span></span>|<span data-ttu-id="6f175-156">**Comment**</span><span class="sxs-lookup"><span data-stu-id="6f175-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f175-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6f175-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6f175-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="6f175-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="6f175-159">MFCMAPI (engl.) verwendet die **IMsgServiceAdmin:: CreateMsgService** -Methode, um einen Dienst zu einem Profil hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f175-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f175-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f175-160">See also</span></span>



[<span data-ttu-id="6f175-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f175-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="6f175-162">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="6f175-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3aae61f7b21c507da7955dbb4393d13bfb5fa24c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792604"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="177d2-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="177d2-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="177d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="177d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="177d2-105">Fügt einen Nachrichtendienst gibt, die Dienst-UID neu hinzugefügt und der aktuellen Profil hinzu.</span><span class="sxs-lookup"><span data-stu-id="177d2-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="177d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="177d2-106">Parameters</span></span>

 <span data-ttu-id="177d2-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="177d2-107">_lpszService_</span></span>
  
> <span data-ttu-id="177d2-108">[in] Ein Zeiger auf den Namen des Diensts Nachricht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="177d2-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="177d2-109">Diese Meldung Dienstname muss in der die Datei "MapiSvc.inf" im Abschnitt **[Services]** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="177d2-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="177d2-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="177d2-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="177d2-111">[in] Ein Zeiger auf den Anzeigenamen des Diensts Nachricht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="177d2-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="177d2-112">Der Parameter _LpszDisplayName_ wird ignoriert, wenn der Message-Dienst die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Datei "MapiSvc.inf" festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="177d2-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="177d2-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="177d2-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="177d2-114">[in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.</span><span class="sxs-lookup"><span data-stu-id="177d2-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="177d2-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="177d2-115">_ulFlags_</span></span>
  
> <span data-ttu-id="177d2-116">[in] Eine Bitmaske aus Flags, die steuert, wie der Nachrichtendienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="177d2-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="177d2-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="177d2-117">The following flags can be set:</span></span>
    
<span data-ttu-id="177d2-118">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="177d2-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="177d2-119">Die LpszService und die LpszDisplayName-Parameter sollte in LPWSTR umgewandelt und als Unicode-Zeichenfolgen interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="177d2-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="177d2-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="177d2-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="177d2-121">Beim Hinzufügen eines neuen Nachricht-Diensts auf das Profil, bestimmt das MAPI-Subsystem, basierend auf verschiedenen Umständen und Kriterien, häufig, dass diese Aktion einen Neustart von Outlook erfordert.</span><span class="sxs-lookup"><span data-stu-id="177d2-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="177d2-122">Wenn das Flag SERVICE_NO_RESTART_WARNING ist nicht mit inbegriffen und Benutzeroberfläche zulässig - basierend auf die Flags SERVICE_UI_ALWAYS und SERVICE_UI_ALLOWED - und mindestens einen Prozess das aktuelle Profil angemeldet ist, gibt diese Funktion die Nachricht "müssen Sie Outlook neu starten diese Änderungen wirksam werden."</span><span class="sxs-lookup"><span data-stu-id="177d2-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="177d2-123">Das Flag SERVICE_NO_RESTART_WARNING einschließlich unterdrückt die Anzeige dieser Warnung Nachricht.</span><span class="sxs-lookup"><span data-stu-id="177d2-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="177d2-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="177d2-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="177d2-125">Die Konfiguration des Dienstes ist Benutzeroberfläche zulässig, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="177d2-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="177d2-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="177d2-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="177d2-127">Die Messagingdiensts zeigt das Eigenschaftenfenster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="177d2-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="177d2-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="177d2-128">_lpuidService_</span></span>
  
> <span data-ttu-id="177d2-129">[out] Der Zeiger auf die UID des Diensts Nachricht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="177d2-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="177d2-130">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="177d2-130">Return value</span></span>

<span data-ttu-id="177d2-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="177d2-131">S_OK</span></span>
  
> <span data-ttu-id="177d2-132">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="177d2-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="177d2-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="177d2-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="177d2-134">Der Dienstname Nachricht ist nicht in der MapiSvc.inf im Abschnitt **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="177d2-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="177d2-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="177d2-135">Remarks</span></span>

<span data-ttu-id="177d2-136">Die **IMsgServiceAdmin2::CreateMsgServiceEx** -Methode wird das aktuelle Profil ein Messagingdiensts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="177d2-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="177d2-137">**CreateMsgServiceEx** Ruft die Messagingdiensts Eintrag Point-Funktion, um alle dienstspezifische Konfigurationsaufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="177d2-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="177d2-138">Wenn das Flag SERVICE_UI_ALLOWED im _UlFlags_ -Parameter festgelegt ist, kann der Message-Dienst installiert wird ein Eigenschaftenblatt durch den Benutzer zum Konfigurieren der Einstellungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="177d2-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="177d2-139">Die Datei "MapiSvc.inf" enthält die Liste der Anbieter, die eine Message Service und die Eigenschaften für jede bilden.</span><span class="sxs-lookup"><span data-stu-id="177d2-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="177d2-140">**CreateMsgServiceEx** zuerst erstellt einen neuen Profilabschnitt für den Dienst und kopiert alle Informationen für den betreffenden Dienst aus der Datei "MapiSvc.inf" in das Profil neue Abschnitte für jeden Anbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="177d2-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="177d2-141">Nachdem alle Informationen aus MapiSvc.inf kopiert wurde, wird die Messagingdiensts Eintrag Point-Funktion, **MSGSERVICEENTRY**, mit dem Wert MSG_SERVICE_CREATE im _UlContext_ -Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="177d2-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="177d2-142">Wenn das Flag SERVICE_UI_ALLOWED in die **CreateMsgServiceEx** -Methode _UlFlags_ Parameter festgelegt ist, werden die Werte in den _UlUIParam_ und _UlFlags_ auch übergeben, wenn die Messagingdiensts Eintrag Point-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="177d2-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="177d2-143">Dienstanbieter sollte ihre Konfiguration Eigenschaftenseiten angezeigt werden, damit Benutzer den Nachrichtendienst konfigurieren zu können.</span><span class="sxs-lookup"><span data-stu-id="177d2-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="177d2-144">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="177d2-144">Notes to callers</span></span>

<span data-ttu-id="177d2-145">Wenn Arguments _LpuidService_ **CreateMsgServiceEx** nicht NULL ist, wird die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft des Diensts Nachricht, die dem Profil hinzugefügt wurde, die **GUID** zurückgegeben, auf die sie zeigt.</span><span class="sxs-lookup"><span data-stu-id="177d2-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="177d2-146">Übergeben Sie den Wert der Eigenschaft **PR_SERVICE_UID** im _LpuidService_ -Parameter an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode zum Konfigurieren des Diensts.</span><span class="sxs-lookup"><span data-stu-id="177d2-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="177d2-147">Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt keine Parameter MAPI_UNICODE und schlägt fehl, wenn sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="177d2-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="177d2-148">Die IMsgServiceAdmin2-Schnittstelle wird durch das gleiche Objekt verfügbar gemacht, die die IMsgServiceAdmin-Schnittstelle implementiert und wurde mithilfe des Outlook-Implementierung des MAPI-Subsystems seit Outlook 2003 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="177d2-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="177d2-149">Die IID wird wie folgt definiert: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _UlFlags_ SERVICE_NO_RESTART_WARNING möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mit dem folgenden Wert hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="177d2-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="177d2-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="177d2-150">See also</span></span>



[<span data-ttu-id="177d2-151">IMsgServiceAdmin2: IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="177d2-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="177d2-152">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="177d2-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


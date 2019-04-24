---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317409"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="c470b-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="c470b-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="c470b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c470b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c470b-105">Konfiguriert einen Nachrichtendienst neu.</span><span class="sxs-lookup"><span data-stu-id="c470b-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="c470b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c470b-106">Parameters</span></span>

 <span data-ttu-id="c470b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c470b-107">_lpUID_</span></span>
  
> <span data-ttu-id="c470b-108">in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu konfigurierenden Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="c470b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="c470b-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c470b-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c470b-110">in Ein Handle für das übergeordnete Fenster des Konfigurationseigenschaften Blatts.</span><span class="sxs-lookup"><span data-stu-id="c470b-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="c470b-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c470b-111">_ulFlags_</span></span>
  
> <span data-ttu-id="c470b-112">in Eine Bitmaske von Flags, die die Anzeige des Eigenschaftenblatts steuert.</span><span class="sxs-lookup"><span data-stu-id="c470b-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="c470b-113">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c470b-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c470b-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c470b-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c470b-115">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c470b-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c470b-116">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c470b-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="c470b-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="c470b-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="c470b-118">Der Nachrichtendienst sollte sein Konfigurationseigenschaften Blatt anzeigen, den Benutzer jedoch nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="c470b-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="c470b-119">Die meisten Nachrichtendienste ignorieren dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="c470b-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="c470b-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="c470b-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="c470b-121">Der Nachrichtendienst sollte sein Konfigurationseigenschaften Blatt nur anzeigen, wenn der Dienst nicht vollständig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="c470b-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="c470b-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="c470b-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="c470b-123">Der Nachrichtendienst muss immer sein Konfigurationseigenschaften Blatt anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c470b-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="c470b-124">Wenn SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Konfigurationseigenschaften Blatt weiterhin angezeigt werden, wenn SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen im Eigenschaftswert Array im _lpProps_ -Parameter nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c470b-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="c470b-125">Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, damit ein Eigenschaftenblatt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c470b-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="c470b-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="c470b-126">_cValues_</span></span>
  
> <span data-ttu-id="c470b-127">in Die Anzahl der Eigenschaftswerte in der [SPropValue](spropvalue.md) -Struktur, auf die durch _lpProps_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c470b-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="c470b-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="c470b-128">_lpProps_</span></span>
  
> <span data-ttu-id="c470b-129">in Ein Zeiger auf ein Array von Eigenschaftswerten, die die Eigenschaften beschreiben, die im Eigenschaftenfenster angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c470b-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="c470b-130">Der _lpProps_ -Parameter sollte nicht NULL sein, wenn der Nachrichtendienst ohne Benutzeroberfläche konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c470b-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c470b-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c470b-131">Return value</span></span>

<span data-ttu-id="c470b-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="c470b-132">S_OK</span></span> 
  
> <span data-ttu-id="c470b-133">Der Nachrichtendienst wurde erfolgreich konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c470b-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="c470b-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="c470b-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="c470b-135">Ein Fehler, der für einen Nachrichtendienst spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="c470b-135">An error specific to a message service.</span></span> <span data-ttu-id="c470b-136">Zum Abrufen der [MAPIERROR](mapierror.md) -Struktur, die den Fehler beschreibt, sollte die Clientanwendung die [IMsgServiceAdmin:: getlasterroraufzurufen](imsgserviceadmin-getlasterror.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c470b-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="c470b-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c470b-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c470b-138">Die **MAPIUID** , auf die durch _lpUID_ verwiesen wird, stimmt nicht mit dem eines vorhandenen Nachrichtendiensts überein.</span><span class="sxs-lookup"><span data-stu-id="c470b-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="c470b-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c470b-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="c470b-140">Der Nachrichtendienst verfügt nicht über eine Einstiegspunktfunktion.</span><span class="sxs-lookup"><span data-stu-id="c470b-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="c470b-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c470b-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c470b-142">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Eigenschaftenfenster.</span><span class="sxs-lookup"><span data-stu-id="c470b-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c470b-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c470b-143">Remarks</span></span>

<span data-ttu-id="c470b-144">Mit der **IMsgServiceAdmin:: ConfigureMsgService** -Methode kann ein Nachrichtendienst mit oder ohne Konfigurationseigenschaften Blatt konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c470b-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="c470b-145">Um die Konfiguration ohne Eigenschaftenblatt Anzeige zuzulassen, bereiten Nachrichtendienste in der Regel eine Headerdatei vor, die Konstanten für alle erforderlichen und optionalen Eigenschaften und deren Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="c470b-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c470b-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c470b-146">Notes to callers</span></span>

<span data-ttu-id="c470b-147">Um die **MAPIUID** -Struktur für den Nachrichtendienst zum Konfigurieren abzurufen, rufen Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Spalte aus der Zeile des Nachrichtendiensts in der Nachrichtendienst Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c470b-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="c470b-148">Weitere Informationen finden Sie in der in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode beschriebenen Prozedur.</span><span class="sxs-lookup"><span data-stu-id="c470b-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="c470b-149">Sie können einen Nachrichtendienst nur konfigurieren, ohne ein Eigenschaftenblatt für einen Benutzer anzuzeigen, wenn Sie über Vorabinformationen zu den festzulegenden Eigenschaftswerten verfügen.</span><span class="sxs-lookup"><span data-stu-id="c470b-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="c470b-150">Wenn Sie einen Nachrichtendienst ohne Anzeige eines Eigenschaftenblatts konfigurieren, übergeben Sie gültige Eigenschaftswerte im _lpProps_ -Parameter, und legen Sie die Flags MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS nicht fest.</span><span class="sxs-lookup"><span data-stu-id="c470b-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="c470b-151">Wenn Sie alle oder einen Teil der Konfigurationsinformationen des Benutzers über ein Eigenschaftenblatt erhalten, legen Sie SERVICE_UI_ALLOWED in _ulFlags_fest.</span><span class="sxs-lookup"><span data-stu-id="c470b-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="c470b-152">Wenn Sie vorhandene Eigenschaftsinformationen nur zum Einrichten von Standardeinstellungen verwenden und der Benutzer in der Lage ist, die Einstellungen zu ändern, legen Sie SERVICE_UI_ALWAYS in _ulFlags_fest.</span><span class="sxs-lookup"><span data-stu-id="c470b-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c470b-153">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c470b-153">MFCMAPI reference</span></span>

<span data-ttu-id="c470b-154">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c470b-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c470b-155">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c470b-155">**File**</span></span>|<span data-ttu-id="c470b-156">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c470b-156">**Function**</span></span>|<span data-ttu-id="c470b-157">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c470b-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c470b-158">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="c470b-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c470b-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="c470b-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="c470b-160">MFCMAPI verwendet die **IMsgServiceAdmin:: ConfigureMsgService** -Methode, um einen Dienst zu konfigurieren, der einem Profil hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c470b-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c470b-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c470b-161">See also</span></span>



[<span data-ttu-id="c470b-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c470b-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c470b-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c470b-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c470b-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c470b-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="c470b-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c470b-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


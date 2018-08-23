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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568294"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="13fa8-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="13fa8-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="13fa8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13fa8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13fa8-105">Konfiguriert einen Message-Dienst neu.</span><span class="sxs-lookup"><span data-stu-id="13fa8-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="13fa8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13fa8-106">Parameters</span></span>

 <span data-ttu-id="13fa8-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="13fa8-107">_lpUID_</span></span>
  
> <span data-ttu-id="13fa8-108">[in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst so konfigurieren Sie enthält.</span><span class="sxs-lookup"><span data-stu-id="13fa8-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="13fa8-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="13fa8-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="13fa8-110">[in] Ein Handle für das übergeordnete Fenster im Eigenschaftsfenster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="13fa8-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="13fa8-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13fa8-111">_ulFlags_</span></span>
  
> <span data-ttu-id="13fa8-112">[in] Eine Bitmaske aus Flags, die die Anzeige des Eigenschaftenfensters steuert.</span><span class="sxs-lookup"><span data-stu-id="13fa8-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="13fa8-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="13fa8-113">The following flags can be set:</span></span>
    
<span data-ttu-id="13fa8-114">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13fa8-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="13fa8-115">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="13fa8-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="13fa8-116">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="13fa8-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="13fa8-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="13fa8-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="13fa8-118">Der Nachrichtendienst sollte das Eigenschaftenfenster Konfiguration anzuzeigen, aber nicht ermöglichen Benutzern das ändern.</span><span class="sxs-lookup"><span data-stu-id="13fa8-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="13fa8-119">Die meisten Message Dienste ignoriert dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="13fa8-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="13fa8-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="13fa8-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="13fa8-121">Der Nachrichtendienst sollte das Eigenschaftenblatt Konfiguration angezeigt werden nur, wenn der Dienst nicht vollständig konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="13fa8-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="13fa8-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="13fa8-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="13fa8-123">Message-Dienst muss immer das Eigenschaftenblatt Konfiguration anzeigen.</span><span class="sxs-lookup"><span data-stu-id="13fa8-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="13fa8-124">Wenn SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Eigenschaftenblatt Konfiguration weiterhin angezeigt, wenn SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen nicht verfügbar aus Array-Eigenschaft den Wert im _LpProps_ -Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="13fa8-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="13fa8-125">SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss für ein Eigenschaftenfenster, angezeigt werden soll, festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="13fa8-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="13fa8-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="13fa8-126">_cValues_</span></span>
  
> <span data-ttu-id="13fa8-127">[in] Die Anzahl der Eigenschaftswerte in der Struktur [SPropValue](spropvalue.md) auf _LpProps_zeigt.</span><span class="sxs-lookup"><span data-stu-id="13fa8-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="13fa8-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="13fa8-128">_lpProps_</span></span>
  
> <span data-ttu-id="13fa8-129">[in] Ein Zeiger auf ein Array der Eigenschaftswerte, die beschreiben, die Eigenschaften im Eigenschaftenfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13fa8-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="13fa8-130">Der Parameter _LpProps_ darf nicht NULL sein, wenn der Nachrichtendienst ohne Benutzeroberfläche konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="13fa8-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="13fa8-131">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="13fa8-131">Return value</span></span>

<span data-ttu-id="13fa8-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="13fa8-132">S_OK</span></span> 
  
> <span data-ttu-id="13fa8-133">Der Nachrichtendienst wurde erfolgreich konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="13fa8-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="13fa8-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="13fa8-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="13fa8-135">Fehler, die speziell für eine Message Service.</span><span class="sxs-lookup"><span data-stu-id="13fa8-135">An error specific to a message service.</span></span> <span data-ttu-id="13fa8-136">Wenn die Struktur [MAPIERROR](mapierror.md) erhalten möchten, die den Fehler beschreibt, sollte die Client-Anwendung die [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="13fa8-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="13fa8-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="13fa8-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="13fa8-138">Die auf den _LpUID_ **MAPIUID** stimmt nicht überein, die einem vorhandenen Meldung-Dienst.</span><span class="sxs-lookup"><span data-stu-id="13fa8-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="13fa8-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="13fa8-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="13fa8-140">Message-Dienst hat keine Funktion bei Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="13fa8-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="13fa8-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="13fa8-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="13fa8-142">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Eigenschaftenfenster abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="13fa8-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="13fa8-143">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="13fa8-143">Remarks</span></span>

<span data-ttu-id="13fa8-144">Die **IMsgServiceAdmin::ConfigureMsgService** -Methode ermöglicht eine Message Service mit oder ohne ein Eigenschaftenblatt Konfiguration konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="13fa8-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="13fa8-145">Um ohne Eigenschaft Blatt Bildschirm Konfiguration zu ermöglichen, Vorbereiten Message-Dienste in der Regel eine Headerdatei, die Konstanten für alle erforderlichen und optionalen Eigenschaften und deren Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="13fa8-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="13fa8-146">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="13fa8-146">Notes to callers</span></span>

<span data-ttu-id="13fa8-147">Rufen Sie die **MAPIUID** -Struktur für den Dienst so konfigurieren abgerufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Spalte aus der Nachrichtendienst Zeile in der Tabelle der Dienste.</span><span class="sxs-lookup"><span data-stu-id="13fa8-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="13fa8-148">Weitere Informationen finden Sie unter dem Verfahren in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="13fa8-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="13fa8-149">Sie können eine Message Service konfigurieren, ohne ein Eigenschaftenfenster, die einem Benutzer, nur, wenn Sie Advance Informationen über die Eigenschaftswerte festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="13fa8-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="13fa8-150">Wenn Sie einen Nachrichtendienst ohne ein Eigenschaftenblatt konfigurieren, valid-Eigenschaftswerte im _LpProps_ -Parameter übergeben, und die Kennzeichen MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="13fa8-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="13fa8-151">Wenn Sie von der Benutzer über ein Eigenschaftenblatt aller oder einiger der Konfigurationsinformationen erhalten haben, legen Sie SERVICE_UI_ALLOWED in _UlFlags_.</span><span class="sxs-lookup"><span data-stu-id="13fa8-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="13fa8-152">Wenn Sie vorhandene Eigenschafteninformationen nur für die Standardeinstellungen einrichten und der Benutzer die Einstellungen zu ändern kann, legen Sie SERVICE_UI_ALWAYS in _UlFlags_.</span><span class="sxs-lookup"><span data-stu-id="13fa8-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="13fa8-153">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="13fa8-153">MFCMAPI reference</span></span>

<span data-ttu-id="13fa8-154">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="13fa8-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13fa8-155">**Datei**</span><span class="sxs-lookup"><span data-stu-id="13fa8-155">**File**</span></span>|<span data-ttu-id="13fa8-156">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="13fa8-156">**Function**</span></span>|<span data-ttu-id="13fa8-157">**Comment**</span><span class="sxs-lookup"><span data-stu-id="13fa8-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13fa8-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="13fa8-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="13fa8-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="13fa8-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="13fa8-160">MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::ConfigureMsgService** -Methode, um einen Dienst zu konfigurieren, der zu einem Profil hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="13fa8-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13fa8-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13fa8-161">See also</span></span>



[<span data-ttu-id="13fa8-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="13fa8-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="13fa8-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="13fa8-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="13fa8-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13fa8-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="13fa8-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="13fa8-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792364"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="cdc21-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cdc21-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="cdc21-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cdc21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cdc21-105">Bestätigen Sie die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="cdc21-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="cdc21-106">Diese Methode wird in allen Status-Objekten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cdc21-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdc21-107">Parameters</span></span>

<span data-ttu-id="cdc21-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cdc21-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="cdc21-109">[in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="cdc21-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cdc21-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cdc21-111">[in] Eine Bitmaske aus Flags, die die Überprüfung steuert.</span><span class="sxs-lookup"><span data-stu-id="cdc21-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="cdc21-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cdc21-112">The following flags can be set:</span></span>
    
<span data-ttu-id="cdc21-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="cdc21-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="cdc21-114">Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** , in dem entsprechenden Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="cdc21-115">Das Statusobjekt besitzt zwei Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="cdc21-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="cdc21-116">Fortsetzen Sie Arbeit an den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cdc21-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="cdc21-117">Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED zurück.</span><span class="sxs-lookup"><span data-stu-id="cdc21-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="cdc21-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="cdc21-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="cdc21-119">Eine oder mehrere der Eigenschaften von Konfiguration der Status des Objekts geändert.</span><span class="sxs-lookup"><span data-stu-id="cdc21-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="cdc21-120">Clients können dieses Kennzeichen ermöglicht die MAPI-Warteschlange dynamisch kritische Transport Anbieter Fehler korrigieren festlegen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="cdc21-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="cdc21-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="cdc21-122">Das Statusobjekt sollte eine Verbindung ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-122">The status object should perform a connection.</span></span> <span data-ttu-id="cdc21-123">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, tritt die Verbindung ohne Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="cdc21-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="cdc21-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="cdc21-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="cdc21-125">Das Statusobjekt sollte einen Trennvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="cdc21-126">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, tritt das Trennen der Verbindung ohne Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="cdc21-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="cdc21-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cdc21-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cdc21-128">Einträge in der Kopfzeile Cachetabelle verarbeitet werden soll, sollten alle Nachrichten mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag heruntergeladen werden und alle Nachrichten mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="cdc21-129">Nachrichten, die MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="cdc21-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="cdc21-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cdc21-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cdc21-131">Bei einem remote-Transport-Anbieter sollte eine neue Liste der Kopfzeilen heruntergeladen werden, und alle Flags, die die Nachricht den Status markieren sollte deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="cdc21-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="cdc21-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="cdc21-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="cdc21-133">Verhindert, dass das Statusobjekt eine Benutzeroberfläche als Teil des Vorgangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cdc21-134">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="cdc21-134">Return value</span></span>

<span data-ttu-id="cdc21-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdc21-135">S_OK</span></span> 
  
> <span data-ttu-id="cdc21-136">Die Überprüfung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cdc21-136">The validation was successful.</span></span>
    
<span data-ttu-id="cdc21-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cdc21-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cdc21-138">Ein anderer Vorgang ist in Bearbeitung. Es dürfen für die Durchführung, oder er angehalten werden sollte, bevor Sie diesen Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cdc21-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="cdc21-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cdc21-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cdc21-140">Das Statusobjekt unterstützt nicht die Methode für die Überprüfung, wie durch die Abwesenheit des STATUS_VALIDATE_STATE-Flags in der Eigenschaft **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) angegeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="cdc21-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="cdc21-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="cdc21-142">Der Benutzer hat den Überprüfungsvorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="cdc21-143">Dieser Wert wird nur von remote-Transport-Anbietern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cdc21-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdc21-144">Remarks</span></span>

<span data-ttu-id="cdc21-145">Die **IMAPIStatus::ValidateState** -Methode überprüft den Status einer Ressource, die ein Statusobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cdc21-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="cdc21-146">**ValidateState** ist die einzige Methode in der [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle, die für alle Status erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cdc21-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="cdc21-147">Das genaue Verhalten dieser Methode hängt von der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="cdc21-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="cdc21-148">Die folgende Tabelle beschreibt die Implementierung der verschiedenen Arten von Status-Objekten.</span><span class="sxs-lookup"><span data-stu-id="cdc21-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="cdc21-149">**Statusobjekt**</span><span class="sxs-lookup"><span data-stu-id="cdc21-149">**Status object**</span></span>|<span data-ttu-id="cdc21-150">ValidateState ** Implementierung **</span><span class="sxs-lookup"><span data-stu-id="cdc21-150">****ValidateState** implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdc21-151">MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="cdc21-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="cdc21-152">Überprüft den Status aller Ressourcen, die die derzeit aktive-Dienstanbieter und Teilsystems selbst besitzen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="cdc21-153">MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="cdc21-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="cdc21-154">Führt eine Anmeldung aller Transport-Anbieter, unabhängig davon, ob sie bereits angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="cdc21-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="cdc21-155">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="cdc21-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="cdc21-156">Überprüft die Einträge in einem Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="cdc21-157">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="cdc21-157">Service provider</span></span>  <br/> |<span data-ttu-id="cdc21-158">Implementierung hängt die Art der Anbieter und die Kennzeichen, die im Parameter _UlFlags_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="cdc21-159">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="cdc21-159">Notes to implementers</span></span>

<span data-ttu-id="cdc21-160">Remote-Clientanwendungen rufen Sie die **ValidateState** -Methode, um remote Verarbeitung für verschiedene Aktionen zu starten.</span><span class="sxs-lookup"><span data-stu-id="cdc21-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="cdc21-161">Diese Methode vorhanden ist, in erster Linie um Statusbits der MAPI-Warteschlange, anstatt Kommunikation tatsächlich Arbeit leisten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="cdc21-162">In der Regel wird der Adressbuchhierarchie Flags in der Statuszeile, die an die Warteschlange MAPI angeben, welche Aktionen initiiert werden, um die Anforderung des Clients abzuschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="cdc21-163">In diesem Modell der Interaktion von Client-Transport-Warteschlange sind die Aktionen, die vom Client angeforderten asynchronen, **ValidateState** zurückgibt, bevor die angeforderten Aktionen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="cdc21-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="cdc21-164">Aktionen, die das zugrunde liegende messaging-System nicht unbedingt beinhalten oder bereit, die eine Schnittstelle Transport-spezifischen beinhalten, können jedoch synchrone sein.</span><span class="sxs-lookup"><span data-stu-id="cdc21-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="cdc21-165">Die Client-Anwendung übergibt eine Bitmaske der folgenden Werte aus, um anzugeben, welche Aktivitäten der Adressbuchhierarchie remote ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cdc21-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="cdc21-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="cdc21-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="cdc21-167">Wenn möglich, sollte der remote Adressbuchhierarchie Vorgänge abzubrechen, die umfassen Kopfzeilen heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="cdc21-168">Hierzu muss der Adressbuchhierarchie die folgenden Eigenschaftswerte in der Statuszeile des Anmeldung-Objekts festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cdc21-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="cdc21-169">Deaktivieren Sie die Bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE in der Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) anzuweisen, die MAPI-Warteschlange den eingehenden flush-Prozess für diesen Transportanbieter anhalten.</span><span class="sxs-lookup"><span data-stu-id="cdc21-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="cdc21-170">Legen Sie die STATUS_OFFLINE bit in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cdc21-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cdc21-171">Legen Sie die **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md))-Eigenschaft auf true fest.</span><span class="sxs-lookup"><span data-stu-id="cdc21-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="cdc21-172">Legen Sie die **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md))-Eigenschaft auf eine Zeichenfolge, die der Adressbuchhierarchie Status für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="cdc21-173">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="cdc21-173">Return S_OK.</span></span> <span data-ttu-id="cdc21-174">Wenn der Vorgang in Arbeit kann nicht abgebrochen werden, sollte **ValidateState** MAPI_E_BUSY zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="cdc21-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="cdc21-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="cdc21-176">Ein remote Transportdienstes richten Sie eine Verbindung mit einer freigegebenen Ressource (z. B. Modem oder COM-Anschluss) außerhalb des Kontexts der MAPI-Warteschlange-Transport-Aktivität beteiligt die [IXPLogon::FlushQueues](ixplogon-flushqueues.md) -Methode sollte niemals.</span><span class="sxs-lookup"><span data-stu-id="cdc21-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="cdc21-177">Wenn dieses Flag **ValidateState** aufgerufen wird, sollte der Adressbuchhierarchie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="cdc21-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="cdc21-178">Legen Sie einen internen Status-Flag, um anzugeben, dass die Verbindung hergestellt werden muss, die **IXPLogon::FlushQueues** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cdc21-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="cdc21-179">Legen Sie die richtigen Werte in der Statustabelle ", die dazu führen, dass die MAPI-Warteschlange, die Warteschlange, die leeren Prozess zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="cdc21-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="cdc21-180">Wenn das Leeren der Warteschlangen abgeschlossen ist, lassen Sie freigegebene Ressource.</span><span class="sxs-lookup"><span data-stu-id="cdc21-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="cdc21-181">Deaktivieren Sie das STATUS_OFFLINE bit in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cdc21-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cdc21-182">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="cdc21-182">Return S_OK.</span></span>
    
<span data-ttu-id="cdc21-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="cdc21-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="cdc21-184">Der remote Adressbuchhierarchie sollte die Verbindung mit der messaging Systemressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="cdc21-185">Nach dem auf diese Weise sollte es das STATUS_OFFLINE Bit in der **PR_STATUS_CODE** -Eigenschaft festgelegt und S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="cdc21-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="cdc21-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cdc21-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cdc21-187">Der remote Adressbuchhierarchie sollte remote-Nachrichten zu verarbeiten und Hochladen von Nachrichten, die zurückgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cdc21-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="cdc21-188">Hierzu muss der Adressbuchhierarchie die folgenden Eigenschaftswerte in der Statuszeile des Anmeldung-Objekts festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cdc21-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="cdc21-189">Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge, die der Adressbuchhierarchie Status für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="cdc21-190">Legen Sie die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE Bits in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cdc21-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cdc21-191">Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Adressbuchhierarchie Statuszeile auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="cdc21-192">Wenn ein anderer Vorgang in Arbeit (beispielsweise Kopfzeilen herunterladen) wird **ValidateState** aufgerufen wird, sollte **ValidateState** MAPI_E_BUSY zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="cdc21-193">Führen Sie den Code für die Verarbeitung der REFRESH_XP_HEADER_CACHE-Flag, um Anforderungen des Microsoft Exchange-Clients zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="cdc21-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cdc21-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cdc21-195">Der remote-Transport-Anbieter sollten alle neuen Nachrichtenkopfzeilen von messaging-System abrufen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="cdc21-196">Zu diesem Zweck muss der Adressbuchhierarchie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="cdc21-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="cdc21-197">Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge, die der Adressbuchhierarchie Status für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="cdc21-198">Legen Sie die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE Bits in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cdc21-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cdc21-199">Deaktivieren Sie das STATUS_OFFLINE bit in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cdc21-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cdc21-200">Legen Sie die STATUS_ONLINE bit in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cdc21-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cdc21-201">Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Adressbuchhierarchie Statuszeile auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="cdc21-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="cdc21-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="cdc21-203">Verfügt Ihre Adressbuchhierarchie alle Teile der Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen (beispielsweise ein Dialogfeld, das bestätigt das Herunterladen von Nachrichten), sollte das Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdc21-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="cdc21-204">Andernfalls können **ValidateState** MAPI_E_NO_SUPPORT zurück.</span><span class="sxs-lookup"><span data-stu-id="cdc21-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="cdc21-205">Wenn alle Flags als diese übergeben werden, sollte **ValidateState** MAPI_E_UNKNOWN_FLAGS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="cdc21-206">Aufruf der Adressbuchhierarchie des Clients werden häufig an die **IMAPIStatus::ValidateState** -Methode.</span><span class="sxs-lookup"><span data-stu-id="cdc21-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="cdc21-207">Während der Verarbeitung der **ValidateState**, sollte der Adressbuchhierarchie keine Aktionen ausführen, die anderen Komponenten um knappe Systemressourcen, wie ein Modem oder COM-Port zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="cdc21-208">Dies ist, da die MAPI-Warteschlange manchmal zum Leeren der Warteschlangen auf mehreren Adressbuchhierarchie benötigen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="cdc21-209">Der Client kann jedoch Adressbuchhierarchie **ValidateState** -Methode können Sie jederzeit aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="cdc21-210">Wenn Ihre Adressbuchhierarchie versucht, eine wertvolle Ressource während der Verarbeitung der **ValidateState**zugewiesen werden, kann ein Fehler aufgrund eines Konflikts mit einem anderen Adressbuchhierarchie führen, die die MAPI-Warteschlange angewiesen hat, um Warteschlangen zu leeren.</span><span class="sxs-lookup"><span data-stu-id="cdc21-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="cdc21-211">Wenn Sie alle anderen Komponenten um knappe Ressourcen Zuweisungen unter die Richtung der die MAPI-Warteschlange erfolgt zulassen, können Sie solche Konflikte vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cdc21-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="cdc21-212">Der Transportdienst sollte die **PR_REMOTE_VALIDATE_OK** -Eigenschaft unterstützen, damit Clientanwendungen erkennen können, wenn Ihre Adressbuchhierarchie ausgelastet oder wartet die MAPI-Warteschlange zum Initiieren einer Aktion ist.</span><span class="sxs-lookup"><span data-stu-id="cdc21-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cdc21-213">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="cdc21-213">Notes to callers</span></span>

<span data-ttu-id="cdc21-214">Da diese Methode anderen potenziell langen Aufrufe erfolgen auftreten kann, können **ValidateState** MAPI_E_BUSY zu informieren, wenn diese Methode auf den Abschluss einer anderen Operation wartet zurück.</span><span class="sxs-lookup"><span data-stu-id="cdc21-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="cdc21-215">Warten Sie, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie versuchen, einer anderen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="cdc21-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="cdc21-216">Sie haben die größte Kontrolle über Ihre Anrufe transport-Anbieter Status Objekte.</span><span class="sxs-lookup"><span data-stu-id="cdc21-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="cdc21-217">Sie können eine oder mehrere Flags an **ValidateState** , die der Adressbuchhierarchie Vorgänge betreffen übergeben.</span><span class="sxs-lookup"><span data-stu-id="cdc21-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="cdc21-218">Das Flag ABORT_XP_HEADER_OPERATION gibt beispielsweise an, dass der Benutzer die Überprüfung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="cdc21-219">Transportanbieter können entscheiden, um den Vorgang abzubrechen, MAPI_E_USER_CANCELED, zurückgeben oder fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="cdc21-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="cdc21-220">Klicken Sie auf einen Anruf an das Statusobjekt einem Dienstanbieter oder die MAPI-Warteschlange, um anzugeben, dass eine Konfigurationsoption geändert wurde, können Sie die CONFIG_CHANGED-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="cdc21-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="cdc21-221">CONFIG_CHANGED können Sie dynamisch eine Transportdienst neu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cdc21-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="cdc21-222">Wenn Sie CONFIG_CHANGED auf einen Anruf an einem Dienstanbieter Status-Objekt festlegen, reagiert der Anbieter mit einem Aufruf von [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) zu warnen, die MAPI-Warteschlange der Änderung.</span><span class="sxs-lookup"><span data-stu-id="cdc21-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="cdc21-223">Wenn Sie CONFIG_CHANGED auf einen Anruf an die MAPI-Warteschlange Status-Objekt festlegen, ruft die Warteschlange [IXPLogon::AddressTypes](ixplogon-addresstypes.md) für jeden Anbieter aktiven Transport.</span><span class="sxs-lookup"><span data-stu-id="cdc21-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="cdc21-224">**AddressTypes** informiert die MAPI-Warteschlange von unterstützten Adresstypen einen Transport.</span><span class="sxs-lookup"><span data-stu-id="cdc21-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="cdc21-225">Einige Dienstanbieter können auch eine Statusanzeige angezeigt, wenn die Überprüfung voraussichtlich dauert sehr lange.</span><span class="sxs-lookup"><span data-stu-id="cdc21-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="cdc21-226">Eine Statusanzeige anzeigen ist hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cdc21-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="cdc21-227">Wenn das Flag SUPPRESS_UI festgelegt ist, können keines der Eigenschaftenseiten Konfiguration oder Fortschritt Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cdc21-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cdc21-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc21-228">See also</span></span>

- [<span data-ttu-id="cdc21-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="cdc21-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="cdc21-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="cdc21-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="cdc21-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="cdc21-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="cdc21-232">PidTagRemoteValidateOk (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cdc21-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="cdc21-233">PidTagResourceMethods (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cdc21-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="cdc21-234">PidTagStatusCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cdc21-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="cdc21-235">PidTagStatusString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cdc21-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="cdc21-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cdc21-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)


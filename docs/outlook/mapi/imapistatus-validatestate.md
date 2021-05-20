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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438148"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="bc46e-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="bc46e-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="bc46e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc46e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc46e-105">Bestätigt die externen Statusinformationen, die für die MAPI-Ressource oder den Dienstanbieter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bc46e-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="bc46e-106">Diese Methode wird in allen Statusobjekten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc46e-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bc46e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc46e-107">Parameters</span></span>

<span data-ttu-id="bc46e-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bc46e-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="bc46e-109">[in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="bc46e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc46e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="bc46e-111">[in] Eine Bitmaske mit Flags, die die Überprüfung steuert.</span><span class="sxs-lookup"><span data-stu-id="bc46e-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="bc46e-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bc46e-112">The following flags can be set:</span></span>
    
<span data-ttu-id="bc46e-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="bc46e-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="bc46e-114">Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen im entsprechenden Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="bc46e-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="bc46e-115">Das status-Objekt verfügt über zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="bc46e-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="bc46e-116">Arbeiten Sie weiter an dem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bc46e-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="bc46e-117">Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="bc46e-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="bc46e-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="bc46e-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="bc46e-119">Eine oder mehrere Konfigurationseigenschaften des Statusobjekts wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="bc46e-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="bc46e-120">Clients können dieses Kennzeichen festlegen, damit der MAPI-Spooler kritische Fehler des Transportanbieters dynamisch korrigieren kann.</span><span class="sxs-lookup"><span data-stu-id="bc46e-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="bc46e-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="bc46e-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="bc46e-122">Das status-Objekt sollte eine Verbindung ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-122">The status object should perform a connection.</span></span> <span data-ttu-id="bc46e-123">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Verbindung ohne Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="bc46e-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="bc46e-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="bc46e-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="bc46e-125">Das status-Objekt sollte einen Verbindungstrennungsvorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="bc46e-126">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Trennung ohne Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="bc46e-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="bc46e-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bc46e-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bc46e-128">Einträge in der Kopfzeilencachetabelle sollten verarbeitet werden, alle nachrichten, die mit dem flag MSGSTATUS_REMOTE_DOWNLOAD gekennzeichnet sind, heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE gekennzeichnet sind, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="bc46e-129">Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt sind, sollten verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="bc46e-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bc46e-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bc46e-131">Für einen Remotetransportanbieter sollte eine neue Liste von Nachrichtenkopfzeilen heruntergeladen werden, und alle Kennzeichen, die den Nachrichtenstatus markieren, sollten entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="bc46e-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="bc46e-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="bc46e-133">Verhindert, dass das Statusobjekt eine Benutzeroberfläche im Rahmen des Vorgangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc46e-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc46e-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc46e-134">Return value</span></span>

<span data-ttu-id="bc46e-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc46e-135">S_OK</span></span> 
  
> <span data-ttu-id="bc46e-136">Die Überprüfung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bc46e-136">The validation was successful.</span></span>
    
<span data-ttu-id="bc46e-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="bc46e-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="bc46e-138">Ein weiterer Vorgang wird ausgeführt. Er sollte abgeschlossen oder beendet werden dürfen, bevor dieser Vorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc46e-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="bc46e-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bc46e-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bc46e-140">Das status-Objekt unterstützt die Überprüfungsmethode nicht, wie durch das Fehlen des STATUS_VALIDATE_STATE-Flag in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc46e-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="bc46e-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bc46e-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="bc46e-142">Der Benutzer hat den Überprüfungsvorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="bc46e-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="bc46e-143">Dieser Wert wird nur von Remote-Transport-Anbietern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc46e-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bc46e-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc46e-144">Remarks</span></span>

<span data-ttu-id="bc46e-145">Die **IMAPIStatus::ValidateState-Methode** überprüft den Status einer Ressource, die einem Statusobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bc46e-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="bc46e-146">**ValidateState** ist die einzige Methode in der [IMAPIStatus-Schnittstelle,](imapistatusimapiprop.md) die für alle Statusobjekte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bc46e-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="bc46e-147">Das genaue Verhalten dieser Methode hängt von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="bc46e-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="bc46e-148">In der folgenden Tabelle wird die Implementierung der einzelnen Typen von Statusobjekten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bc46e-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="bc46e-149">**Status-Objekt**</span><span class="sxs-lookup"><span data-stu-id="bc46e-149">**Status object**</span></span>|<span data-ttu-id="bc46e-150">ValidateState**-Implementierung**</span><span class="sxs-lookup"><span data-stu-id="bc46e-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc46e-151">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="bc46e-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="bc46e-152">Überprüft den Status aller Ressourcen, die die derzeit aktiven Dienstanbieter und das Subsystem selbst besitzen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="bc46e-153">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="bc46e-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="bc46e-154">Führt eine Anmeldung aller Transportanbieter aus, unabhängig davon, ob sie bereits angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="bc46e-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="bc46e-155">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="bc46e-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="bc46e-156">Überprüft die Einträge im Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="bc46e-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="bc46e-157">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="bc46e-157">Service provider</span></span>  <br/> |<span data-ttu-id="bc46e-158">Die Implementierung hängt vom Typ des Anbieters und den im  _ulFlags-Parameter festgelegten Flags_ ab.</span><span class="sxs-lookup"><span data-stu-id="bc46e-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="bc46e-159">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="bc46e-159">Notes to implementers</span></span>

<span data-ttu-id="bc46e-160">Remoteclientanwendungen rufen die **ValidateState-Methode** auf, um die Remoteverarbeitung für verschiedene Aktionen zu starten.</span><span class="sxs-lookup"><span data-stu-id="bc46e-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="bc46e-161">Diese Methode ist in erster Linie zum Festlegen von Statusbits für die Kommunikation mit dem MAPI-Spooler vorhanden, anstatt tatsächlich arbeit zu tun.</span><span class="sxs-lookup"><span data-stu-id="bc46e-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="bc46e-162">In der Regel legt der Transportanbieter Flags in seiner Statuszeile fest, die dem MAPI-Spooler angeben, welche Aktionen zum Abschließen der Clientanforderung initiiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="bc46e-163">In diesem Modell der Client-Transport-Spooler-Interaktion sind die vom Client angeforderten Aktionen asynchron, da **ValidateState** zurückgibt, bevor die angeforderten Aktionen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="bc46e-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="bc46e-164">Aktionen, die nicht unbedingt das zugrunde liegende Messagingsystem oder eine transportspezifische Schnittstelle betreffen, können jedoch synchron sein.</span><span class="sxs-lookup"><span data-stu-id="bc46e-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="bc46e-165">Die Clientanwendung übergibt eine Bitmaske der folgenden Flags, um anzugeben, welche Aktionen der Remotetransportanbieter ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="bc46e-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="bc46e-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="bc46e-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="bc46e-167">Wenn möglich, sollte der Remotetransportanbieter alle Vorgänge abbrechen, die das Herunterladen von Kopfzeilen beinhalten.</span><span class="sxs-lookup"><span data-stu-id="bc46e-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="bc46e-168">Dazu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des Anmeldeobjekts festlegen:</span><span class="sxs-lookup"><span data-stu-id="bc46e-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="bc46e-169">Löschen Sie STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE bits in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) -Eigenschaft, um den #A0 anzuhalten, den eingehenden Leervorgang für diesen Transportanbieter zu stoppen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="bc46e-170">Legen Sie STATUS_OFFLINE-Bit in der **PR_STATUS_CODE-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="bc46e-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bc46e-171">Legen Sie **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) -Eigenschaft auf TRUE.</span><span class="sxs-lookup"><span data-stu-id="bc46e-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="bc46e-172">Legen Sie **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) -Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="bc46e-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="bc46e-173">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="bc46e-173">Return S_OK.</span></span> <span data-ttu-id="bc46e-174">Wenn der ausgeführte Vorgang jedoch nicht abgebrochen werden kann, sollte **ValidateState** MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="bc46e-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="bc46e-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="bc46e-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="bc46e-176">Ein Remote-Transport-Anbieter sollte nie eine Verbindung mit einer freigegebenen Ressource (z. B. einem Modem oder EINEM COM-Port) außerhalb des Kontexts der MAPI-Spooler-Transport-Interaktion herstellen, die an der [IXPLogon::FlushQueues-Methode](ixplogon-flushqueues.md) beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="bc46e-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="bc46e-177">Wenn **ValidateState** mit diesem Flag aufgerufen wird, sollte Ihr Transportanbieter die folgenden Schritte unternehmen:</span><span class="sxs-lookup"><span data-stu-id="bc46e-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="bc46e-178">Legen Sie ein internes Statusflag fest, um anzugeben, dass die Remoteverbindung hergestellt werden muss, wenn die **IXPLogon::FlushQueues-Methode** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bc46e-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="bc46e-179">Legen Sie die richtigen Werte in der Statustabelle so ein, dass der MAPI-Spooler den Warteschlangenleervorgang initiiert.</span><span class="sxs-lookup"><span data-stu-id="bc46e-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="bc46e-180">Wenn das Leeren von Warteschlangen abgeschlossen ist, geben Sie die freigegebene Ressource frei.</span><span class="sxs-lookup"><span data-stu-id="bc46e-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="bc46e-181">Löschen Sie STATUS_OFFLINE-Bit in  der PR_STATUS_CODE-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bc46e-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bc46e-182">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="bc46e-182">Return S_OK.</span></span>
    
<span data-ttu-id="bc46e-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="bc46e-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="bc46e-184">Der Remotetransportanbieter sollte seine Verbindung zu den Messagingsystemressourcen frei geben.</span><span class="sxs-lookup"><span data-stu-id="bc46e-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="bc46e-185">Anschließend sollte das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE-Eigenschaft** festgelegt und S_OK.</span><span class="sxs-lookup"><span data-stu-id="bc46e-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="bc46e-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bc46e-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bc46e-187">Der Remotetransportanbieter sollte Remotenachrichten verarbeiten und alle zurückgestellten Nachrichten hochladen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="bc46e-188">Dazu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des Anmeldeobjekts festlegen:</span><span class="sxs-lookup"><span data-stu-id="bc46e-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="bc46e-189">Legen Sie **PR_STATUS_STRING** auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="bc46e-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="bc46e-190">Legen Sie die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE in der **PR_STATUS_CODE-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="bc46e-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bc46e-191">Legen Sie **PR_REMOTE_VALIDATE_OK** eigenschaft in der Statuszeile des Transportanbieters auf FALSE.</span><span class="sxs-lookup"><span data-stu-id="bc46e-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="bc46e-192">Wenn ein anderer Vorgang ausgeführt wird (z. B. das Herunterladen von Kopfzeilen), wenn **ValidateState** aufgerufen wird, sollte **ValidateState** MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="bc46e-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="bc46e-193">Führen Sie den Code für die Verarbeitung des REFRESH_XP_HEADER_CACHE aus, um die Anforderungen des Microsoft-Exchange erfüllen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="bc46e-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bc46e-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bc46e-195">Der Remotetransportanbieter sollte alle neuen Nachrichtenkopfzeilen aus dem Messagingsystem abrufen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="bc46e-196">Dazu muss der Transportanbieter die folgenden Schritte tun:</span><span class="sxs-lookup"><span data-stu-id="bc46e-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="bc46e-197">Legen Sie **PR_STATUS_STRING** auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="bc46e-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="bc46e-198">Legen Sie die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE in der **PR_STATUS_CODE-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="bc46e-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bc46e-199">Löschen Sie STATUS_OFFLINE-Bit in  der PR_STATUS_CODE-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bc46e-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bc46e-200">Legen Sie STATUS_ONLINE-Bit in der **PR_STATUS_CODE-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="bc46e-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bc46e-201">Legen Sie **PR_REMOTE_VALIDATE_OK** eigenschaft in der Statuszeile des Transportanbieters auf FALSE.</span><span class="sxs-lookup"><span data-stu-id="bc46e-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="bc46e-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="bc46e-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="bc46e-203">Wenn Ihr Transportanbieter über eine Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen verfügt (z. B. ein Dialogfeld, das das Herunterladen von Nachrichten bestätigt), sollte dieses Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="bc46e-204">Andernfalls **kann ValidateState** MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="bc46e-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="bc46e-205">Wenn andere Kennzeichen als diese übergeben werden, sollte **ValidateState** MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="bc46e-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="bc46e-206">Der Clientaufruf an den Transportanbieter wird häufig an die **IMAPIStatus::ValidateState-Methode** gesendet.</span><span class="sxs-lookup"><span data-stu-id="bc46e-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="bc46e-207">Während der Verarbeitung von **ValidateState** sollte der Transportanbieter keine Aktionen ausführen, die knappe Systemressourcen zuweisen, z. B. ein Modem oder einen COM-Port.</span><span class="sxs-lookup"><span data-stu-id="bc46e-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="bc46e-208">Dies liegt daran, dass der MAPI-Spooler manchmal Warteschlangen für mehrere Transportanbieter leeren muss.</span><span class="sxs-lookup"><span data-stu-id="bc46e-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="bc46e-209">Der Client kann jedoch jederzeit die **ValidateState-Methode** eines beliebigen Transportanbieters aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="bc46e-210">Wenn Ihr Transportanbieter versucht, während der Verarbeitung von **ValidateState** eine knappe Ressource zuzuordnen, kann ein Fehler aufgrund eines Konflikts mit einem anderen Transportanbieter verursacht werden, den der MAPI-Spooler angewiesen hat, seine Warteschlangen zu leeren.</span><span class="sxs-lookup"><span data-stu-id="bc46e-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="bc46e-211">Wenn Sie zulassen, dass alle knappen Ressourcenzuweisungen unter der Richtung des MAPI-Spoolers erfolgen, können Sie solche Konflikte vermeiden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="bc46e-212">Ihr Transportanbieter sollte die **PR_REMOTE_VALIDATE_OK-Eigenschaft** unterstützen, damit Clientanwendungen erkennen können, wann Ihr Transportanbieter ausgelastet ist oder darauf wartet, dass der MAPI-Spooler eine Aktion initiiert.</span><span class="sxs-lookup"><span data-stu-id="bc46e-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bc46e-213">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="bc46e-213">Notes to callers</span></span>

<span data-ttu-id="bc46e-214">Da diese Methode dazu führen kann, dass andere potenziell langwierige Aufrufe vorgenommen werden, kann **ValidateState** MAPI_E_BUSY zurückgeben, um Sie darüber zu informieren, dass diese Methode auf den Abschluss eines anderen Vorgangs wartet.</span><span class="sxs-lookup"><span data-stu-id="bc46e-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="bc46e-215">Sie sollten warten, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie eine andere Aufgabe versuchen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="bc46e-216">Sie haben die größte Kontrolle über Ihre Aufrufe an Statusobjekte des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="bc46e-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="bc46e-217">Sie können ein oder mehrere Flags an **ValidateState** übergeben, die sich auf die Vorgänge des Transportanbieters auswirken.</span><span class="sxs-lookup"><span data-stu-id="bc46e-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="bc46e-218">Das Flag ABORT_XP_HEADER_OPERATION z. B. an, dass der Benutzer die Überprüfung abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="bc46e-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="bc46e-219">Transportanbieter können sich für einen Abbruch entscheiden, MAPI_E_USER_CANCELED zurückgeben oder fortfahren.</span><span class="sxs-lookup"><span data-stu-id="bc46e-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="bc46e-220">Sie können das CONFIG_CHANGED für einen Aufruf des Statusobjekts eines Dienstanbieters oder des MAPI-Spoolers festlegen, um anzugeben, dass eine Konfigurationsoption geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="bc46e-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="bc46e-221">Sie können die CONFIG_CHANGED verwenden, um einen Transportanbieter dynamisch neu zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bc46e-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="bc46e-222">Wenn Sie CONFIG_CHANGED einem Aufruf des Statusobjekts eines Dienstanbieters festlegen, antwortet der Anbieter mit einem Aufruf von [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) um den MAPI-Spooler über die Änderung zu warnen.</span><span class="sxs-lookup"><span data-stu-id="bc46e-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="bc46e-223">Wenn Sie CONFIG_CHANGED Aufruf des Statusobjekts des MAPI-Spoolers festlegen, ruft der Spooler [IXPLogon::AddressTypes](ixplogon-addresstypes.md) für jeden aktiven Transportanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="bc46e-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="bc46e-224">**AddressTypes** informiert den MAPI-Spooler über die unterstützten Adresstypen eines Transports.</span><span class="sxs-lookup"><span data-stu-id="bc46e-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="bc46e-225">Einige Dienstanbieter zeigen auch einen Fortschrittsindikator an, wenn die Überprüfung voraussichtlich sehr lange dauert.</span><span class="sxs-lookup"><span data-stu-id="bc46e-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="bc46e-226">Das Anzeigen eines Statusindikators ist hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc46e-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="bc46e-227">Wenn das SUPPRESS_UI festgelegt ist, können keines der Konfigurationseigenschaftsblätter oder Statusdialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bc46e-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc46e-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc46e-228">See also</span></span>

- [<span data-ttu-id="bc46e-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="bc46e-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="bc46e-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="bc46e-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="bc46e-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="bc46e-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="bc46e-232">PidTagRemoteValidateOk (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc46e-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="bc46e-233">PidTagResourceMethods (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc46e-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="bc46e-234">PidTagStatusCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc46e-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="bc46e-235">PidTagStatusString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc46e-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="bc46e-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bc46e-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)


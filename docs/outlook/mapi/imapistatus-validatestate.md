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
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331549"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="24e54-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="24e54-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="24e54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24e54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24e54-105">Bestätigt die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="24e54-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="24e54-106">Diese Methode wird in allen Status-Objekten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24e54-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="24e54-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="24e54-107">Parameters</span></span>

<span data-ttu-id="24e54-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="24e54-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="24e54-109">in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="24e54-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="24e54-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24e54-110">_ulFlags_</span></span>
  
> <span data-ttu-id="24e54-111">in Eine Bitmaske von Flags, die die Validierung steuert.</span><span class="sxs-lookup"><span data-stu-id="24e54-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="24e54-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="24e54-112">The following flags can be set:</span></span>
    
<span data-ttu-id="24e54-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="24e54-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="24e54-114">Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im entsprechenden Dialogfeld geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="24e54-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="24e54-115">Das Status-Objekt verfügt über zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="24e54-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="24e54-116">Arbeiten Sie weiterhin an dem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="24e54-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="24e54-117">Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="24e54-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="24e54-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="24e54-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="24e54-119">Eine oder mehrere der Konfigurationseigenschaften des Status-Objekts wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="24e54-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="24e54-120">Clients können dieses Flag festlegen, um zu ermöglichen, dass der MAPI-Spooler kritische Transportanbieter Fehler dynamisch korrigiert.</span><span class="sxs-lookup"><span data-stu-id="24e54-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="24e54-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="24e54-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="24e54-122">Das Status-Objekt sollte eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="24e54-122">The status object should perform a connection.</span></span> <span data-ttu-id="24e54-123">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE-oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, erfolgt die Verbindung ohne Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="24e54-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="24e54-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="24e54-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="24e54-125">Das Status-Objekt sollte einen Disconnect-Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="24e54-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="24e54-126">Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE-oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, erfolgt die Trennung ohne Zwischenspeicherung.</span><span class="sxs-lookup"><span data-stu-id="24e54-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="24e54-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="24e54-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="24e54-128">Einträge in der Kopfzeile-Cache-Tabelle sollten verarbeitet werden, alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag gekennzeichnet sind, sollten heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet sind, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="24e54-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="24e54-129">Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="24e54-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="24e54-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="24e54-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="24e54-131">Bei einem Remote Transportanbieter sollte eine neue Liste mit Nachrichtenkopfzeilen heruntergeladen werden, und alle Kennzeichnungen, die den Nachrichtenstatus markieren, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="24e54-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="24e54-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="24e54-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="24e54-133">Verhindert, dass das Statusobjekt eine Benutzeroberfläche als Teil des Vorgangs anzeigt.</span><span class="sxs-lookup"><span data-stu-id="24e54-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24e54-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24e54-134">Return value</span></span>

<span data-ttu-id="24e54-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="24e54-135">S_OK</span></span> 
  
> <span data-ttu-id="24e54-136">Die Überprüfung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="24e54-136">The validation was successful.</span></span>
    
<span data-ttu-id="24e54-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="24e54-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="24e54-138">Ein anderer Vorgang wird ausgeführt; Sie sollte zugelassen werden, oder Sie sollte beendet werden, bevor dieser Vorgang eingeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="24e54-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="24e54-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="24e54-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="24e54-140">Das Status-Objekt unterstützt die Validierungsmethode nicht, wie durch das Fehlen des STATUS_VALIDATE_STATE-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="24e54-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="24e54-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="24e54-142">Der Benutzer hat den Validierungsvorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="24e54-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="24e54-143">Dieser Wert wird nur von Remote Transportanbietern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="24e54-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24e54-144">Remarks</span></span>

<span data-ttu-id="24e54-145">Die **IMAPIStatus:: ValidateState** -Methode überprüft den Status einer Ressource, die einem Statusobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="24e54-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="24e54-146">**ValidateState** ist die einzige Methode in der [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle, die für alle Status-Objekte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="24e54-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="24e54-147">Das genaue Verhalten dieser Methode hängt von der Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="24e54-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="24e54-148">In der folgenden Tabelle wird die Implementierung der einzelnen Arten von Statusobjekten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="24e54-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="24e54-149">**Status-Objekt**</span><span class="sxs-lookup"><span data-stu-id="24e54-149">**Status object**</span></span>|<span data-ttu-id="24e54-150">ValidateState \* \* Implementierung \* \*</span><span class="sxs-lookup"><span data-stu-id="24e54-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="24e54-151">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="24e54-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="24e54-152">Überprüft den Status aller Ressourcen, die die derzeit aktiven Dienstanbieter und das Subsystem selbst besitzen.</span><span class="sxs-lookup"><span data-stu-id="24e54-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="24e54-153">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="24e54-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="24e54-154">Führt eine Anmeldung aller Transportanbieter aus, unabhängig davon, ob Sie bereits angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="24e54-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="24e54-155">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="24e54-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="24e54-156">Überprüft die Einträge im Profil Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="24e54-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="24e54-157">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="24e54-157">Service provider</span></span>  <br/> |<span data-ttu-id="24e54-158">Die Implementierung hängt vom Anbietertyp und den im _ulFlags_ -Parameter festgelegten Flags ab.</span><span class="sxs-lookup"><span data-stu-id="24e54-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="24e54-159">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="24e54-159">Notes to implementers</span></span>

<span data-ttu-id="24e54-160">Remote Clientanwendungen rufen die **ValidateState** -Methode auf, um die Remoteverarbeitung für verschiedene Aktionen zu starten.</span><span class="sxs-lookup"><span data-stu-id="24e54-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="24e54-161">Diese Methode besteht hauptsächlich darin, Statusbits für die Kommunikation mit dem MAPI-Spooler festzulegen, statt tatsächlich arbeiten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="24e54-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="24e54-162">In der Regel legt der Transportanbieter Flags in der Statuszeile fest, die dem MAPI-Spooler zeigen, welche Aktionen initiiert werden müssen, um die Anforderung des Clients abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="24e54-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="24e54-163">In diesem Modell der Client-Transport-Spooler-Interaktion sind die vom Client angeforderten Aktionen asynchron, da **ValidateState** zurückgegeben wird, bevor die angeforderten Aktionen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="24e54-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="24e54-164">Aktionen, die nicht notwendigerweise das zugrunde liegende Messagingsystem oder eine transportspezifische Schnittstelle beinhalten, können jedoch synchron sein.</span><span class="sxs-lookup"><span data-stu-id="24e54-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="24e54-165">Die Clientanwendung übergibt eine Bitmaske der folgenden Flags, um anzugeben, welche Aktionen vom Remote Transportanbieter ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24e54-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="24e54-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="24e54-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="24e54-167">Wenn möglich, sollte der Remote Transportanbieter alle Vorgänge abbrechen, die das Herunterladen von Kopfzeilen beinhalten.</span><span class="sxs-lookup"><span data-stu-id="24e54-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="24e54-168">Hierzu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des LOGON-Objekts festlegen:</span><span class="sxs-lookup"><span data-stu-id="24e54-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="24e54-169">Löschen Sie die STATUS_INBOUND_ENABLED-und STATUS_INBOUND_ACTIVE-Bits in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft, um dem MAPI-Spooler mitzuteilen, dass der Prozess für eingehende Flush für diesen Transportanbieter angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="24e54-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="24e54-170">Legen Sie das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="24e54-171">Legen Sie die **PR_REMOTE_VALIDATE_OK** ([pidtagremotevalidateok (](pidtagremotevalidateok-canonical-property.md))-Eigenschaft auf true fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="24e54-172">Legen Sie die **PR_STATUS_STRING** ([pidtagstatusstring (](pidtagstatusstring-canonical-property.md))-Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="24e54-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="24e54-173">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="24e54-173">Return S_OK.</span></span> <span data-ttu-id="24e54-174">Wenn jedoch der laufende Vorgang nicht abgebrochen werden kann, sollte **VALIDATESTATE** MAPI_E_BUSY zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="24e54-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="24e54-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="24e54-176">Ein Remote Transportanbieter sollte niemals eine Verbindung zu einer freigegebenen Ressource (beispielsweise einem Modem oder COM-Anschluss) außerhalb des Kontexts der MAPI-Spooler-Transport Interaktion herstellen, die an der [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) -Methode beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="24e54-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="24e54-177">Wenn **ValidateState** mit diesem Flag aufgerufen wird, sollte der Transportanbieter folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="24e54-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="24e54-178">Legen Sie ein internes Statuskennzeichen fest, um anzugeben, dass die Remoteverbindung hergestellt werden muss, wenn die **IXPLogon:: FlushQueues** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="24e54-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="24e54-179">Legen Sie die richtigen Werte in der Statustabelle fest, damit der MAPI-Spooler den Prozess der Warteschlangen Bereinigung initiiert.</span><span class="sxs-lookup"><span data-stu-id="24e54-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="24e54-180">Wenn das Leeren der Warteschlangen abgeschlossen ist, lassen Sie die freigegebene Ressource frei.</span><span class="sxs-lookup"><span data-stu-id="24e54-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="24e54-181">Löschen Sie das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="24e54-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="24e54-182">Geben Sie S_OK zur�ck.</span><span class="sxs-lookup"><span data-stu-id="24e54-182">Return S_OK.</span></span>
    
<span data-ttu-id="24e54-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="24e54-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="24e54-184">Der Remote Transportanbieter sollte seine Verbindung mit den Messagingsystem Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="24e54-185">Anschließend sollte das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft festgelegt und S_OK zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24e54-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="24e54-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="24e54-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="24e54-187">Der Remote Transportanbieter sollte Remotenachrichten verarbeiten und alle verzögerten Nachrichten hochladen.</span><span class="sxs-lookup"><span data-stu-id="24e54-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="24e54-188">Hierzu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des LOGON-Objekts festlegen:</span><span class="sxs-lookup"><span data-stu-id="24e54-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="24e54-189">Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="24e54-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="24e54-190">Legen Sie die STATUS_OUTBOUND_ENABLED-und STATUS_OUTBOUND_ACTIVE-Bits in der **PR_STATUS_CODE** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="24e54-191">Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Statuszeile des Transportanbieters auf false fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="24e54-192">Wenn ein anderer Vorgang ausgeführt wird (beispielsweise das Herunterladen von Kopfzeilen), wenn **ValidateState** aufgerufen wird, sollte **ValidateState** MAPI_E_BUSY zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="24e54-193">Führen Sie den Code für die Verarbeitung des REFRESH_XP_HEADER_CACHE-Flags aus, um die Anforderungen des Microsoft Exchange-Clients zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="24e54-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="24e54-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="24e54-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="24e54-195">Der Remote Transportanbieter sollte neue Nachrichtenkopfzeilen aus dem Messagingsystem abrufen.</span><span class="sxs-lookup"><span data-stu-id="24e54-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="24e54-196">Hierzu muss der Transportanbieter folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="24e54-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="24e54-197">Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="24e54-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="24e54-198">Legen Sie die STATUS_INBOUND_ENABLED-und STATUS_INBOUND_ACTIVE-Bits in der **PR_STATUS_CODE** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="24e54-199">Löschen Sie das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="24e54-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="24e54-200">Legen Sie das STATUS_ONLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="24e54-201">Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Statuszeile des Transportanbieters auf false fest.</span><span class="sxs-lookup"><span data-stu-id="24e54-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="24e54-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="24e54-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="24e54-203">Wenn Ihr Transportanbieter über Teile der Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen verfügt (beispielsweise ein Dialogfeld, das das Herunterladen von Nachrichten bestätigt), sollte dieses Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="24e54-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="24e54-204">Andernfalls kann **VALIDATESTATE** MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="24e54-205">Wenn andere Flags als diese übergeben werden, sollte **VALIDATESTATE** MAPI_E_UNKNOWN_FLAGS zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="24e54-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="24e54-206">Der Aufruf des Clients an den Transportanbieter erfolgt häufig über die **IMAPIStatus:: ValidateState** -Methode.</span><span class="sxs-lookup"><span data-stu-id="24e54-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="24e54-207">Während der Verarbeitung von **ValidateState**sollte der Transportanbieter keine Aktionen ausführen, die knappe Systemressourcen wie ein Modem oder einen COM-Anschluss zuweisen.</span><span class="sxs-lookup"><span data-stu-id="24e54-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="24e54-208">Der Grund dafür ist, dass der MAPI-Spooler manchmal Warteschlangen für mehrere Transportanbieter leeren muss.</span><span class="sxs-lookup"><span data-stu-id="24e54-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="24e54-209">Der Client kann jedoch jederzeit die **ValidateState** -Methode eines beliebigen Transportanbieters aufrufen.</span><span class="sxs-lookup"><span data-stu-id="24e54-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="24e54-210">Wenn Ihr Transportanbieter versucht, eine knappe Ressource während der Verarbeitung von **ValidateState**zu reservieren, kann ein Fehler aufgrund eines Konflikts mit einem anderen Transportanbieter verursacht werden, den der MAPI-Spooler angewiesen hat, seine Warteschlangen zu leeren.</span><span class="sxs-lookup"><span data-stu-id="24e54-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="24e54-211">Wenn Sie zulassen, dass alle knappen Ressourcenzuordnungen unter der Richtung des MAPI-Spoolers auftreten, können Sie solche Konflikte vermeiden.</span><span class="sxs-lookup"><span data-stu-id="24e54-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="24e54-212">Der Transportanbieter sollte die **PR_REMOTE_VALIDATE_OK** -Eigenschaft unterstützen, damit Clientanwendungen feststellen können, ob der Transportanbieter ausgelastet ist oder darauf wartet, dass der MAPI-Spooler eine Aktion initiiert.</span><span class="sxs-lookup"><span data-stu-id="24e54-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="24e54-213">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="24e54-213">Notes to callers</span></span>

<span data-ttu-id="24e54-214">Da diese Methode andere potenziell langwierige Aufrufe auslösen kann, kann **VALIDATESTATE** MAPI_E_BUSY zurückgeben, um Sie darüber zu informieren, dass diese Methode auf den Abschluss eines anderen Vorgangs wartet.</span><span class="sxs-lookup"><span data-stu-id="24e54-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="24e54-215">Sie sollten warten, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie eine andere Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="24e54-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="24e54-216">Sie haben die größte Kontrolle über Ihre Aufrufe an Transportanbieter Status-Objekte.</span><span class="sxs-lookup"><span data-stu-id="24e54-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="24e54-217">Sie können ein oder mehrere Flags an **ValidateState** , die sich auf die Vorgänge des Transportanbieters auswirken.</span><span class="sxs-lookup"><span data-stu-id="24e54-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="24e54-218">Das ABORT_XP_HEADER_OPERATION-Flag gibt beispielsweise an, dass der Benutzer die Validierung abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="24e54-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="24e54-219">Transport Anbieter können entscheiden, ob Sie abgebrochen werden, MAPI_E_USER_CANCELED zurückgeben oder fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="24e54-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="24e54-220">Sie können das CONFIG_CHANGED-Flag für einen Aufruf entweder an das Status-Objekt eines Dienstanbieters oder an den MAPI-Spooler festlegen, um anzugeben, dass eine Konfigurationsoption geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="24e54-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="24e54-221">Sie können CONFIG_CHANGED verwenden, um einen Transportanbieter dynamisch neu zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="24e54-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="24e54-222">Wenn Sie CONFIG_CHANGED für einen Aufruf des Status Objekts eines Dienstanbieters festlegen, antwortet der Anbieter mit einem Aufruf von [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) , um den MAPI-Spooler der Änderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="24e54-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="24e54-223">Wenn Sie CONFIG_CHANGED für einen Aufruf des Status Objekts des MAPI-Spoolers festlegen, ruft der Spooler [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) für jeden aktiven Transportanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="24e54-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="24e54-224">**AddressTypes** informiert den MAPI-Spooler über die unterstützten Adresstypen eines Transports.</span><span class="sxs-lookup"><span data-stu-id="24e54-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="24e54-225">Einige Dienstanbieter zeigen auch eine Statusanzeige an, wenn die Überprüfung sehr lange dauern wird.</span><span class="sxs-lookup"><span data-stu-id="24e54-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="24e54-226">Das Anzeigen einer Statusanzeige ist hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="24e54-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="24e54-227">Wenn das SUPPRESS_UI-Flag festgelegt ist, können keine der Konfigurationseigenschaften Blätter oder Fortschritts Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="24e54-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24e54-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24e54-228">See also</span></span>

- [<span data-ttu-id="24e54-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="24e54-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="24e54-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="24e54-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="24e54-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="24e54-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="24e54-232">Kanonische Pidtagremotevalidateok (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24e54-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="24e54-233">Kanonische Pidtagresourcemethods (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24e54-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="24e54-234">Kanonische Pidtagstatuscode (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24e54-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="24e54-235">Kanonische Pidtagstatusstring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24e54-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="24e54-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="24e54-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)


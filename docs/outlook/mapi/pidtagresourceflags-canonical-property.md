---
title: Kanonische Pidtagresourceflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330184"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="4eb75-103">Kanonische Pidtagresourceflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4eb75-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4eb75-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4eb75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4eb75-105">Enthält eine Bitmaske von Flags für Nachrichtendienste und Anbieter.</span><span class="sxs-lookup"><span data-stu-id="4eb75-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4eb75-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4eb75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4eb75-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4eb75-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="4eb75-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4eb75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4eb75-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="4eb75-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="4eb75-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4eb75-110">Data type:</span></span>  <br/> |<span data-ttu-id="4eb75-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4eb75-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4eb75-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4eb75-112">Area:</span></span>  <br/> |<span data-ttu-id="4eb75-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="4eb75-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4eb75-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eb75-114">Remarks</span></span>

<span data-ttu-id="4eb75-115">Diese Eigenschaft beschreibt die Merkmale eines Nachrichtendiensts, eines Dienstanbieters oder eines Status Objekts.</span><span class="sxs-lookup"><span data-stu-id="4eb75-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="4eb75-116">Die für diese Eigenschaft festgelegten Flags hängen vom jeweiligen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="4eb75-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="4eb75-117">Beispielsweise sind einige Flags nur für Statusobjekte und andere Flags nur für Spalten in der Nachrichtendienst Tabelle gültig.</span><span class="sxs-lookup"><span data-stu-id="4eb75-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="4eb75-118">Die Flags bestehen aus drei Klassen: statisch, änderbar und dynamisch.</span><span class="sxs-lookup"><span data-stu-id="4eb75-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="4eb75-119">Statische Flags werden von Daten in MAPISVC von MAPI festgelegt. INF und nie geändert.</span><span class="sxs-lookup"><span data-stu-id="4eb75-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="4eb75-120">Veränderbare Flags werden von MAPI von MAPISVC festgelegt. INF kann aber nachträglich geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="4eb75-121">Dynamische Kennzeichnungen können durch MAPI-Methoden festgelegt und zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="4eb75-122">Bei einem Nachrichtendienst können eine oder mehrere der folgenden Flags in dieser Eigenschaft festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4eb75-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="4eb75-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="4eb75-124">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4eb75-124">Reserved.</span></span> <span data-ttu-id="4eb75-125">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-125">Do not use.</span></span>
    
<span data-ttu-id="4eb75-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="4eb75-127">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-127">Dynamic.</span></span> <span data-ttu-id="4eb75-128">Der Nachrichtendienst enthält den Standardspeicher.</span><span class="sxs-lookup"><span data-stu-id="4eb75-128">The message service contains the default store.</span></span> <span data-ttu-id="4eb75-129">Es sollte eine Benutzeroberfläche angezeigt werden, in der der Benutzer zur Bestätigung aufgefordert wird, bevor dieser Dienst aus dem Profil gelöscht oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4eb75-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="4eb75-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="4eb75-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="4eb75-131">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-131">Static.</span></span> <span data-ttu-id="4eb75-132">Das Dienst Level-Flag, das festgelegt werden sollte, um anzugeben, dass keiner der Anbieter im Nachrichtendienst zur Bereitstellung einer Identität verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4eb75-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="4eb75-133">Entweder dieses Flag oder SERVICE_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="4eb75-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="4eb75-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="4eb75-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="4eb75-135">Änderbaren.</span><span class="sxs-lookup"><span data-stu-id="4eb75-135">Modifiable.</span></span> <span data-ttu-id="4eb75-136">Der entsprechende Nachrichtendienst enthält den Anbieter, der für die primäre Identität für diese Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4eb75-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="4eb75-137">Verwenden Sie [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) , um dieses Flag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4eb75-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="4eb75-138">Entweder dieses Flag oder SERVICE_NO_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="4eb75-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="4eb75-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="4eb75-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="4eb75-140">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-140">Static.</span></span> <span data-ttu-id="4eb75-141">Jeder Versuch, diesen Nachrichtendienst in ein Profil zu erstellen oder zu kopieren, in dem der Dienst bereits vorhanden ist, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="4eb75-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="4eb75-142">So erstellen Sie einen Einzelkopiecluster-Dienst fügen Sie die **PR_RESOURCE_FLAGS** -Eigenschaft zum Abschnitt des Diensts in Mapisvc hinzu. INF, und legen Sie dieses Flag fest.</span><span class="sxs-lookup"><span data-stu-id="4eb75-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="4eb75-143">Bei einem Dienstanbieter kann eine oder mehrere der folgenden Flags in **PR_RESOURCE_FLAGS**festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4eb75-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="4eb75-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="4eb75-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="4eb75-145">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-145">Static.</span></span> <span data-ttu-id="4eb75-146">Der Spooler-Hook muss eingehende Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4eb75-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="4eb75-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="4eb75-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="4eb75-148">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-148">Static.</span></span> <span data-ttu-id="4eb75-149">Der Spooler-Hook muss ausgehende Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4eb75-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="4eb75-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="4eb75-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="4eb75-151">Änderbaren.</span><span class="sxs-lookup"><span data-stu-id="4eb75-151">Modifiable.</span></span> <span data-ttu-id="4eb75-152">Diese Identität sollte auf ausgehende Nachrichten angewendet werden, wenn das Profil mehrere Instanzen dieses Transportanbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="4eb75-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="4eb75-153">Dies kann passieren, wenn mehrere Instanzen eines einzelnen Transportanbieters im Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="4eb75-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="4eb75-155">Änderbaren.</span><span class="sxs-lookup"><span data-stu-id="4eb75-155">Modifiable.</span></span> <span data-ttu-id="4eb75-156">Dieser Nachrichtenspeicher ist der Standardspeicher für das Profil.</span><span class="sxs-lookup"><span data-stu-id="4eb75-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="4eb75-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="4eb75-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="4eb75-158">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-158">Dynamic.</span></span> <span data-ttu-id="4eb75-159">Die Standardordner in diesem Nachrichtenspeicher, einschließlich des Stammordners für die zwischenmenschlichen Nachrichten (IPM), wurden noch nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="4eb75-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="4eb75-160">Das Flag wird von MAPI festgelegt und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4eb75-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="4eb75-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="4eb75-162">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-162">Static.</span></span> <span data-ttu-id="4eb75-163">Dieser Nachrichtenspeicher kann nicht zum Standardnachrichtenspeicher für das Profil werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="4eb75-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="4eb75-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="4eb75-165">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-165">Static.</span></span> <span data-ttu-id="4eb75-166">Dieser Anbieter liefert keine Identität in der Statuszeile.</span><span class="sxs-lookup"><span data-stu-id="4eb75-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="4eb75-167">Entweder dieses Flag oder STATUS_PRIMARY_IDENTITY muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="4eb75-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="4eb75-169">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-169">Static.</span></span> <span data-ttu-id="4eb75-170">Dieser Transportanbieter ist eng mit einem Nachrichtenspeicher gekoppelt und liefert die **PR_OWN_STORE_ENTRYID** ([pidtagownstoreentryid (](pidtagownstoreentryid-canonical-property.md))-Eigenschaft in der Statuszeile.</span><span class="sxs-lookup"><span data-stu-id="4eb75-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="4eb75-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="4eb75-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="4eb75-172">Änderbaren.</span><span class="sxs-lookup"><span data-stu-id="4eb75-172">Modifiable.</span></span> <span data-ttu-id="4eb75-173">Dieser Anbieter liefert die primäre Identität für die Sitzung; die Eintrags-ID für das Objekt, das die Identität eingibt, wird von [IMAPISession:: QueryIdentity](imapisession-queryidentity.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4eb75-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="4eb75-174">Entweder dieses Flag oder **STATUS_NO_PRIMARY_IDENTITY** muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="4eb75-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="4eb75-176">Änderbaren.</span><span class="sxs-lookup"><span data-stu-id="4eb75-176">Modifiable.</span></span> <span data-ttu-id="4eb75-177">Dieser Nachrichtenspeicher soll verwendet werden, wenn sich eine Clientanwendung anmeldet.</span><span class="sxs-lookup"><span data-stu-id="4eb75-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="4eb75-178">Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="4eb75-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="4eb75-180">Änderbaren.</span><span class="sxs-lookup"><span data-stu-id="4eb75-180">Modifiable.</span></span> <span data-ttu-id="4eb75-181">Dieser Nachrichtenspeicher soll verwendet werden, wenn der primäre Speicher nicht verfügbar ist, wenn sich eine Clientanwendung anmeldet.</span><span class="sxs-lookup"><span data-stu-id="4eb75-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="4eb75-182">Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb75-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="4eb75-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="4eb75-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="4eb75-184">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-184">Dynamic.</span></span> <span data-ttu-id="4eb75-185">Dieser Nachrichtenspeicher wird von Simple MAPI als Standardnachrichtenspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="4eb75-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="4eb75-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="4eb75-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="4eb75-187">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-187">Dynamic.</span></span> <span data-ttu-id="4eb75-188">Dieser Nachrichtenspeicher sollte nicht in der Nachrichtenspeichertabelle veröffentlicht werden und wird nach der Abmeldung aus dem Profil gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4eb75-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="4eb75-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="4eb75-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="4eb75-190">Statische.</span><span class="sxs-lookup"><span data-stu-id="4eb75-190">Static.</span></span> <span data-ttu-id="4eb75-191">Dieser Transport erwartet, dass er der letzte Transport ist, der zum Senden einer Nachricht ausgewählt wurde, wenn mehrere Transportanbieter die Nachricht übertragen können.</span><span class="sxs-lookup"><span data-stu-id="4eb75-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4eb75-192">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4eb75-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4eb75-193">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4eb75-193">Header files</span></span>

<span data-ttu-id="4eb75-194">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4eb75-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="4eb75-195">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4eb75-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="4eb75-196">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4eb75-196">Mapitags.h</span></span>
  
> <span data-ttu-id="4eb75-197">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4eb75-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4eb75-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eb75-198">See also</span></span>



[<span data-ttu-id="4eb75-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="4eb75-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="4eb75-200">Kanonische Pidtagidentityentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4eb75-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="4eb75-201">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4eb75-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4eb75-202">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4eb75-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4eb75-203">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4eb75-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4eb75-204">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4eb75-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidTagResourceFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 875b37183134a6c5beca76ab7910cf601d1b6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567503"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="d3792-103">PidTagResourceFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3792-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d3792-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3792-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3792-105">Enthält eine Bitmaske aus Flags für die Message-Dienste und -Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d3792-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3792-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d3792-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3792-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d3792-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d3792-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d3792-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3792-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="d3792-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="d3792-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d3792-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3792-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d3792-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d3792-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d3792-112">Area:</span></span>  <br/> |<span data-ttu-id="d3792-113">Allgemeine MAPI</span><span class="sxs-lookup"><span data-stu-id="d3792-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3792-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d3792-114">Remarks</span></span>

<span data-ttu-id="d3792-115">Diese Eigenschaft beschreibt die Merkmale eines Diensts Nachricht, einem Dienstanbieter oder Status-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d3792-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="d3792-116">Die Kennzeichen, die für diese Eigenschaft festgelegt sind, hängt von dessen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="d3792-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="d3792-117">Beispielsweise sind einige Kennzeichen gilt nur für Objekte der Status und anderen Flags nur für Spalten in der Tabelle der Dienste.</span><span class="sxs-lookup"><span data-stu-id="d3792-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="d3792-118">Die Flags sind drei Klassen: statische, änderbare und dynamische.</span><span class="sxs-lookup"><span data-stu-id="d3792-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="d3792-119">Statische Flags werden anhand von Daten in MAPISVC MAPI festgelegt. INF-Datei und nicht mehr verändert.</span><span class="sxs-lookup"><span data-stu-id="d3792-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="d3792-120">Änderbare Flags werden von MAPI aus MAPISVC festgelegt. INF-Datei kann jedoch später geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="d3792-121">Dynamische Flags können festgelegt und zurücksetzen, indem Sie MAPI-Methoden.</span><span class="sxs-lookup"><span data-stu-id="d3792-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="d3792-122">Für einen Nachrichtendienst kann in dieser Eigenschaft eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d3792-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="d3792-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="d3792-124">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d3792-124">Reserved.</span></span> <span data-ttu-id="d3792-125">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3792-125">Do not use.</span></span>
    
<span data-ttu-id="d3792-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="d3792-127">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="d3792-127">Dynamic.</span></span> <span data-ttu-id="d3792-128">Der Nachrichtendienst enthält des Standard-Informationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="d3792-128">The message service contains the default store.</span></span> <span data-ttu-id="d3792-129">Eine Benutzeroberfläche zur sollen Bestätigung durch den Benutzer zur Bestätigung vor dem Löschen oder verschieben diesen Dienst das Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="d3792-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d3792-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d3792-131">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-131">Static.</span></span> <span data-ttu-id="d3792-132">Die Ebene Service-Flag, die festgelegt werden soll, um anzugeben, dass keines der Anbieter in den Dienst zum Angeben eines Identitätswerts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3792-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="d3792-133">Entweder dieses Flag oder SERVICE_PRIMARY_IDENTITY sollte Set, jedoch nicht beide.</span><span class="sxs-lookup"><span data-stu-id="d3792-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="d3792-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d3792-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d3792-135">Geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-135">Modifiable.</span></span> <span data-ttu-id="d3792-136">Der entsprechende Nachrichtendienst enthält den Anbieter für die primäre Identität für diese Sitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3792-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="d3792-137">Verwenden Sie [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) , um dieses Flag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3792-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="d3792-138">Entweder dieses Flag oder SERVICE_NO_PRIMARY_IDENTITY sollte Set, jedoch nicht beide.</span><span class="sxs-lookup"><span data-stu-id="d3792-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="d3792-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="d3792-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="d3792-140">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-140">Static.</span></span> <span data-ttu-id="d3792-141">Jeder Versuch, erstellen oder kopieren Sie diesen Nachrichtendienst in einem Profil, auf dem der Dienst bereits vorhanden ist, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="d3792-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="d3792-142">Zum Erstellen einer einzelnen Kopie Messagingdiensts die **PR_RESOURCE_FLAGS** -Eigenschaft auf den Dienst im Abschnitt MAPISVC hinzufügen. INF-Datei, und legen Sie dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="d3792-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="d3792-143">Einem Dienstanbieter kann in **PR_RESOURCE_FLAGS**eines oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d3792-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="d3792-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="d3792-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="d3792-145">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-145">Static.</span></span> <span data-ttu-id="d3792-146">Verarbeitung eingehender Nachrichten muss der Warteschlange Hook.</span><span class="sxs-lookup"><span data-stu-id="d3792-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="d3792-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="d3792-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="d3792-148">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-148">Static.</span></span> <span data-ttu-id="d3792-149">Der Warteschlange Hook muss ausgehende Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3792-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="d3792-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="d3792-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="d3792-151">Geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-151">Modifiable.</span></span> <span data-ttu-id="d3792-152">Diese Identität werden soll für ausgehende Nachrichten angewendet, wenn das Profil mehrere Instanzen dieser Transportdienst enthält.</span><span class="sxs-lookup"><span data-stu-id="d3792-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="d3792-153">Dies kann vorkommen, wenn mehrere Instanzen eines einzigen Anbieters im Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="d3792-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="d3792-155">Geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-155">Modifiable.</span></span> <span data-ttu-id="d3792-156">Dieses Nachrichtenspeichers ist der Standard-Informationsspeichers für das Profil.</span><span class="sxs-lookup"><span data-stu-id="d3792-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="d3792-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="d3792-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="d3792-158">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="d3792-158">Dynamic.</span></span> <span data-ttu-id="d3792-159">Die standardmäßigen Ordner dieses Nachrichtenspeichers, einschließlich den Stammordner zwischen Personen Nachricht (IPM) wurden nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="d3792-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="d3792-160">MAPI festgelegt und löscht dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="d3792-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="d3792-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="d3792-162">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-162">Static.</span></span> <span data-ttu-id="d3792-163">Dieses Nachrichtenspeichers ist nicht in der Lage sind somit Nachricht Standardspeicher für das Profil.</span><span class="sxs-lookup"><span data-stu-id="d3792-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="d3792-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d3792-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d3792-165">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-165">Static.</span></span> <span data-ttu-id="d3792-166">Diesem Anbieter ist nicht mit eine Identität in der Statuszeile sind.</span><span class="sxs-lookup"><span data-stu-id="d3792-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="d3792-167">Entweder dieses Flag oder STATUS_PRIMARY_IDENTITY muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="d3792-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="d3792-169">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-169">Static.</span></span> <span data-ttu-id="d3792-170">Dieser Transportdienst ist eng mit einem Nachrichtenspeicher verknüpft und stellt die **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md))-Eigenschaft in der Statuszeile bereit.</span><span class="sxs-lookup"><span data-stu-id="d3792-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="d3792-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d3792-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d3792-172">Geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-172">Modifiable.</span></span> <span data-ttu-id="d3792-173">Dieser Anbieter stellt die primäre Identität für die Sitzung bereit; die Eintrags-ID für die Einrichtung der Identity-Objekt wird von [IMAPISession::QueryIdentity](imapisession-queryidentity.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3792-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="d3792-174">Entweder dieses Flag oder **STATUS_NO_PRIMARY_IDENTITY** muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="d3792-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="d3792-176">Geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-176">Modifiable.</span></span> <span data-ttu-id="d3792-177">Dieses Nachrichtenspeichers ist verwendet werden, wenn eine Clientanwendung anmeldet.</span><span class="sxs-lookup"><span data-stu-id="d3792-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="d3792-178">Nach dem Öffnen, sollte diesen Informationsspeicher als Standardspeicher für das Profil festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="d3792-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="d3792-180">Geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-180">Modifiable.</span></span> <span data-ttu-id="d3792-181">Dieses Nachrichtenspeichers ist geeignet, wenn der primäre Speicher nicht verfügbar ist, wenn eine Clientanwendung anmeldet.</span><span class="sxs-lookup"><span data-stu-id="d3792-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="d3792-182">Nach dem Öffnen, sollte diesen Informationsspeicher als Standardspeicher für das Profil festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="d3792-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="d3792-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="d3792-184">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="d3792-184">Dynamic.</span></span> <span data-ttu-id="d3792-185">Dieses Nachrichtenspeichers wird als den Standard-Nachrichtenspeicher von Simple MAPI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="d3792-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="d3792-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="d3792-187">Dynamische.</span><span class="sxs-lookup"><span data-stu-id="d3792-187">Dynamic.</span></span> <span data-ttu-id="d3792-188">Dieses Nachrichtenspeichers sollte nicht in der Nachricht Store Tabelle veröffentlicht werden und wird aus dem Profil nach der Abmeldung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="d3792-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="d3792-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="d3792-190">Statische.</span><span class="sxs-lookup"><span data-stu-id="d3792-190">Static.</span></span> <span data-ttu-id="d3792-191">Dieser Transport erwartet in der letzten Übertragungsprotokoll zum Senden einer Nachricht, wenn mehrere Transportanbieter zum Übertragen der Nachricht können ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="d3792-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d3792-192">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3792-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d3792-193">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d3792-193">Header files</span></span>

<span data-ttu-id="d3792-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3792-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3792-195">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d3792-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3792-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3792-196">Mapitags.h</span></span>
  
> <span data-ttu-id="d3792-197">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d3792-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3792-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3792-198">See also</span></span>



[<span data-ttu-id="d3792-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="d3792-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="d3792-200">PidTagIdentityEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3792-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="d3792-201">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3792-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3792-202">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3792-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3792-203">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d3792-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3792-204">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d3792-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


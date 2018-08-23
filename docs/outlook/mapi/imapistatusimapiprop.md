---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 23663cea49c50f3f584d6b06e331545320e8283b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565382"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="d17b1-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d17b1-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="d17b1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d17b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d17b1-105">Enthält Statusinformationen zu MAPI-Subsystems, integrierte des Adressbuchs und die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d17b1-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="d17b1-106">Ein Dienstanbieter implementiert **IMAPIStatus** , um Informationen über einen eigenen Status bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d17b1-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d17b1-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d17b1-107">Header file:</span></span>  <br/> |<span data-ttu-id="d17b1-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d17b1-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d17b1-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="d17b1-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="d17b1-110">Status-Objekte</span><span class="sxs-lookup"><span data-stu-id="d17b1-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="d17b1-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d17b1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d17b1-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="d17b1-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="d17b1-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d17b1-113">Called by:</span></span>  <br/> |<span data-ttu-id="d17b1-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="d17b1-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="d17b1-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="d17b1-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d17b1-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="d17b1-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="d17b1-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="d17b1-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="d17b1-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="d17b1-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="d17b1-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="d17b1-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="d17b1-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="d17b1-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d17b1-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d17b1-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d17b1-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="d17b1-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="d17b1-123">Bestätigen Sie die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d17b1-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="d17b1-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="d17b1-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="d17b1-125">Zeigt ein Eigenschaftenfenster, mit dem den Benutzer einem Dienstanbieter Konfiguration ändern kann.</span><span class="sxs-lookup"><span data-stu-id="d17b1-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="d17b1-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="d17b1-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="d17b1-127">Ändert das Kennwort des Dienstanbieters ohne eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d17b1-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="d17b1-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d17b1-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="d17b1-129">Erzwingt, dass alle Nachrichten gesendet oder empfangen, um sofort hoch- oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="d17b1-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="d17b1-130">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="d17b1-130">**Required properties**</span></span>|<span data-ttu-id="d17b1-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="d17b1-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d17b1-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-133">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="d17b1-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="d17b1-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-135">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="d17b1-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="d17b1-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-137">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d17b1-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="d17b1-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-139">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d17b1-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="d17b1-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-141">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d17b1-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="d17b1-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-143">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d17b1-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="d17b1-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d17b1-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d17b1-145">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d17b1-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d17b1-146">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d17b1-146">Remarks</span></span>

<span data-ttu-id="d17b1-147">Der Status, die von MAPI implementierte Objekte unterstützen die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="d17b1-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="d17b1-148">**Statusobjekt**</span><span class="sxs-lookup"><span data-stu-id="d17b1-148">**Status object**</span></span>|<span data-ttu-id="d17b1-149">**Unterstützte Methoden**</span><span class="sxs-lookup"><span data-stu-id="d17b1-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d17b1-150">MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="d17b1-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="d17b1-151">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="d17b1-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="d17b1-152">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="d17b1-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="d17b1-153">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="d17b1-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="d17b1-154">MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d17b1-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="d17b1-155">**ValidateState** und **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="d17b1-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="d17b1-156">Der Status, die von MAPI implementierte Objekte sind erforderlich, um eine schreibgeschützte Version der Methoden der Schnittstelle [IMAPIProp](imapipropiunknown.md) haben und die **ValidateState** -Methode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d17b1-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="d17b1-157">Transportanbieter sollten auch **FlushQueues**unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d17b1-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="d17b1-158">Alle Anbieter sollte **SettingsDialog**unterstützen. Unterstützung für **ChangePassword** optional ist.</span><span class="sxs-lookup"><span data-stu-id="d17b1-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="d17b1-159">Clients verwenden Status Objekte zum Ausführen der Konfiguration und zum Status der Sitzung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="d17b1-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="d17b1-160">Sie haben ein Statusobjekt durch Aufrufen der **OpenStatusEntry** -Methode eines Service Provider Anmeldung-Objekts oder die [IMAPISession::GetStatusTable](imapisession-getstatustable.md) -Methode zum Abrufen des Status-Objekts zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d17b1-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d17b1-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d17b1-161">See also</span></span>



[<span data-ttu-id="d17b1-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d17b1-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


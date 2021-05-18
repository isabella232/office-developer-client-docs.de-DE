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
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408299"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="4cb7e-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4cb7e-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="4cb7e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cb7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cb7e-105">Stellt Statusinformationen zum MAPI-Subsystem, zum integrierten Adressbuch und zum MAPI-Spooler zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="4cb7e-106">Ein Dienstanbieter implementiert **IMAPIStatus,** um Informationen zu seinem eigenen Status zu liefern.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cb7e-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="4cb7e-107">Header file:</span></span>  <br/> |<span data-ttu-id="4cb7e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cb7e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4cb7e-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="4cb7e-110">Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="4cb7e-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="4cb7e-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="4cb7e-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="4cb7e-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="4cb7e-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-113">Called by:</span></span>  <br/> |<span data-ttu-id="4cb7e-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="4cb7e-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="4cb7e-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4cb7e-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="4cb7e-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="4cb7e-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="4cb7e-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="4cb7e-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="4cb7e-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="4cb7e-120">Nichttransaktioniert</span><span class="sxs-lookup"><span data-stu-id="4cb7e-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4cb7e-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="4cb7e-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4cb7e-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="4cb7e-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="4cb7e-123">Bestätigt die externen Statusinformationen, die für die MAPI-Ressource oder den Dienstanbieter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="4cb7e-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="4cb7e-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="4cb7e-125">Zeigt ein Eigenschaftenblatt an, mit dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="4cb7e-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="4cb7e-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="4cb7e-127">Ändert das Kennwort eines Dienstanbieters, ohne dass eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="4cb7e-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="4cb7e-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="4cb7e-129">Erzwingt, dass alle Nachrichten, die auf das Senden oder Empfangen warten, sofort hochgeladen oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="4cb7e-130">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-130">**Required properties**</span></span>|<span data-ttu-id="4cb7e-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cb7e-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4cb7e-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="4cb7e-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4cb7e-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="4cb7e-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4cb7e-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="4cb7e-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4cb7e-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="4cb7e-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4cb7e-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="4cb7e-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4cb7e-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="4cb7e-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cb7e-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4cb7e-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4cb7e-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cb7e-146">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4cb7e-146">Remarks</span></span>

<span data-ttu-id="4cb7e-147">Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="4cb7e-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="4cb7e-148">**Status-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-148">**Status object**</span></span>|<span data-ttu-id="4cb7e-149">**Unterstützte Methoden**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cb7e-150">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="4cb7e-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="4cb7e-151">**Nur ValidateState**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="4cb7e-152">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="4cb7e-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="4cb7e-153">**Nur ValidateState**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="4cb7e-154">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="4cb7e-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="4cb7e-155">**ValidateState** und **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="4cb7e-156">Die von MAPI implementierten Statusobjekte müssen über eine schreibgeschützte Version der Methoden der [IMAPIProp-Schnittstelle](imapipropiunknown.md) verfügen und die **ValidateState-Methode** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="4cb7e-157">Transportanbieter sollten auch **FlushQueues unterstützen.**</span><span class="sxs-lookup"><span data-stu-id="4cb7e-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="4cb7e-158">Alle Anbieter sollten **SettingsDialog unterstützen;** Die Unterstützung **für ChangePassword** ist optional.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="4cb7e-159">Clients verwenden Statusobjekte, um die Konfiguration durchzuführen und mehr über den Status der Sitzung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="4cb7e-160">Sie greifen auf ein Statusobjekt zu, indem sie die **OpenStatusEntry-Methode** eines Anmeldeobjekts eines Dienstanbieters oder die [IMAPISession::GetStatusTable-Methode](imapisession-getstatustable.md) aufrufen, um das Statusobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4cb7e-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cb7e-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cb7e-161">See also</span></span>



[<span data-ttu-id="4cb7e-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="4cb7e-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


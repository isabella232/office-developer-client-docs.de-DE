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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331528"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="2d4cb-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2d4cb-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="2d4cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d4cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d4cb-105">Stellt Statusinformationen zum MAPI-Subsystem, dem integrierten Adressbuch und dem MAPI-Spooler bereit.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="2d4cb-106">Ein Dienstanbieter implementiert **IMAPIStatus** , um Informationen über seinen eigenen Status bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d4cb-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2d4cb-107">Header file:</span></span>  <br/> |<span data-ttu-id="2d4cb-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2d4cb-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2d4cb-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2d4cb-110">Statusobjekte</span><span class="sxs-lookup"><span data-stu-id="2d4cb-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="2d4cb-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2d4cb-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="2d4cb-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="2d4cb-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-113">Called by:</span></span>  <br/> |<span data-ttu-id="2d4cb-114">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="2d4cb-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="2d4cb-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2d4cb-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="2d4cb-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="2d4cb-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2d4cb-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="2d4cb-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="2d4cb-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="2d4cb-120">Nicht durchgeführten</span><span class="sxs-lookup"><span data-stu-id="2d4cb-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2d4cb-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2d4cb-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2d4cb-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="2d4cb-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="2d4cb-123">Bestätigt die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="2d4cb-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="2d4cb-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="2d4cb-125">Zeigt ein Eigenschaftenfenster an, in dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="2d4cb-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="2d4cb-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="2d4cb-127">Ändert das Kennwort eines Dienstanbieters, ohne eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="2d4cb-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="2d4cb-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="2d4cb-129">ErZwingt, dass alle Nachrichten, die darauf warten, gesendet oder empfangen werden, sofort hochgeladen oder heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="2d4cb-130">**Erforderliche Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-130">**Required properties**</span></span>|<span data-ttu-id="2d4cb-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d4cb-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2d4cb-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="2d4cb-134">**PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2d4cb-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="2d4cb-136">**PR_PROVIDER_DLL_NAME** ([Pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2d4cb-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="2d4cb-138">**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2d4cb-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="2d4cb-140">**PR_RESOURCE_METHODS** ([Pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2d4cb-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="2d4cb-142">**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2d4cb-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="2d4cb-144">**PR_STATUS_CODE** ([Pidtagstatuscode (](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d4cb-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2d4cb-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2d4cb-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d4cb-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d4cb-146">Remarks</span></span>

<span data-ttu-id="2d4cb-147">Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="2d4cb-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="2d4cb-148">**Status-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-148">**Status object**</span></span>|<span data-ttu-id="2d4cb-149">**Unterstützte Methoden**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d4cb-150">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="2d4cb-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="2d4cb-151">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="2d4cb-152">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="2d4cb-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="2d4cb-153">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="2d4cb-154">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="2d4cb-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="2d4cb-155">**ValidateState** und **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="2d4cb-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="2d4cb-156">Die von MAPI implementierten Statusobjekte sind erforderlich, um eine schreibgeschützte Version der Methoden der [IMAPIProp](imapipropiunknown.md) -Schnittstelle und die **ValidateState** -Methode zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="2d4cb-157">Transport Anbieter sollten auch **FlushQueues**unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="2d4cb-158">Alle Anbieter sollten **Settingsdialog**unterstützen; die Unterstützung für **ChangePassword** ist optional.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="2d4cb-159">Clients verwenden Statusobjekte, um die Konfiguration auszuführen und um den Status der Sitzung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="2d4cb-160">Sie greifen auf ein Status-Objekt zu, indem Sie die **OpenStatusEntry** -Methode eines Dienstanbieter-Anmelde Objekts oder die [IMAPISession::](imapisession-getstatustable.md) getstatusable-Methode aufrufen, um das Status-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2d4cb-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d4cb-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d4cb-161">See also</span></span>



[<span data-ttu-id="2d4cb-162">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2d4cb-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


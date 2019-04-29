---
title: Kanonische Pidtagresourcemethods (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436335"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="2fb18-103">Kanonische Pidtagresourcemethods (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2fb18-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="2fb18-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fb18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fb18-105">Enthält eine Bitmaske von Flags, die die Methoden in der **IMAPIStatus** -Schnittstelle, die vom Status-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2fb18-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fb18-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2fb18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2fb18-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="2fb18-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="2fb18-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2fb18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2fb18-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="2fb18-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="2fb18-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2fb18-110">Data type:</span></span>  <br/> |<span data-ttu-id="2fb18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2fb18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2fb18-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2fb18-112">Area:</span></span>  <br/> |<span data-ttu-id="2fb18-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="2fb18-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fb18-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fb18-114">Remarks</span></span>

<span data-ttu-id="2fb18-115">Diese Eigenschaft gibt an, welche der Methoden in der Implementierung von **IMAPIStatus** eines Status Objekts unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2fb18-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="2fb18-116">Status-Objekte können MAPI_E_NO_SUPPORT von nicht unterstützten Methoden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2fb18-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="2fb18-117">Clients verwenden die **PR_RESOURCE_METHODS** -Eigenschaft eines Status Objekts, um das Aufrufen von nicht unterstützten Methoden zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2fb18-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="2fb18-118">Wenn das Flag für eine bestimmte Methode festgelegt ist, ist die Methode vorhanden und kann aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2fb18-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="2fb18-119">Wenn dieses Flag leer ist, sollte die Methode nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2fb18-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="2fb18-120">Die von MAPI implementierten Statusobjekte unterstützen die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="2fb18-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="2fb18-121">**Status-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2fb18-121">**Status object**</span></span>|<span data-ttu-id="2fb18-122">**Unterstützte Methoden**</span><span class="sxs-lookup"><span data-stu-id="2fb18-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2fb18-123">MAPI-Subsystem</span><span class="sxs-lookup"><span data-stu-id="2fb18-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="2fb18-124">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="2fb18-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="2fb18-125">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="2fb18-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="2fb18-126">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="2fb18-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="2fb18-127">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="2fb18-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="2fb18-128">**ValidateState** und **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="2fb18-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="2fb18-129">Eine oder mehrere der folgenden Flags können in **PR_RESOURCE_METHODS**festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="2fb18-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="2fb18-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="2fb18-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="2fb18-131">Gibt an, dass die [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) -Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2fb18-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="2fb18-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="2fb18-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="2fb18-133">Gibt an, dass die [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2fb18-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="2fb18-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2fb18-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="2fb18-135">Gibt an, dass die [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2fb18-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="2fb18-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="2fb18-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="2fb18-137">Gibt an, dass die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2fb18-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="2fb18-138">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2fb18-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2fb18-139">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2fb18-139">Header files</span></span>

<span data-ttu-id="2fb18-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2fb18-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="2fb18-141">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2fb18-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="2fb18-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2fb18-142">Mapitags.h</span></span>
  
> <span data-ttu-id="2fb18-143">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2fb18-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fb18-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fb18-144">See also</span></span>



[<span data-ttu-id="2fb18-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fb18-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2fb18-146">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fb18-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2fb18-147">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2fb18-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2fb18-148">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2fb18-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


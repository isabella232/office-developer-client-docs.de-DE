---
title: Kanonische PidTagResourceMethods-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794965"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="94713-103">Kanonische PidTagResourceMethods-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="94713-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="94713-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94713-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94713-105">Enthält eine Bitmaske der Flags, die die Methoden in der Schnittstelle **IMAPIStatus** angeben, die durch die Statusobjekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="94713-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94713-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="94713-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94713-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="94713-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="94713-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="94713-108">Identifier:</span></span>  <br/> |<span data-ttu-id="94713-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="94713-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="94713-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="94713-110">Data type:</span></span>  <br/> |<span data-ttu-id="94713-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="94713-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="94713-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="94713-112">Area:</span></span>  <br/> |<span data-ttu-id="94713-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="94713-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94713-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="94713-114">Remarks</span></span>

<span data-ttu-id="94713-115">Diese Eigenschaft gibt an, welche der Methoden in der Implementierung der **IMAPIStatus** ein Statusobjekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="94713-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="94713-116">Status-Objekte sind zulässig, nicht unterstützten Methoden MAPI_E_NO_SUPPORT zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94713-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="94713-117">Clients verwenden ein Statusobjekt **PR_RESOURCE_METHODS** -Eigenschaft, um das Aufrufen von nicht unterstützten Methoden zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="94713-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="94713-118">Wenn das Flag, das eine bestimmte Methode entspricht, festgelegt ist, wird die Methode vorhanden ist und aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="94713-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="94713-119">Wenn Flags deaktiviert ist, sollte die Methode nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="94713-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="94713-120">Die Status-Objekte, die von MAPI-Unterstützung die folgenden Methoden implementiert:</span><span class="sxs-lookup"><span data-stu-id="94713-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="94713-121">**Statusobjekt**</span><span class="sxs-lookup"><span data-stu-id="94713-121">**Status object**</span></span>|<span data-ttu-id="94713-122">**Unterstützte Methoden**</span><span class="sxs-lookup"><span data-stu-id="94713-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="94713-123">MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="94713-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="94713-124">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="94713-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="94713-125">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="94713-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="94713-126">Nur **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="94713-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="94713-127">MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="94713-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="94713-128">**ValidateState** und **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="94713-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="94713-129">In **PR_RESOURCE_METHODS**kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="94713-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="94713-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="94713-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="94713-131">Gibt an, dass die [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) -Methode unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="94713-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="94713-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="94713-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="94713-133">Gibt an, dass die Methode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="94713-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="94713-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="94713-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="94713-135">Gibt an, dass [die SettingsDialog](imapistatus-settingsdialog.md) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="94713-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="94713-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="94713-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="94713-137">Gibt an, dass die Methode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="94713-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="94713-138">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94713-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="94713-139">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="94713-139">Header files</span></span>

<span data-ttu-id="94713-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94713-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="94713-141">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="94713-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="94713-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="94713-142">Mapitags.h</span></span>
  
> <span data-ttu-id="94713-143">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="94713-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94713-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94713-144">See also</span></span>



[<span data-ttu-id="94713-145">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94713-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94713-146">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94713-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94713-147">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="94713-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94713-148">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="94713-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


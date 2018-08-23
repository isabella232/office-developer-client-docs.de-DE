---
title: Informationen zu benannten von Outlook verwendete Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566229"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="3ff1c-103">Informationen zu benannten von Outlook verwendete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ff1c-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="3ff1c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ff1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ff1c-p101">MAPI bietet die M�glichkeit zum Zuweisen von Namen auf bestimmte Eigenschaften f�r die Zuordnung Managementsystems zu eindeutigen IDs und zum Beschleunigen des best�ndigen dieser Name-zu-Bezeichner zuordnen in allen Sitzungen. Benannte Eigenschaften werden durch einen Namen und einen global eindeutigen Bezeichner (GUID) f�r einen Eigenschaftensatz identifiziert. Der Name kann eine Zahl oder eine Zeichenfolge sein. F�r Microsoft Outlook 2013 oder Microsoft Outlook 2010 ist der Eigenschaftensatz oft einen Namespace definiert durch Outlook 2013 oder Outlook 2010 wie **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="3ff1c-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="3ff1c-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span><span class="sxs-lookup"><span data-stu-id="3ff1c-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="3ff1c-p103">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span><span class="sxs-lookup"><span data-stu-id="3ff1c-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="3ff1c-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Kanonische PidLidEmail1EmailAddress-Eigenschaft](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span><span class="sxs-lookup"><span data-stu-id="3ff1c-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="3ff1c-120">In dieser Referenz werden eine Reihe von benannten Eigenschaften die unten aufgef�hrten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ff1c-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="3ff1c-121">Benannte Eigenschaften im Namespace **PSETID_Address** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-122">Kanonische PidLidEmail1AddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-123">Kanonische PidLidEmail1EmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-124">Kanonische PidLidEmail1OriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-125">Kanonische PidLidEmail2AddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-126">Kanonische PidLidEmail2DisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-127">Kanonische PidLidEmail2EmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-128">Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-129">Kanonische PidLidEmail2OriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-130">Kanonische PidLidEmail3AddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-131">Kanonische PidLidEmail3DisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-132">Kanonische PidLidEmail3EmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-133">Kanonische PidLidEmail3OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-134">Kanonische PidLidEmail3OriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-135">Kanonische PidLidEmail1DisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-136">Kanonische PidLidEmail1OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-137">Kanonische PidLidFileUnder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-138">Kanonische PidLidInstantMessagingAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-139">Kanonische PidLidWorkAddressCity-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-140">Kanonische PidLidWorkAddressCountry-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-141">Kanonische PidLidWorkAddressPostalCode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-142">Kanonische PidLidWorkAddressPostOfficeBox-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-143">Kanonische PidLidWorkAddressState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-144">Kanonische PidLidWorkAddressStreet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-145">Kanonische PidLidYomiCompanyName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-146">Kanonische PidLidYomiFirstName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-147">Kanonische PidLidYomiLastName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="3ff1c-148">Benannte Eigenschaften im Namespace **PSETID_Appointment** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-149">Kanonische PidLidAllAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-150">Kanonische PidLidAppointmentCounterProposal-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-151">Kanonische PidLidAppointmentDuration-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-152">Kanonische PidLidAppointmentEndWhole-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-153">Kanonische PidLidAppointmentStartWhole-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-154">Kanonische PidLidBusyStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-155">Kanonische PidLidCcAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-156">Kanonische PidLidLocation-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-157">Kanonische PidLidRecurring-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-158">Kanonische PidLidToAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="3ff1c-159">Benannte Eigenschaften im Namespace **PSETID_Common** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-160">Kanonische PidLidCommonEnd-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-161">Kanonische PidLidCommonStart-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-162">Kanonische PidLidCompanies-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-163">Kanonische PidLidContacts-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-164">Kanonische PidLidCustomFlag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-165">Kanonische PidLidFormPropStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-166">Kanonische PidLidFormStorage-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-167">Kanonische PidLidHeaderItem-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-168">Kanonische PidLidPageDirStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-169">Kanonische PidLidPropertyDefinitionStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-170">Kanonische PidLidReminderSet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-171">Kanonische PidLidReminderTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-172">Kanonische PidLidFlagRequest-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-173">Kanonische PidLidScriptStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-174">Kanonische PidLidSmartNoAttach-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-175">Kanonische PidLidToDoTitle-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-176">Kanonische PidLidUseTnef-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="3ff1c-177">Benannte Eigenschaften im Namespace **PSETID_Meeting** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-178">Kanonische PidLidMeetingType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="3ff1c-179">Benannte Eigenschaften im Namespace **PSETID_Task** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-180">Kanonische PidLidTaskActualEffort-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-181">Kanonische PidLidTaskDueDate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-182">Kanonische PidLidTaskEstimatedEffort-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-183">Kanonische PidLidTaskFRecurring-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-184">Kanonische PidLidTaskStartDate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-185">Kanonische PidLidTaskStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="3ff1c-186">Benannte Eigenschaften im Namespace **PS_INTERNET_HEADERS** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-187">Kanonische PidTagInternetReturnPath-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="3ff1c-188">Benannte Eigenschaften im Namespace **PSETID_Log** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-189">Kanonische PidLidLogDuration-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-190">Kanonische PidLidLogEnd-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-191">Kanonische PidLidLogStart-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-192">Kanonische PidLidLogType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="3ff1c-193">Benannte Eigenschaften im Namespace **PS_PUBLIC_STRINGS** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ff1c-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="3ff1c-194">Kanonische PidNameKeywords-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="3ff1c-195">Kanonische PidNameExchangeJunkEmailMoveStamp-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff1c-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="3ff1c-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ff1c-196">See also</span></span>



[<span data-ttu-id="3ff1c-197">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3ff1c-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3ff1c-198">Ermitteln, ob Outlook nur die Kopfzeile einer Nachricht heruntergeladen hat</span><span class="sxs-lookup"><span data-stu-id="3ff1c-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="3ff1c-199">Abrufen der E-Mail-Adresse eines Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="3ff1c-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="3ff1c-200">Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden</span><span class="sxs-lookup"><span data-stu-id="3ff1c-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)


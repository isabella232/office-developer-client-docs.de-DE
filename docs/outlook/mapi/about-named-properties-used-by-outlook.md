---
title: Informationen zu benannten Eigenschaften in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566229"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="d43aa-103">Informationen zu benannten Eigenschaften in Outlook</span><span class="sxs-lookup"><span data-stu-id="d43aa-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="d43aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d43aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d43aa-p101">MAPI bietet die Möglichkeit, Namen bestimmten Eigenschaften zuzuweisen, diese Namen eindeutigen IDs zuzuordnen und diese Namen-zu-ID-Zuordnung über Sitzungen hinweg Sitzungen dauerhaft zu machen. Benannte Eigenschaften werden durch einen Namen und einen global eindeutigen Bezeichner (GUID) für einen Eigenschaftensatz identifiziert. Der Name kann eine Zahl oder eine Zeichenfolge sein. Für Microsoft Outlook 2013 oder Microsoft Outlook 2010 ist der Eigenschaftensatz häufig ein Namespace, der von Outlook 2013 oder Outlook 2010 definiert wird, z. B. **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="d43aa-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="d43aa-p102">Benannte Eigenschaften werden mithilfe der [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)-Funktion und der [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)-Funktion bearbeitet. Der Name und die GUID des Eigenschaftensatzes werden an die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)-Funktion übergeben, um eine Eigenschaften-ID abzurufen, die für die aktuelle MAPI-Sitzung gültig ist. Da die Eigenschaften-ID von Computer zu Computer variieren kann, besteht die einzige konsistente Möglichkeit zum Zugreifen auf eine benannte Eigenschaft darin, dass sie deren Namen und GUID des Eigenschaftensatzes kennen. Der Bereich von IDs liegt immer zwischen 0x8000 and 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="d43aa-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="d43aa-p103">Jedes Objekt, das die [IMAPIProp : IUnknown](imapipropiunknown.md)-Schnittstelle implementiert, kann benannte Eigenschaften unterstützen. Insbesondere ein MAPI-Dienstanbieter oder ein MAPI-Client muss [IMAPIProp::GetProps](imapiprop-getprops.md) implementieren, um Werte von benannten Eigenschaften abzurufen. Das Festlegen von benannten Eigenschaften, die von Outlook 2013 oder Outlook 2010 verwendet werden, wird aufgrund des Risikos einer Beschädigung von Daten nicht unterstützt, die gemeinsam mit anderen MAPI-Anbietern oder -Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d43aa-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="d43aa-p104">Outlook 2013 und Outlook 2010 verwenden benannte Eigenschaften von MAPI, um viele ihrer Features zu implementieren, z. B. Anlagensicherheit und Gegenvorschläge zu Besprechungen. Auf diesen zugrunde liegenden Daten machen Outlook 2013 und Outlook 2010 einige dieser Eigenschaften als Elementeigenschaften in ihren Outlook 2013- und Outlook 2010-Objektmodellen verfügbar. Die **Email1Address**-Eigenschaft des **ContactItem**-Objekts im Objektmodell entspricht beispielsweise der benannten kanonischen Eigenschaft [PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) im **PSETID_Address**-Namespace. Im Allgemeinen werden aber aufgrund von Bedenken bezüglich Kompatibilität und Datenintegrität viele der MAPI-Eigenschaften, die von Outlook 2013 und Outlook 2010 verwendet werden, nicht im Objektmodell verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="d43aa-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="d43aa-120">In dieser Referenz wird eine Reihe von benannten Eigenschaften beschrieben, die nachfolgend aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d43aa-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="d43aa-121">Benannte Eigenschaften im Namespace **PSETID_Address** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-122">Kanonische PidLidEmail1AddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="d43aa-123">Kanonische PidLidEmail1EmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="d43aa-124">Kanonische PidLidEmail1OriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="d43aa-125">Kanonische PidLidEmail2AddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="d43aa-126">Kanonische PidLidEmail2DisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-127">Kanonische PidLidEmail2EmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="d43aa-128">Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-129">Kanonische PidLidEmail2OriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="d43aa-130">Kanonische PidLidEmail3AddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="d43aa-131">Kanonische PidLidEmail3DisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-132">Kanonische PidLidEmail3EmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="d43aa-133">Kanonische PidLidEmail3OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-134">Kanonische PidLidEmail3OriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="d43aa-135">Kanonische PidLidEmail1DisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-136">Kanonische PidLidEmail1OriginalDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-137">Kanonische PidLidFileUnder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="d43aa-138">Kanonische PidLidInstantMessagingAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="d43aa-139">Kanonische PidLidWorkAddressCity-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="d43aa-140">Kanonische PidLidWorkAddressCountry-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="d43aa-141">Kanonische PidLidWorkAddressPostalCode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="d43aa-142">Kanonische PidLidWorkAddressPostOfficeBox-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="d43aa-143">Kanonische PidLidWorkAddressState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="d43aa-144">Kanonische PidLidWorkAddressStreet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="d43aa-145">Kanonische PidLidYomiCompanyName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-146">Kanonische PidLidYomiFirstName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="d43aa-147">Kanonische PidLidYomiLastName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="d43aa-148">Benannte Eigenschaften im Namespace **PSETID_Appointment** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-149">Kanonische PidLidAllAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="d43aa-150">Kanonische PidLidAppointmentCounterProposal-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="d43aa-151">Kanonische PidLidAppointmentDuration-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="d43aa-152">Kanonische PidLidAppointmentEndWhole-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="d43aa-153">Kanonische PidLidAppointmentStartWhole-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="d43aa-154">Kanonische PidLidBusyStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="d43aa-155">Kanonische PidLidCcAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="d43aa-156">Kanonische PidLidLocation-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="d43aa-157">Kanonische PidLidRecurring-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="d43aa-158">Kanonische PidLidToAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="d43aa-159">Benannte Eigenschaften im Namespace **PSETID_Common** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-160">Kanonische PidLidCommonEnd-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="d43aa-161">Kanonische PidLidCommonStart-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="d43aa-162">Kanonische PidLidCompanies-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="d43aa-163">Kanonische PidLidContacts-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="d43aa-164">Kanonische PidLidCustomFlag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="d43aa-165">Kanonische PidLidFormPropStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="d43aa-166">Kanonische PidLidFormStorage-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="d43aa-167">Kanonische PidLidHeaderItem-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="d43aa-168">Kanonische PidLidPageDirStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="d43aa-169">Kanonische PidLidPropertyDefinitionStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="d43aa-170">Kanonische PidLidReminderSet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="d43aa-171">Kanonische PidLidReminderTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="d43aa-172">Kanonische PidLidFlagRequest-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="d43aa-173">Kanonische PidLidScriptStream-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="d43aa-174">Kanonische PidLidSmartNoAttach-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="d43aa-175">Kanonische PidLidToDoTitle-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="d43aa-176">Kanonische PidLidUseTnef-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="d43aa-177">Benannte Eigenschaften im Namespace **PSETID_Meeting** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-178">Kanonische PidLidMeetingType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="d43aa-179">Benannte Eigenschaften im Namespace **PSETID_Task** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-180">Kanonische PidLidTaskActualEffort-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="d43aa-181">Kanonische PidLidTaskDueDate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="d43aa-182">Kanonische PidLidTaskEstimatedEffort-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="d43aa-183">Kanonische PidLidTaskFRecurring-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="d43aa-184">Kanonische PidLidTaskStartDate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="d43aa-185">Kanonische PidLidTaskStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="d43aa-186">Benannte Eigenschaften im Namespace **PS_INTERNET_HEADERS** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-187">Kanonische PidTagInternetReturnPath-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="d43aa-188">Benannte Eigenschaften im Namespace **PSETID_Log** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-189">Kanonische PidLidLogDuration-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="d43aa-190">Kanonische PidLidLogEnd-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="d43aa-191">Kanonische PidLidLogStart-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="d43aa-192">Kanonische PidLidLogType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="d43aa-193">Benannte Eigenschaften im Namespace **PS_PUBLIC_STRINGS** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d43aa-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="d43aa-194">Kanonische PidNameKeywords-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="d43aa-195">Kanonische PidNameExchangeJunkEmailMoveStamp-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d43aa-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="d43aa-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d43aa-196">See also</span></span>



[<span data-ttu-id="d43aa-197">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d43aa-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d43aa-198">Ermitteln, ob Outlook nur die Kopfzeile einer Nachricht heruntergeladen hat</span><span class="sxs-lookup"><span data-stu-id="d43aa-198">Determine if Outlook downloaded only the header of a message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="d43aa-199">Abrufen der E-Mail-Adresse eines Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="d43aa-199">Get the email address of a Contact item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="d43aa-200">Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden</span><span class="sxs-lookup"><span data-stu-id="d43aa-200">Remove custom form definition saved with a message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)


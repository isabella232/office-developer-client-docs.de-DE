---
title: Informationen zu benannten Eigenschaften in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 328ff423025689795669d661f529270886123a7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322239"
---
# <a name="about-named-properties-used-by-outlook"></a>Informationen zu benannten Eigenschaften in Outlook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet die Möglichkeit, Namen bestimmten Eigenschaften zuzuweisen, diese Namen eindeutigen IDs zuzuordnen und diese Namen-zu-ID-Zuordnung über Sitzungen hinweg Sitzungen dauerhaft zu machen. Benannte Eigenschaften werden durch einen Namen und einen global eindeutigen Bezeichner (GUID) für einen Eigenschaftensatz identifiziert. Der Name kann eine Zahl oder eine Zeichenfolge sein. Für Microsoft Outlook 2013 oder Microsoft Outlook 2010 ist der Eigenschaftensatz häufig ein Namespace, der von Outlook 2013 oder Outlook 2010 definiert wird, z. B. **PSETID_Appointment**. 
  
Benannte Eigenschaften werden mithilfe der [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)-Funktion und der [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)-Funktion bearbeitet. Der Name und die GUID des Eigenschaftensatzes werden an die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)-Funktion übergeben, um eine Eigenschaften-ID abzurufen, die für die aktuelle MAPI-Sitzung gültig ist. Da die Eigenschaften-ID von Computer zu Computer variieren kann, besteht die einzige konsistente Möglichkeit zum Zugreifen auf eine benannte Eigenschaft darin, dass sie deren Namen und GUID des Eigenschaftensatzes kennen. Der Bereich von IDs liegt immer zwischen 0x8000 and 0xFFFE. 
  
Jedes Objekt, das die [IMAPIProp : IUnknown](imapipropiunknown.md)-Schnittstelle implementiert, kann benannte Eigenschaften unterstützen. Insbesondere ein MAPI-Dienstanbieter oder ein MAPI-Client muss [IMAPIProp::GetProps](imapiprop-getprops.md) implementieren, um Werte von benannten Eigenschaften abzurufen. Das Festlegen von benannten Eigenschaften, die von Outlook 2013 oder Outlook 2010 verwendet werden, wird aufgrund des Risikos einer Beschädigung von Daten nicht unterstützt, die gemeinsam mit anderen MAPI-Anbietern oder -Clients verwendet werden. 
  
Outlook 2013 und Outlook 2010 verwenden benannte Eigenschaften von MAPI, um viele ihrer Features zu implementieren, z. B. Anlagensicherheit und Gegenvorschläge zu Besprechungen. Auf diesen zugrunde liegenden Daten machen Outlook 2013 und Outlook 2010 einige dieser Eigenschaften als Elementeigenschaften in ihren Outlook 2013- und Outlook 2010-Objektmodellen verfügbar. Die **Email1Address**-Eigenschaft des **ContactItem**-Objekts im Objektmodell entspricht beispielsweise der benannten kanonischen Eigenschaft [PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) im **PSETID_Address**-Namespace. Im Allgemeinen werden aber aufgrund von Bedenken bezüglich Kompatibilität und Datenintegrität viele der MAPI-Eigenschaften, die von Outlook 2013 und Outlook 2010 verwendet werden, nicht im Objektmodell verfügbar gemacht. 
  
In dieser Referenz wird eine Reihe von benannten Eigenschaften beschrieben, die nachfolgend aufgeführt sind.
  
Benannte Eigenschaften im Namespace **PSETID_Address** lauten wie folgt: 
  
- [Kanonische PidLidEmail1AddressType-Eigenschaft](pidlidemail1addresstype-canonical-property.md)
    
- [Kanonische PidLidEmail1EmailAddress-Eigenschaft](pidlidemail1emailaddress-canonical-property.md)
    
- [Kanonische PidLidEmail1OriginalEntryId-Eigenschaft](pidlidemail1originalentryid-canonical-property.md)
    
- [Kanonische PidLidEmail2AddressType-Eigenschaft](pidlidemail2addresstype-canonical-property.md)
    
- [Kanonische PidLidEmail2DisplayName-Eigenschaft](pidlidemail2displayname-canonical-property.md)
    
- [Kanonische PidLidEmail2EmailAddress-Eigenschaft](pidlidemail2emailaddress-canonical-property.md)
    
- [Kanonische PidLidEmail2OriginalDisplayName-Eigenschaft](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Kanonische PidLidEmail2OriginalEntryId-Eigenschaft](pidlidemail2originalentryid-canonical-property.md)
    
- [Kanonische PidLidEmail3AddressType-Eigenschaft](pidlidemail3addresstype-canonical-property.md)
    
- [Kanonische PidLidEmail3DisplayName-Eigenschaft](pidlidemail3displayname-canonical-property.md)
    
- [Kanonische PidLidEmail3EmailAddress-Eigenschaft](pidlidemail3emailaddress-canonical-property.md)
    
- [Kanonische PidLidEmail3OriginalDisplayName-Eigenschaft](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Kanonische PidLidEmail3OriginalEntryId-Eigenschaft](pidlidemail3originalentryid-canonical-property.md)
    
- [Kanonische PidLidEmail1DisplayName-Eigenschaft](pidlidemail1displayname-canonical-property.md)
    
- [Kanonische PidLidEmail1OriginalDisplayName-Eigenschaft](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Kanonische PidLidFileUnder-Eigenschaft](pidlidfileunder-canonical-property.md)
    
- [Kanonische PidLidInstantMessagingAddress-Eigenschaft](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Kanonische PidLidWorkAddressCity-Eigenschaft](pidlidworkaddresscity-canonical-property.md)
    
- [Kanonische PidLidWorkAddressCountry-Eigenschaft](pidlidworkaddresscountry-canonical-property.md)
    
- [Kanonische PidLidWorkAddressPostalCode-Eigenschaft](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Kanonische PidLidWorkAddressPostOfficeBox-Eigenschaft](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Kanonische PidLidWorkAddressState-Eigenschaft](pidlidworkaddressstate-canonical-property.md)
    
- [Kanonische PidLidWorkAddressStreet-Eigenschaft](pidlidworkaddressstreet-canonical-property.md)
    
- [Kanonische PidLidYomiCompanyName-Eigenschaft](pidlidyomicompanyname-canonical-property.md)
    
- [Kanonische PidLidYomiFirstName-Eigenschaft](pidlidyomifirstname-canonical-property.md)
    
- [Kanonische PidLidYomiLastName-Eigenschaft](pidlidyomilastname-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PSETID_Appointment** lauten wie folgt: 
  
- [Kanonische PidLidAllAttendeesString-Eigenschaft](pidlidallattendeesstring-canonical-property.md)
    
- [Kanonische PidLidAppointmentCounterProposal-Eigenschaft](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Kanonische PidLidAppointmentDuration-Eigenschaft](pidlidappointmentduration-canonical-property.md)
    
- [Kanonische PidLidAppointmentEndWhole-Eigenschaft](pidlidappointmentendwhole-canonical-property.md)
    
- [Kanonische PidLidAppointmentStartWhole-Eigenschaft](pidlidappointmentstartwhole-canonical-property.md)
    
- [Kanonische PidLidBusyStatus-Eigenschaft](pidlidbusystatus-canonical-property.md)
    
- [Kanonische PidLidCcAttendeesString-Eigenschaft](pidlidccattendeesstring-canonical-property.md)
    
- [Kanonische PidLidLocation-Eigenschaft](pidlidlocation-canonical-property.md)
    
- [Kanonische PidLidRecurring-Eigenschaft](pidlidrecurring-canonical-property.md)
    
- [Kanonische PidLidToAttendeesString-Eigenschaft](pidlidtoattendeesstring-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PSETID_Common** lauten wie folgt: 
  
- [Kanonische PidLidCommonEnd-Eigenschaft](pidlidcommonend-canonical-property.md)
    
- [Kanonische PidLidCommonStart-Eigenschaft](pidlidcommonstart-canonical-property.md)
    
- [Kanonische PidLidCompanies-Eigenschaft](pidlidcompanies-canonical-property.md)
    
- [Kanonische PidLidContacts-Eigenschaft](pidlidcontacts-canonical-property.md)
    
- [Kanonische PidLidCustomFlag-Eigenschaft](pidlidcustomflag-canonical-property.md)
    
- [Kanonische PidLidFormPropStream-Eigenschaft](pidlidformpropstream-canonical-property.md)
    
- [Kanonische PidLidFormStorage-Eigenschaft](pidlidformstorage-canonical-property.md)
    
- [Kanonische PidLidHeaderItem-Eigenschaft](pidlidheaderitem-canonical-property.md)
    
- [Kanonische PidLidPageDirStream-Eigenschaft](pidlidpagedirstream-canonical-property.md)
    
- [Kanonische PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Kanonische PidLidReminderSet-Eigenschaft](pidlidreminderset-canonical-property.md)
    
- [Kanonische PidLidReminderTime-Eigenschaft](pidlidremindertime-canonical-property.md)
    
- [Kanonische PidLidFlagRequest-Eigenschaft](pidlidflagrequest-canonical-property.md)
    
- [Kanonische PidLidScriptStream-Eigenschaft](pidlidscriptstream-canonical-property.md)
    
- [Kanonische PidLidSmartNoAttach-Eigenschaft](pidlidsmartnoattach-canonical-property.md)
    
- [Kanonische PidLidToDoTitle-Eigenschaft](pidlidtodotitle-canonical-property.md)
    
- [Kanonische PidLidUseTnef-Eigenschaft](pidlidusetnef-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PSETID_Meeting** lauten wie folgt: 
  
- [Kanonische PidLidMeetingType-Eigenschaft](pidlidmeetingtype-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PSETID_Task** lauten wie folgt: 
  
- [Kanonische PidLidTaskActualEffort-Eigenschaft](pidlidtaskactualeffort-canonical-property.md)
    
- [Kanonische PidLidTaskDueDate-Eigenschaft](pidlidtaskduedate-canonical-property.md)
    
- [Kanonische PidLidTaskEstimatedEffort-Eigenschaft](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Kanonische PidLidTaskFRecurring-Eigenschaft](pidlidtaskfrecurring-canonical-property.md)
    
- [Kanonische PidLidTaskStartDate-Eigenschaft](pidlidtaskstartdate-canonical-property.md)
    
- [Kanonische PidLidTaskStatus-Eigenschaft](pidlidtaskstatus-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PS_INTERNET_HEADERS** lauten wie folgt: 
  
- [Kanonische PidTagInternetReturnPath-Eigenschaft](pidtaginternetreturnpath-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PSETID_Log** lauten wie folgt: 
  
- [Kanonische PidLidLogDuration-Eigenschaft](pidlidlogduration-canonical-property.md)
    
- [Kanonische PidLidLogEnd-Eigenschaft](pidlidlogend-canonical-property.md)
    
- [Kanonische PidLidLogStart-Eigenschaft](pidlidlogstart-canonical-property.md)
    
- [Kanonische PidLidLogType-Eigenschaft](pidlidlogtype-canonical-property.md)
    
Benannte Eigenschaften im Namespace **PS_PUBLIC_STRINGS** lauten wie folgt: 
  
- [Kanonische PidNameKeywords-Eigenschaft](pidnamekeywords-canonical-property.md)
    
- [Kanonische PidNameExchangeJunkEmailMoveStamp-Eigenschaft](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Konstanten](mapi-constants.md)
  
[Ermitteln, ob Outlook nur die Kopfzeile einer Nachricht heruntergeladen hat](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Abrufen der E-Mail-Adresse eines Kontaktelements](how-to-get-the-email-address-of-a-contact-item.md)
  
[Entfernen benutzerdefinierter Formulardefinitionen, die mit einer Nachricht gespeichert wurden](how-to-remove-custom-form-definition-saved-with-a-message.md)


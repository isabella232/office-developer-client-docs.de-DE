---
title: Kanonische Pidlidpostaladdressid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPostalAddressId
api_type:
- COM
ms.assetid: 30fdfb20-1e12-442a-bfa0-8c18c15fa5c3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 83f3c0559a3317de3789f8c93d024f08ada3e735
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315995"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>Kanonische Pidlidpostaladdressid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, welche physikalische Adresse die e-Mail-Adresse des Kontakts ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidPostalAddressId  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long-ID (Deckel):  <br/> |0x00008022  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sofern vorhanden, muss diese Eigenschaft einen der Werte aufweisen, die in der folgenden Tabelle oder in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)angegeben sind. Wenn diese Einstellung nicht festgelegt ist, sollte die Anwendung davon ausgehen, dass der Wert "0x00000000" lautet.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Es wird keine Adresse als Postanschrift ausgewählt. **PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **PR_LOCALITY** ([pidtaglocality (](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([ Pidtagcountry (](pidtagcountry-canonical-property.md)), **dispidAddressCountryCode** ([pidlidaddresscountrycode (](pidlidaddresscountrycode-canonical-property.md)) und **PR_POSTAL_ADDRESS** ([pidtagpostaladdress (](pidtagpostaladdress-canonical-property.md)) dürfen nicht festgelegt werden.  <br/> |
|0x00000001  <br/> |Die Privatadresse ist die Postanschrift. Die Werte von **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([pidtagpostofficebox (](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode **-und **PR_POSTAL_ADDRESS** -Eigenschaften müssen den Werten der **PR_HOME_ADDRESS_STREET** ([pidtaghomeaddressstreet (](pidtaghomeaddressstreet-canonical-property.md)), **PR_HOME_ADDRESS_CITY** ([pidtaghomeaddresscity (](pidtaghomeaddresscity-canonical-property.md)), **PR_HOME_ ADDRESS_STATE_OR_PROVINCE** ([pidtaghomeaddressstateorprovince (](pidtaghomeaddressstateorprovince-canonical-property.md)), **PR_HOME_ADDRESS_POSTAL_CODE** ([pidtaghomeaddresspostalcode (](pidtaghomeaddresspostalcode-canonical-property.md)), **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([ Pidtaghomeaddresspostofficebox (](pidtaghomeaddresspostofficebox-canonical-property.md)), **PR_HOME_ADDRESS_COUNTRY** ([pidtaghomeaddresscountry (](pidtaghomeaddresscountry-canonical-property.md)), **dispidHomeAddressCountryCode** ([pidlidhomeaddresscountrycode (](pidlidhomeaddresscountrycode-canonical-property.md)) und **dispidHomeAddress** ( [Pidlidhomeaddress (](pidlidhomeaddress-canonical-property.md)) Eigenschaften.  <br/> |
|0x00000002  <br/> |Die Arbeitsadresse ist die Postanschrift. Die Werte von **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode**und **PR_POSTAL_ADDRESS **Eigenschaften müssen den Werten von **dispidWorkAddressStreet** ([pidlidworkaddressstreet (](pidlidworkaddressstreet-canonical-property.md)), **dispidWorkAddressCity** ([pidlidworkaddresscity (](pidlidworkaddresscity-canonical-property.md)), **dispidWorkAddressState** ([ Pidlidworkaddressstate (](pidlidworkaddressstate-canonical-property.md)), **dispidWorkAddressPostalCode** ([pidlidworkaddresspostalcode (](pidlidworkaddresspostalcode-canonical-property.md)), **dispidWorkAddressPostOfficeBox** ([pidlidworkaddresspostofficebox (](pidlidworkaddresspostofficebox-canonical-property.md)), **dispidWorkAddressCountry **([Pidlidworkaddresscountry (](pidlidworkaddresscountry-canonical-property.md)), **dispidWorkAddressCountryCode** ([pidlidworkaddresscountrycode (](pidlidworkaddresscountrycode-canonical-property.md)) und **dispidWorkAddress** ([pidlidworkaddress (](pidlidworkaddress-canonical-property.md)).  <br/> |
|0x00000003  <br/> |Die andere Adresse ist die Postanschrift. Die Werte der, **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, **dispidAddressCountryCode**und **PR_POSTAL_ADDRESS **Eigenschaften müssen den Werten von **PR_OTHER_ADDRESS_STREET** ([pidtagotheraddressstreet (](pidtagotheraddressstreet-canonical-property.md)), **PR_OTHER_ADDRESS_CITY** ([pidtagotheraddresscity (](pidtagotheraddresscity-canonical-property.md)), **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** ( [Pidtagotheraddressstateorprovince (](pidtagotheraddressstateorprovince-canonical-property.md)), **PR_OTHER_ADDRESS_POSTAL_CODE** ([pidtagotheraddresspostalcode (](pidtagotheraddresspostalcode-canonical-property.md)), **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([pidtagotheraddresspostofficebox (](pidtagotheraddresspostofficebox-canonical-property.md)), ** dispidOtherAddressCountryCode** ([pidlidotheraddresscountrycode (](pidlidotheraddresscountrycode-canonical-property.md)) und **dispidOtherAddress** ([pidlidotheraddress (](pidlidotheraddress-canonical-property.md)).  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


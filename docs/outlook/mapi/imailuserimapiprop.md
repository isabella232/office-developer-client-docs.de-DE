---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436594"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die vielen Eigenschaften, die Messagingbenutzern zugeordnet sind. Die **IMailUser-Schnittstelle** wird von Messagingbenutzerobjekten implementiert. **IMailUser erbt** von der [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) und verfügt über keine eigenen eindeutigen Methoden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Messagingbenutzerobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMailUser  <br/> |
|Zeigertyp:  <br/> |LPMAILUSER  <br/> |
|Transaktionsmodell:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle verfügt nicht über eindeutige Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Fünf der erforderlichen Eigenschaften werden als Basisadresseneigenschaften für Empfänger bekannt:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Diese Eigenschaften gelten als besonders, da viele andere Gruppen ähnlicher Eigenschaften auf dieser Basisgruppe aufgebaut sind. Die anderen Gruppen werden verwendet, um einen Empfänger in verschiedenen Rollen zu beschreiben, z. B. dem ursprünglichen Absender oder dem Stellvertretungssender einer Nachricht. Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI Address Types](mapi-address-types.md).
  
Messagingbenutzer können eine Auflistung ihrer Eigenschaften anzeigen, indem sie die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft unterstützen. **PR_DETAILS_TABLE** ist eine Anzeigetabelle, in der das Layout eines Detaildialogfelds oder einer Registerkarteneigenschaftsseite beschrieben wird, auf der Empfängereigenschaftsinformationen angezeigt werden. MAPI erstellt Detaildialogfelder, wenn ein Client die [IAddrBook::D etails-Methode](iaddrbook-details.md) aufruft. 
  
Messagingbenutzerobjekten können andere optionale Eigenschaften zugeordnet sein. MAPI definiert viele Eigenschaften, die zusätzliche Adressierungsinformationen zu einem Messagingbenutzer bereitstellen. Alle diese Eigenschaften sind Zeichenzeichenfolgen. Die folgende Liste zeigt die häufiger verwendeten Eigenschaften:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Eine vollständige Liste der Eigenschaften finden Sie unter [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)


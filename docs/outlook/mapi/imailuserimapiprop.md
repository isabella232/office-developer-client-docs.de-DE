---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1c5485860c6e8efcf7ba768f25c0c13384f0733b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576107"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die vielen Eigenschaften, die Messagingbenutzern zugeordnet sind. Die **IMailUser-Schnittstelle** wird von Messaging-Benutzerobjekten implementiert. **IMailUser** erbt von der [IMAPIProp: IUnknown-Schnittstelle](imapipropiunknown.md) und verfügt über keine eigenen eindeutigen Methoden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Messaging-Benutzerobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMailUser  <br/> |
|Zeigertyp:  <br/> |LPMAILUSER  <br/> |
|Transaktionsmodell:  <br/> |Transaktiven  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

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
   
## <a name="remarks"></a>HinwBemerkungeneise

Fünf der erforderlichen Eigenschaften werden als Basisadresseigenschaften für Empfänger bezeichnet:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Diese Eigenschaften gelten als besonders, da viele andere Gruppen ähnlicher Eigenschaften auf dieser Basisgruppe basieren. Die anderen Gruppen werden verwendet, um einen Empfänger in verschiedenen Rollen zu beschreiben, z. B. den ursprünglichen Absender einer Nachricht oder den Absender einer Stellvertretung. Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI-Adresstypen.](mapi-address-types.md)
  
Messagingbenutzer können eine Auflistung ihrer Eigenschaften anzeigen, indem sie die **eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) unterstützen. **PR_DETAILS_TABLE** ist eine Anzeigetabelle, die das Layout eines Detaildialogfelds oder einer Eigenschaftenseite mit Registerkarten beschreibt, auf der Empfängereigenschafteninformationen angezeigt werden. MAPI erstellt Detaildialogfelder, wenn ein Client die [IAddrBook::D etails-Methode aufruft.](iaddrbook-details.md) 
  
Messaging-Benutzerobjekte können mit anderen optionalen Eigenschaften verknüpft sein. MAPI definiert viele Eigenschaften, die zusätzliche Adressierungsinformationen zu einem Messagingbenutzer bereitstellen. Alle diese Eigenschaften sind Zeichenfolgen. In der folgenden Liste sind die häufiger verwendeten Eigenschaften aufgeführt:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagNumberIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Eine vollständige Liste der Eigenschaften finden Sie unter [Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen.](mapping-canonical-property-names-to-mapi-names.md)
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)


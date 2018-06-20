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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792070"
---
# <a name="imailuser--imapiprop"></a>IMailUser: IMAPIProp

  
  
**Betrifft**: Outlook 
  
Bietet Zugriff auf die viele Eigenschaften, die messaging-Benutzer zugeordnet sind. Die **IMailUser** -Schnittstelle wird von messaging Benutzerobjekte implementiert. **IMailUser** erbt von der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und verfügt über keine eindeutigen Methoden eigenen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Messaging User-Objekte  <br/> |
|Implementiert von:  <br/> |Von adressbuchanbietern implementierte  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMailUser  <br/> |
|Zeigertyp:  <br/> |LPMAILUSER  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle hat keinen eindeutigen Methoden.
  
|**Erforderliche Eigenschaften**|**Zugriff**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Lese-/Schreibzugriff  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Schreibgeschützt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Fünf erforderlichen Eigenschaften sind als die Eigenschaften Basisadresse für Empfänger bekannt:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Diese Eigenschaften gelten besondere, da viele andere Gruppen von ähnlichen Eigenschaften auf dieser Basis Gruppe basieren. Die anderen Gruppen werden verwendet, um einen Empfänger in verschiedenen Rollen wird beschrieben, wie eine Nachricht ursprünglichen's oder Absender delegieren. Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI-Adresstypen](mapi-address-types.md).
  
Messaging-Benutzer kann eine Auflistung von deren Eigenschaften anzeigen, indem Sie die Eigenschaft **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) unterstützt. **PR_DETAILS_TABLE** ist eine zeigt die Tabelle, die beschreibt das Layout einer im Dialogfeld Details oder eine der Eigenschaftenseiten, die Empfänger-Eigenschafteninformationen anzeigt. MAPI erstellt Details Dialogfelder, wenn ein Client die [IAddrBook::Details](iaddrbook-details.md) -Methode aufruft. 
  
Messaging User-Objekte kann weitere optionalen Eigenschaften zugeordnet haben. MAPI definiert viele Eigenschaften, die zusätzliche reagieren auf Informationen über ein messaging-Benutzer bereitzustellen. Alle diese Eigenschaften sind Zeichenfolgen. Die folgende Liste enthält mehrere Eigenschaften häufig verwendet:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Eine vollständige Liste der Eigenschaften finden Sie unter [Zuordnen von kanonischen Eigenschaftennamen MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)


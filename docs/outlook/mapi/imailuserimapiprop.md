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
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351399"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die vielen Eigenschaften, die Messaging Benutzern zugeordnet sind. Die **IMailUser** -Schnittstelle wird von Messaging-Benutzerobjekten implementiert. **IMailUser** erbt von der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und verfügt über keine eigenen eindeutigen Methoden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Messaging-Benutzerobjekte  <br/> |
|Implementiert von:  <br/> |Adressbuchanbieter  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMailUser  <br/> |
|Zeigertyp:  <br/> |LPMAILUSER  <br/> |
|Transaktionsmodell:  <br/> |Durchgeführt  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

Diese Schnittstelle hat keine eindeutigen Methoden.
  
|**Erforderliche Eigenschaften**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Lesen/Schreiben  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
|**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Fünf der erforderlichen Eigenschaften werden als Basis Adresseigenschaften für Empfänger bezeichnet:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Diese Eigenschaften gelten als besonders, da viele andere Gruppen ähnlicher Eigenschaften auf dieser Basisgruppe basieren. Die anderen Gruppen werden zur Beschreibung eines Empfängers in verschiedenen Rollen verwendet, beispielsweise als ursprünglicher oder Stellvertreter der Nachricht. Weitere Informationen zu diesen Eigenschaften und deren Verwendung finden Sie unter [MAPI address types](mapi-address-types.md).
  
Messaging Benutzer können eine Auflistung ihrer Eigenschaften anzeigen, indem Sie die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft unterstützen. **PR_DETAILS_TABLE** ist eine Anzeigetabelle, die das Layout eines Details-Dialogfelds oder einer Eigenschaftenseite mit Registerkarten beschreibt, auf dem Informationen zu Empfänger Eigenschaften angezeigt werden. MAPI erstellt Detail Dialogfelder, wenn ein Client die [IAddrBook::D ails](iaddrbook-details.md) -Methode aufruft. 
  
Für Messaging-Benutzerobjekte können andere optionale Eigenschaften zugeordnet werden. MAPI definiert viele Eigenschaften, die zusätzliche Adressinformationen zu einem Messagingbenutzer bereitstellen. Alle diese Eigenschaften sind Zeichenfolgen. Die folgende Liste zeigt die häufiger verwendeten Eigenschaften:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([Pidtaggovernmentidnumber (](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([Pidtaglocality (](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([Pidtagpostaladdress (](pidtagpostaladdress-canonical-property.md)) 
    
Eine vollständige Liste der Eigenschaften finden Sie unter [Zuordnen von kanonischEn Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)


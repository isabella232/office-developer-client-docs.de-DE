---
title: PidTagReceivedByAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359227"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a>PidTagReceivedByAddressType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den E-Mail-Adresstyp, z. B. SMTP, für den Messagingbenutzer, der die Nachricht tatsächlich empfängt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W  <br/> |
|Kennung:  <br/> |0x0075  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Umschlag  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der die Nachricht tatsächlich empfängt. Sie müssen vom eingehenden Transportanbieter festgelegt werden.
  
Die Adresstypzeichenfolge kann nur die Großbuchstaben A bis Z und die Zahlen null bis neun enthalten. Diese Eigenschaften qualifizieren die **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) -Eigenschaft, indem sie einen Adresstyp angeben, z. B. SMTP, wodurch angegeben wird, wie die Adresse erstellt werden soll.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


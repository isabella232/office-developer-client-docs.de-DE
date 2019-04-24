---
title: Kanonische Pidtagrecipientcertificate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356714"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Kanonische Pidtagrecipientcertificate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das ASN. 1-Zertifikat eines Nachrichtenempfängers für die Verwendung in einem Bericht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Kennung:  <br/> |0x0C13  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine Kopie der **PR_USER_CERTIFICATE** ([pidtagusercertificate (](pidtagusercertificate-canonical-property.md))-Eigenschaft des Empfängers für die Verwendung in einem Bericht. Es kann verwendet werden, um dem Absender zu beweisen, dass der Empfänger die Nachricht tatsächlich erhalten hat, die ein zugestellter Bericht nicht unbedingt anzeigt.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


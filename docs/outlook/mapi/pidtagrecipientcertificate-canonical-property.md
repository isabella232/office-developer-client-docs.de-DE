---
title: Kanonische PidTagRecipientCertificate-Eigenschaft
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
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794909"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Kanonische PidTagRecipientCertificate-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Nachrichtenempfänger ASN. 1-Zertifikat für die Verwendung in einem Bericht.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Bezeichner:  <br/> |0x0C13  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist eine Kopie des Empfängers **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md))-Eigenschaft für die Verwendung in einem Bericht. Hiermit können Sie an den Ersteller nachweisen, dass der Empfänger tatsächlich die Nachricht empfangen hat, die die ein Unzustellbarkeitsberichts nicht notwendigerweise aufweisen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


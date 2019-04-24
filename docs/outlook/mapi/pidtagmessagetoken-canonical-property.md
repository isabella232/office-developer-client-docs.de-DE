---
title: Kanonische Pidtagmessagetoken (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355804"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Kanonische Pidtagmessagetoken (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein ASN. 1-Sicherheitstoken für eine Nachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Kennung:  <br/> |0x0C03  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Eigenschaften für sichere Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft übermittelt geschützte sicherheitsbezogene Informationen vom Absender an den Empfänger. In Verbindung mit der **PR_MESSAGE_SECURITY_LABEL** ([pidtagmessagesecuritylabel (](pidtagmessagesecuritylabel-canonical-property.md))-Eigenschaft wird die Zuordnung der Bezeichnung zum Nachrichteninhalt garantiert. In Verbindung mit der **PR_CONTENT_INTEGRITY_CHECK** ([pidtagcontentintegritycheck (](pidtagcontentintegritycheck-canonical-property.md))-Eigenschaft wird überprüft, ob der Nachrichteninhalt unverändert ist.
  
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


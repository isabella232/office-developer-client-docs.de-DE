---
title: PidTagViewsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427311"
---
# <a name="pidtagviewsentryid-canonical-property"></a>PidTagViewsEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des benutzerdefinierten Ordners Ansichten.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Kennung:  <br/> |0x35E5  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Allgemeine Ansichtsordner enthält einen vordefinierten Satz von Standardansichtsbezeichnern, während der Ansichtsordner von einem Messagingbenutzer definierte Specifier enthält. Diese Ordner, die in der IpM-Hierarchie (Interpersonal Message) nicht sichtbar sind, können viele Ansichtsbezeichner enthalten, die jeweils als Nachricht gespeichert sind. Die Clientanwendung kann die beiden Sätze von Specifiern zusammenführen und beide verfügbar machen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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


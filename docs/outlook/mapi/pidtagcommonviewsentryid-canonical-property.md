---
title: PidTagCommonViewsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437343"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>PidTagCommonViewsEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID des vordefinierten Ordners für allgemeine Ansicht. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|Kennung:  <br/> |0x35E6  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Outlook-Anwendung  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Allgemeine Ansichtsordner enthält einen vordefinierten Satz von Standardansichtsbezeichnern, während der Ansichtsordner von einem Messagingbenutzer definierte Specifier enthält. Diese Ordner, die in der IpM-Hierarchie (Interpersonal Message) nicht sichtbar sind, können viele Ansichtsbezeichner enthalten, die jeweils als Nachricht gespeichert sind. Eine Clientanwendung kann die beiden Sätze von Specifiern zusammenführen und beide verfügbar machen. 
  
Weitere Informationen zu Ansichten finden Sie unter [View Folders](mapi-view-folders.md).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagDefaultViewEntryId (kanonische Eigenschaft)](pidtagdefaultviewentryid-canonical-property.md)
  
[PidTagViewsEntryId (kanonische Eigenschaft)](pidtagviewsentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


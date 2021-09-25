---
title: PidTagViewsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ef38395a37be6b1bedab0eb6ef032ae6717f20c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591325"
---
# <a name="pidtagviewsentryid-canonical-property"></a>PidTagViewsEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner des benutzerdefinierten Ordners Ansichten.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_VIEWS_ENTRYID  <br/> |
|Kennung:  <br/> |0x35E5  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der allgemeine Ansichtsordner enthält einen vordefinierten Satz von Standardansichtsbezeichnern, während der Ansichtsordner von einem Messagingbenutzer definierte Bezeichner enthält. Diese Ordner, die in der Hierarchie zwischen zwischenmenschlicher Nachrichten (Interpersonal Message, IPM) nicht sichtbar sind, können viele Ansichtsbezeichner enthalten, die jeweils als Nachricht gespeichert sind. Die Clientanwendung kann die beiden Sätze von Spezifizierern zusammenführen und beide verfügbar machen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


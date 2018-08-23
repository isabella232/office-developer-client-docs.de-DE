---
title: PidTagDiscreteValues (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f1aa54c3364185d322137ef41f6aface31c5c556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587418"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>PidTagDiscreteValues (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält True, wenn ein Unzustellbarkeitsbericht zu nur einzelne Mitglieder einer Verteilerliste, anstatt die gesamte Liste angewendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Kennung:  <br/> |0x0E0E  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird in einen Unzustellbarkeitsbericht verwendet, wenn die Nachricht an einen oder mehrere Mitglieder von Verteilerlisten nicht übermittelt werden konnte. Dient zur erneuten Begrenzung nur die einzelnen Elemente und nicht die Verteilerliste als Ganzes versucht, ein. 
  
Die Empfänger ein Unzustellbarkeitsbericht-Tabelle enthält Einträge für alle Empfänger auf denen die Nachricht nicht übermittelt werden konnte und für die Verteilerlisten, falls vorhanden, zu denen sie gehören. Der Adressbuchhierarchie sollte diese Eigenschaft für jeden Listeneintrag Verteilung auf TRUE festgelegt, und es sollten die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) sowie die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_SEARCH_KEY** ([ Kopieren PidTagSearchKey](pidtagsearchkey-canonical-property.md)) aus der Verteilerliste **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) und **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) Eigenschaften für jedes Mitglied der gewünschten Verteilerliste. 
  
 **PR_DISCRETE_VALUES** sollte nicht für alle Empfänger Nondelivery Bericht-Eintrag keiner Verteilerliste festgelegt werden. 
  
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


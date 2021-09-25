---
title: PidTagDiscreteValues (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8cb2e6968a84869719060192d805cc94c60c8f3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563644"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>PidTagDiscreteValues (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nichtzustellbarkeitsbericht nur auf diskrete Mitglieder einer Verteilerliste und nicht auf die gesamte Liste angewendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Kennung:  <br/> |0x0E0E  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird in einem Nichtzustellbarkeitsbericht verwendet, wenn die Nachricht nicht an ein oder mehrere Mitglieder einer Verteilerliste übermittelt werden konnte. Der Zweck besteht darin, die Wiederholungsversuche auf diese einzelnen Mitglieder und nicht auf die Verteilerliste als Ganzes zu beschränken. 
  
Die Empfängertabelle eines Nichtzustellbarkeitsberichts enthält Einträge für alle Empfänger, denen die Nachricht nicht zugestellt werden konnte, und ggf. auch für die Verteilerlisten, zu denen sie gehören. Der Transportanbieter sollte diese Eigenschaft für jeden Verteilerlisteneintrag auf TRUE festlegen und die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) aus der Verteilerliste in **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) und **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))-Eigenschaften für jedes Mitglied dieser Verteilerliste. 
  
 **PR_DISCRETE_VALUES** sollte nicht für einen empfängerfremden Empfängereintrag als eine Verteilerliste festgelegt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


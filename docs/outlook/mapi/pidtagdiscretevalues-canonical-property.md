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
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404841"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>PidTagDiscreteValues (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Nicht-Verteilerbericht nur für einzelne Mitglieder einer Verteilerliste und nicht für die gesamte Liste gilt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Kennung:  <br/> |0x0E0E  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird innerhalb eines Nicht-Verteilerberichts verwendet, wenn die Nachricht nicht an ein oder mehrere Mitglieder einer Verteilerliste zugestellt werden konnte. Ihr Zweck besteht in der Beschränkung der Erneutübertragungsversuche auf die einzelnen Mitglieder und nicht auf die Verteilerliste als Ganzes. 
  
Die Empfängertabelle eines Unzustellbarberichts enthält Einträge für alle Empfänger, denen die Nachricht nicht zugestellt werden konnte, sowie für die Verteilerlisten, zu denen sie gehören. Der Transportanbieter sollte diese Eigenschaft für jeden Verteilerlisteneintrag auf TRUE festlegen und die **Eigenschaften PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_SEARCH_KEY** ( PidTagSearchKey ) aus der Verteilerliste in **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) und **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) für jedes Mitglied dieser Verteilerliste kopieren.[](pidtagsearchkey-canonical-property.md) 
  
 **PR_DISCRETE_VALUES** sollte nicht für einen anderen Empfängereintrag als eine Verteilerliste festgelegt werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


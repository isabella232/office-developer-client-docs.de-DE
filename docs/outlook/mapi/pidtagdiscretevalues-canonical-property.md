---
title: Kanonische Pidtagdiscretevalues (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360823"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Kanonische Pidtagdiscretevalues (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Unzustellbarkeitsbericht nur auf diskrete Mitglieder einer Verteilerliste anstatt auf die gesamte Liste angewendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Kennung:  <br/> |0x0E0E  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in einem Unzustellbarkeitsbericht verwendet, wenn die Nachricht nicht an ein oder mehrere Mitglieder einer Verteilerliste zugestellt werden konnte. Der Zweck besteht darin, die Wiederholungsversuche auf die einzelnen Mitglieder und nicht auf die Verteilerliste als Ganzes zu begrenzen. 
  
Die Empfängertabelle eines Unzustellbarkeitsberichts enthält Einträge für alle Empfänger, an die die Nachricht nicht übermittelt werden konnte, sowie an die Verteilerlisten, falls vorhanden, zu denen Sie gehören. Der Transportanbieter sollte diese Eigenschaft für jeden Verteilerlisteneintrag auf TRUE festlegen und die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_SEARCH_KEY** ([ Pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) aus der Verteilerliste nach **PR_ORIGINAL_DISPLAY_NAME** ([pidtagoriginaldisplayname (](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([pidtagoriginalentryid (](pidtagoriginalentryid-canonical-property.md)) und **PR_ORIGINAL_SEARCH_KEY** ([ Pidtagoriginalsearchkey (](pidtagoriginalsearchkey-canonical-property.md))-Eigenschaften für jedes Mitglied dieser Verteilerliste. 
  
 **PR_DISCRETE_VALUES** sollte nicht für einen nicht Zustellungs Berichts-Empfängereintrag außer einer Verteilerliste festgelegt werden. 
  
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


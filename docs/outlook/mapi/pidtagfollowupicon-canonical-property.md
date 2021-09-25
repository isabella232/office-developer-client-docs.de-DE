---
title: PidTagFollowupIcon (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8fb1a570f2bad075c69a9328427de53e86fab938
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563553"
---
# <a name="pidtagfollowupicon-canonical-property"></a>PidTagFollowupIcon (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Flagfarbe des Nachrichtenobjekts an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Kennung:  <br/> |0x1095  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenordner umbenennen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft darf nur vorhanden sein, wenn der Wert der **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) -Eigenschaft auf "followupFlagged" festgelegt ist oder das Nachrichtenobjekt ein Besprechungsobjekt ist. Diese Eigenschaft sollte für ein Aufgabenobjekt nicht vorhanden sein. Wenn sie für andere Nachrichtenobjekte festgelegt wird, muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden.
  
|**Numerischer Wert**|**Name**|**Beschreibung**|
|:-----|:-----|:-----|
|Nicht vorhanden  <br/> |-  <br/> |Keine Farbe  <br/> |
|1  <br/> |followupIcon1  <br/> |Lila  <br/> |
|2  <br/> |followupIcon2  <br/> |Orangefarbene Kennzeichnung  <br/> |
|3  <br/> |followupIcon3  <br/> |Grüne Kennzeichnung  <br/> |
|4   <br/> |followupIcon4  <br/> |Gelbe Kennzeichnung  <br/> |
|5  <br/> |followupIcon5  <br/> |Blaue Kennzeichnung  <br/> |
|6   <br/> |followupIcon6  <br/> |Rote Kennzeichnung  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
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


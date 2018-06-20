---
title: Kanonische PidTagFollowupIcon-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 39840f27d67daca625daea08555ab89d5a362e63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794389"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Kanonische PidTagFollowupIcon-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt die Kennzeichnungsfarbe des Message-Objekts.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Bezeichner:  <br/> |0x1095  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Benennen Sie Nachrichtenordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft darf nicht vorhanden sein, es sei denn, der Wert der **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md))-Eigenschaft auf "FollowupFlagged" festgelegt ist, oder Message-Objekts ein bezüglich Besprechungen-Objekt ist. Diese Eigenschaft sollte auf ein Task-Objekt nicht vorhanden. Bei Festlegung auf andere Nachrichtenobjekte, muss diese Eigenschaft auf einen der folgenden Werte festgelegt sein.
  
|**Numerischen Wert**|**Name**|**Beschreibung**|
|:-----|:-----|:-----|
|Nicht vorhanden  <br/> |n/v  <br/> |Keine Farbe  <br/> |
|1  <br/> |followupIcon1  <br/> |Lila Kennzeichnung  <br/> |
|2  <br/> |followupIcon2  <br/> |Orange Kennzeichnung  <br/> |
|3  <br/> |followupIcon3  <br/> |Grüne Kennzeichnung  <br/> |
|4  <br/> |followupIcon4  <br/> |Gelbe Kennzeichnung  <br/> |
|5  <br/> |followupIcon5  <br/> |Blaue Kennzeichnung  <br/> |
|6  <br/> |followupIcon6  <br/> |Rote Kennzeichnung  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


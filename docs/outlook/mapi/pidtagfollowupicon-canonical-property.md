---
title: Kanonische Pidtagfollowupicon (-Eigenschaft
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
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316282"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Kanonische Pidtagfollowupicon (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die flagfarbe des Message-Objekts an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Kennung:  <br/> |0x1095  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Nachrichten Ordner umbenennen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft darf nur vorhanden sein, wenn der Wert der **PR_FLAG_STATUS** ([pidtagflagstatus (](pidtagflagstatus-canonical-property.md))-Eigenschaft auf "followupFlagged" festgelegt ist oder das Message-Objekt ein Besprechungs bezogenes Objekt ist. Diese Eigenschaft sollte in einem Task-Objekt nicht vorhanden sein. Wenn diese Eigenschaft für andere Nachrichtenobjekte festgelegt ist, muss Sie auf einen der folgenden Werte festgelegt werden.
  
|**Numerischer Wert**|**Name**|**Beschreibung**|
|:-----|:-----|:-----|
|Nicht vorhanden  <br/> |Nicht zutreffend  <br/> |Keine Farbe  <br/> |
|1  <br/> |followupIcon1  <br/> |Violette Kennzeichnung  <br/> |
|2  <br/> |followupIcon2  <br/> |Orangefarbene Kennzeichnung  <br/> |
|3  <br/> |followupIcon3  <br/> |Grüne Kennzeichnung  <br/> |
|4  <br/> |followupIcon4  <br/> |Gelbe Kennzeichnung  <br/> |
|5  <br/> |followupIcon5  <br/> |Blaue Kennzeichnung  <br/> |
|6  <br/> |followupIcon6  <br/> |Rote Kennzeichnung  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidTagFlagStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9793115f67c5c889d8c674e0279516177aac837a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616439"
---
# <a name="pidtagflagstatus-canonical-property"></a>PidTagFlagStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Flagstatus des Nachrichtenobjekts an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FLAG_STATUS  <br/> |
|Kennung:  <br/> |0x1090  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft darf nicht in einem Besprechungsobjekt vorhanden sein, und sie sollte nicht für ein Aufgabenobjekt vorhanden sein. Wenn sie für andere Nachrichtenobjekte festgelegt wird, muss diese Eigenschaft auf einen der folgenden Werte festgelegt werden:
  
|**Numerischer Wert**|**Name**|**Beschreibung**|
|:-----|:-----|:-----|
|Nicht vorhanden  <br/> |Nicht zutreffend  <br/> |Nicht entflaggt  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Gekennzeichnet abgeschlossen  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Gekennzeichnet  <br/> |
   
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


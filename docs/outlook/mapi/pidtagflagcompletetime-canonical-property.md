---
title: PidTagFlagCompleteTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fed617b195ad2615df26a4db8e4844a8d766f18a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616453"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>PidTagFlagCompleteTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt das Datum und die Uhrzeit in koordinierter Weltzeit (COORDINATED Universal Time, UTC) an, an dem das Nachrichtenobjekt als abgeschlossen gekennzeichnet wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|Kennung:  <br/> |0x1091  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird gelöscht, wenn das Nachrichtenobjekt nicht als abgeschlossen gekennzeichnet ist. Die kleinste Auflösung der Zeit muss Minuten sein (der Wert muss ein Vielfaches von 600.000.000 sein). Diese Eigenschaft darf nicht vorhanden sein, wenn es sich bei dem Objekt um ein besprechungsbezogenes Objekt handelt, und sie sollte nicht für ein Aufgabenobjekt vorhanden sein.
  
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


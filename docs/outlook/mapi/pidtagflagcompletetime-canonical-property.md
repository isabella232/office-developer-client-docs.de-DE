---
title: Kanonische PidTagFlagCompleteTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: efaa8cf84204234697431a190a5cb6745b55ecae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794360"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>Kanonische PidTagFlagCompleteTime-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt das Datum und die Uhrzeit in Coordinated Universal Time (UTC), die das Objekt "Message" als abgeschlossen gekennzeichnet wurde.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|Bezeichner:  <br/> |0x1091  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird gelöscht, wenn das Objekt "Message" nicht abgeschlossen gekennzeichnet ist. Die Zeit kleinsten Auflösung muss Minuten (der Wert muss ein Vielfaches von 600,000,000). Diese Eigenschaft muss nicht vorhanden, wenn das Objekt ein Objekt bezüglich Besprechungen ist und sollte nicht auf ein Task-Objekt vorhanden sein.
  
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


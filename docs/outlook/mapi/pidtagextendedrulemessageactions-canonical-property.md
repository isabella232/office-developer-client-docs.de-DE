---
title: PidTagExtendedRuleMessageActions (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5425496a5b7845daabf736978e6ed24518451fe0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794378"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>PidTagExtendedRuleMessageActions (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält zusätzliche Informationen zu den benannten Eigenschaften in einer Nachricht Ordner verknüpften Informationen (FAI) verwendet.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Bezeichner:  <br/> |0x0E99  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft muss auf eine Nachricht FAI festgelegt werden. Diese Eigenschaft dient dem gleichen Zweck als **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), jedoch enthält zusätzliche Informationen zur Version der benannten Eigenschaften in die Regelaktion gespeichert und die Regel sowie Informationen zu den Aktionen werden Durch diese Regel ausgeführt. Alle String-Werten, die in einem beliebigen Teil des Puffers Aktion verwendet, um Aktionen enthalten enthalten sind, muss im Unicode-Format.
  
Informationen zum Format dieser binäre Eigenschaft finden Sie unter [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.
    
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


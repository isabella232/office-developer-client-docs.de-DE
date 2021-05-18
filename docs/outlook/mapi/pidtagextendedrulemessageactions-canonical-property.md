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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316338"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>PidTagExtendedRuleMessageActions (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält zusätzliche Informationen zu den benannten Eigenschaften, die in einer Folder Associated Information (FAI)-Nachricht verwendet werden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Kennung:  <br/> |0x0E99  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss für eine FAI-Nachricht festgelegt werden. Diese Eigenschaft dient dem gleichen Zweck wie **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), enthält jedoch zusätzliche Informationen zur Version der Regel und zu den benannten Eigenschaften, die in der Regelaktion gespeichert sind, sowie Informationen zu den aktionen, die von dieser Regel ausgeführt werden sollen. Alle Zeichenfolgenwerte, die in einem Beliebigen Teil des Aktionspuffers enthalten sind, der Aktionen enthält, müssen im Unicode-Format vorliegen.
  
Informationen zum Format dieser binären Eigenschaft finden Sie unter [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: Kanonische Pidtagrulestate (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338612"
---
# <a name="pidtagrulestate-canonical-property"></a>Kanonische Pidtagrulestate (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Wert, der als Bitmasken Kombination von Flags interpretiert wird, die den Status der Regel angeben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_STATE  <br/> |
|Kennung:  <br/> |0x6677  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Server seitige Regeln  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle sind die möglichen Werte dieser Eigenschaft definiert.
  
DE (ST_ENABLED, Bitmaske 0x00000001)
  
> Die Regel ist für die Ausführung aktiviert. Wenn dieses Flag nicht festgelegt ist, muss der Server diese Regel beim Auswerten von Regeln überspringen.
    
ER (ST_ERROR, Bitmaske 0x00000002)
  
> Der Server hat einen Fehler bei der Verarbeitung der Regel festgestellt.
    
OF (ST_ONLY_WHEN_OOF, Bitmaske 0x00000004)
  
> Die Regel wird nur ausgeführt, wenn der Benutzer den Abwesenheitsstatus (abwesend) für das Postfach festlegt. Dieses Flag darf nicht in einer Regel für Öffentliche Ordner festgelegt werden.
    
Hallo (ST_KEEP_OOF_HIST, Bitmaske 0x00000008)
  
> Dieses Flag darf nicht in einer Regel für Öffentliche Ordner festgelegt werden.
    
EL (ST_EXIT_LEVEL, Bitmaske 0x00000010)
  
> Die Regelauswertung endet nach der Ausführung dieser Regel, mit Ausnahme der Auswertung von Abwesenheitsregeln.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, Bitmaske 0x00000020)
  
> Die Auswertung dieser Regel kann übersprungen werden.
    
PE (ST_RULE_PARSE_ERROR, Bitmaske 0x00000040)
  
> Beim Analysieren der vom Client bereitgestellten Regel Daten ist ein Fehler aufgetreten.
    
X
  
> Wird von diesem Protokoll nicht verwendet. Dieses Bit darf vom Client nicht geändert werden.
    
Beachten Sie die Interaktion zwischen ST_ONLY_WHEN_OOF-und ST_EXIT_LEVEL-Flags: 
  
Wenn der Status "Abwesenheit" für das Postfach festgelegt ist und eine Regelbedingung "TRUE" ergibt, 
  
UND
  
- Die Regel hat das ST_EXIT_LEVEL-Flag festgelegt und verfügt nicht über ST_ONLY_WHEN_OOF-Flagsatz. Anschließend darf der Server nachfolgende Regeln, für die kein ST_ONLY_WHEN_OOF-Flag festgelegt ist, auswerten und nachfolgende Regeln auswerten, die ST_ONLY_WHEN_OOF-Flagsatz aufweisen.
    
ODER
  
- Die Regel weist sowohl die ST_EXIT_LEVEL-als auch die ST_ONLY_WHEN_OOF-Flags auf. Anschließend darf der Server keine nachfolgenden Regeln auswerten.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende e-Mail-Nachrichten auf einem Server.
    
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


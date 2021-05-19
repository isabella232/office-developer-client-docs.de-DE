---
title: PidTagRuleState (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338612"
---
# <a name="pidtagrulestate-canonical-property"></a>PidTagRuleState (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Wert, der als Bitmaskenkombination von Flags interpretiert wird, die den Status der Regel angeben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RULE_STATE  <br/> |
|Kennung:  <br/> |0x6677  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

In der folgenden Tabelle werden die möglichen Werte dieser Eigenschaft definiert.
  
EN (ST_ENABLED, bitmask 0x00000001)
  
> Die Regel ist für die Ausführung aktiviert. Wenn dieses Flag nicht festgelegt ist, muss der Server diese Regel beim Auswerten von Regeln überspringen.
    
ER (ST_ERROR, bitmask 0x00000002)
  
> Auf dem Server ist ein Fehler bei der Verarbeitung der Regel aufgetreten.
    
OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)
  
> Die Regel wird nur ausgeführt, wenn der Benutzer den Status Out of Office (OOF) für das Postfach fest legt. Dieses Flag darf nicht in einer Regel für öffentliche Ordner festgelegt werden.
    
HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)
  
> Dieses Flag darf nicht in einer Regel für öffentliche Ordner festgelegt werden.
    
EL (ST_EXIT_LEVEL, bitmask 0x00000010)
  
> Die Regelauswertung endet nach der Ausführung dieser Regel, mit Ausnahme der Auswertung von Out of Office Regeln.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)
  
> Die Auswertung dieser Regel kann übersprungen werden.
    
PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)
  
> Auf dem Server ist ein Fehler aufgetreten, bei dem die vom Client bereitgestellten Regeldaten analyset werden.
    
X
  
> Von diesem Protokoll nicht verwendet. Dieses Bit darf vom Client nicht geändert werden.
    
Hinweis zur Interaktion zwischen ST_ONLY_WHEN_OOF und ST_EXIT_LEVEL Flags: 
  
Wenn der Status "Out of Office" für das Postfach festgelegt ist und eine Regelbedingung auf TRUE ausgewertet wird, 
  
AND:
  
- Für die Regel ist ST_EXIT_LEVEL Flag festgelegt und ST_ONLY_WHEN_OOF festgelegt. Anschließend darf der Server keine nachfolgenden Regeln auswerten, für die ST_ONLY_WHEN_OOF festgelegt ist, und nachfolgende Regeln mit ST_ONLY_WHEN_OOF auswerten.
    
OR:
  
- Für die Regel sind die ST_EXIT_LEVEL und ST_ONLY_WHEN_OOF festgelegt. Anschließend darf der Server keine nachfolgenden Regeln auswerten.
    
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


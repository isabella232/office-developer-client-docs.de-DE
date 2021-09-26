---
title: PidTagRuleState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c28c4af9117ca0aee1b19ecef812c2636860c45c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599494"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

In der folgenden Tabelle werden die möglichen Werte dieser Eigenschaft definiert.
  
EN (ST_ENABLED, Bitmaske 0x00000001)
  
> Die Regel ist für die Ausführung aktiviert. Wenn dieses Kennzeichen nicht festgelegt ist, muss der Server diese Regel beim Auswerten von Regeln überspringen.
    
ER (ST_ERROR, Bitmaske 0x00000002)
  
> Beim Verarbeiten der Regel ist auf dem Server ein Fehler aufgetreten.
    
OF (ST_ONLY_WHEN_OOF, Bitmaske 0x00000004)
  
> Die Regel wird nur ausgeführt, wenn der Benutzer den OOF-Status (Out of Office) für das Postfach festlegt. Dieses Flag darf nicht in einer Regel für öffentliche Ordner festgelegt werden.
    
HI (ST_KEEP_OOF_HIST, Bitmaske 0x00000008)
  
> Dieses Flag darf nicht in einer Regel für öffentliche Ordner festgelegt werden.
    
EL (ST_EXIT_LEVEL, Bitmaske 0x00000010)
  
> Die Regelauswertung endet nach der Ausführung dieser Regel, mit Ausnahme der Auswertung von Out of Office Regeln.
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, Bitmaske 0x00000020)
  
> Die Auswertung dieser Regel kann übersprungen werden.
    
PE (ST_RULE_PARSE_ERROR, Bitmaske 0x00000040)
  
> Auf dem Server ist ein Fehler beim Analysieren der regeldaten aufgetreten, die vom Client bereitgestellt werden.
    
X
  
> Wird von diesem Protokoll nicht verwendet. Dieses Bit darf nicht vom Client geändert werden.
    
Beachten Sie die Interaktion zwischen ST_ONLY_WHEN_OOF und ST_EXIT_LEVEL Flags: 
  
Wenn der Status "Nicht mehr Office" für das Postfach festgelegt ist und eine Regelbedingung auf TRUE ausgewertet wird, 
  
UND:
  
- Für die Regel ist das ST_EXIT_LEVEL-Kennzeichen festgelegt und ST_ONLY_WHEN_OOF Flag nicht festgelegt. Anschließend darf der Server keine nachfolgenden Regeln auswerten, für die ST_ONLY_WHEN_OOF Flag nicht festgelegt ist, und nachfolgende Regeln, für die ST_ONLY_WHEN_OOF Flag festgelegt wurde, auswerten.
    
ODER:
  
- Für die Regel sind sowohl die ST_EXIT_LEVEL als auch ST_ONLY_WHEN_OOF Flags festgelegt. Anschließend darf der Server keine nachfolgenden Regeln auswerten.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.
    
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


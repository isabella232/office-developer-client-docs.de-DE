---
title: Kanonische PidTagRuleState-Eigenschaft
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
ms.openlocfilehash: 519ee2b91275e4253845afa35a9a80470071966d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795051"
---
# <a name="pidtagrulestate-canonical-property"></a>Kanonische PidTagRuleState-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Ein Wert, der als eine Bitmaske Kombination von Flags, die angeben, den Status der Regel interpretiert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RULE_STATE  <br/> |
|Bezeichner:  <br/> |0x6677  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Serverseitige Regeln  <br/> |
   
## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die möglichen Werte dieser Eigenschaft an.
  
De-de (ST_ENABLED, 0 x 00000001 Bitmaske)
  
> Die Regel ist für die Ausführung aktiviert. Wenn dieses Flag nicht festgelegt ist, muss der Server diese Regel überspringen, beim Auswerten der Regeln.
    
ER (ST_ERROR, 0 x 00000002 Bitmaske)
  
> Der Server ist Verarbeitung der Regel einen Fehler aufgetreten.
    
DER (ST_ONLY_WHEN_OOF, 0 x 00000004 Bitmaske)
  
> Die Regel wird ausgeführt, nur, wenn der Benutzer den Status von Office (OOF) für das Postfach festlegt. Dieses Kennzeichen müssen in einer Regel für Öffentliche Ordner nicht festgelegt werden.
    
HI (ST_KEEP_OOF_HIST, 0 x 00000008 Bitmaske)
  
> Dieses Kennzeichen müssen in einer Regel für Öffentliche Ordner nicht festgelegt werden.
    
EL (ST_EXIT_LEVEL, 0 x 00000010 Bitmaske)
  
> Auswertung der Regel werden nach dem Ausführen dieser Regel, mit Ausnahme der Auswertung von Abwesenheitsnotizen Regeln beendet.
    
SCL-Bewertung (ST_SKIP_IF_SCL_IS_SAFE, 0 x 00000020 Bitmaske)
  
> Auswertung dieser Regel möglicherweise übersprungen werden.
    
PE (ST_RULE_PARSE_ERROR, 0 x 00000040 Bitmaske)
  
> Der Server ist ein Fehler, die Analyse der Regeldaten vom Client aufgetreten.
    
X
  
> Von dieses Protokoll nicht verwendet. Dieses Bit muss vom Client nicht geändert werden.
    
Beachten Sie auf die Interaktion zwischen ST_ONLY_WHEN_OOF und ST_EXIT_LEVEL Flags: 
  
Wenn der Status "Abwesend" für das Postfach festgelegt ist, und eine Bedingung TRUE ergibt, 
  
UND:
  
- Die Regel muss das ST_EXIT_LEVEL-Flag festlegen und keinen ST_ONLY_WHEN_OOF-Flag festlegen. Klicken Sie dann der Server muss nicht ausgewertet werden nachfolgende Regeln, die keine ST_ONLY_WHEN_OOF flag festgelegt und nachfolgende Regeln, die ST_ONLY_WHEN_OOF gekennzeichnet sind ausgewertet werden.
    
ODER:
  
- Die Regel verwendet den ST_EXIT_LEVEL und die ST_ONLY_WHEN_OOF Flags festgelegt. Klicken Sie dann, muss der Server nicht ausgewertet werden alle nachfolgenden Regeln.
    
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


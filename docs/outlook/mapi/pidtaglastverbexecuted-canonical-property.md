---
title: PidTagLastVerbExecuted (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9abd4eb955428595ebe41ab9b2c661303ee2779a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279615"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>PidTagLastVerbExecuted (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das letzte ausgeführte Verb.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|Kennung:  <br/> |0x1081  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Verlauf  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann einen der folgenden Werte haben:
  
|**Verb**|**Eigenschaftswert**|
|:-----|:-----|
|Beitrag  <br/> |0x00000001  <br/> |
|Andere  <br/> |0x00000003  <br/> |
|Lesen von E-Mails  <br/> |0x00000100  <br/> |
|Ungelesene E-Mails  <br/> |0x00000101  <br/> |
|Gesendete E-Mails  <br/> |0x00000102  <br/> |
|Nicht gesendete E-Mails  <br/> |0x00000103  <br/> |
|Empfangsmail  <br/> |0x00000104  <br/> |
|Beantwortete E-Mails  <br/> |0x00000105  <br/> |
|Weitergeleitete E-Mails  <br/> |0x00000106  <br/> |
|Remote-E-Mail  <br/> |0x00000107  <br/> |
|Zustellungsbestätigung  <br/> |0x00000108  <br/> |
|Lesebestätigung  <br/> |0x00000109  <br/> |
|Nondelivery Receipt  <br/> |0x0000010A  <br/> |
|Ungelesener Beleg  <br/> |0x0000010B  <br/> |
|Recall_S E-Mail  <br/> |0x0000010C  <br/> |
|Recall_F E-Mail  <br/> |0x0000010D  <br/> |
|Nachverfolgen von E-Mails  <br/> |0x0000010E  <br/> |
|Out of Office mail  <br/> |0x0000011B  <br/> |
|Rückruf von E-Mails  <br/> |0x0000011C  <br/> |
|Nachverfolgte E-Mails  <br/> |0x00000139  <br/> |
|Kontakt  <br/> |0x00000200  <br/> |
|Verteilerliste  <br/> |0x00000201  <br/> |
|Sticky Note, Blue  <br/> |0x00000300  <br/> |
|Sticky Note, Green  <br/> |0x00000301  <br/> |
|Sticky Note, Pink  <br/> |0x00000302  <br/> |
|Sticky Note, Yellow  <br/> |0x00000303  <br/> |
|Sticky Note, White  <br/> |0x00000304  <br/> |
|Termin für eine einzelne Instanz  <br/> |0x00000400  <br/> |
|Terminserie  <br/> |0x00000401  <br/> |
|Besprechung mit einer instanz  <br/> |0x00000402  <br/> |
|Besprechungsserie  <br/> |0x00000403  <br/> |
|Besprechungsanfrage/ vollständiges Update  <br/> |0x00000404  <br/> |
|Annehmen  <br/> |0x00000405  <br/> |
|Decline  <br/> |0x00000406  <br/> |
|Mit Zag  <br/> |0x00000407  <br/> |
|Abbrechen  <br/> |0x00000408  <br/> |
|Informationsupdate  <br/> |0x00000409  <br/> |
|Vorgangs-/Aufgabenupdate  <br/> |0x00000500  <br/> |
|Nicht zugewiesene wiederkehrende Aufgabe  <br/> |0x00000501  <br/> |
|Aufgabe des Assignee  <br/> |0x00000502  <br/> |
|Aufgabe des Assigners  <br/> |0x00000503  <br/> |
|Aufgabenanfrage  <br/> |0x00000504  <br/> |
|Aufgabenakzeptanz  <br/> |0x00000505  <br/> |
|Vorgangsverweigerung  <br/> |0x00000506  <br/> |
|Journal-Unterhaltung  <br/> |0x00000601  <br/> |
|Journal-E-Mail-Nachricht  <br/> |0x00000602  <br/> |
|Journal-Besprechungsanfrage  <br/> |0x00000603  <br/> |
|Antwort auf Journal-Besprechungen  <br/> |0x00000604  <br/> |
|Journalaufgabesanforderung  <br/> |0x00000606  <br/> |
|Antwort auf Journalaufgabe  <br/> |0x00000607  <br/> |
|Journalnotiz  <br/> |0x00000608  <br/> |
|Journalfax  <br/> |0x00000609  <br/> |
|Journalanruf Telefon  <br/> |0x0000060A  <br/> |
|Journalaufgabe  <br/> |0x0000060B  <br/> |
|Journal Letter  <br/> |0x0000060C  <br/> |
|Journal Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Journal Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Journal Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Journal Microsoft Office Access  <br/> |0x00000610  <br/> |
|Journaldokument  <br/> |0x00000612  <br/> |
|Journal besprechung  <br/> |0x00000613  <br/> |
|Abbruch der Journalsitzung  <br/> |0x00000614  <br/> |
|Journal-Remotesitzung  <br/> |0x00000615  <br/> |
|Neue E-Mails  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
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


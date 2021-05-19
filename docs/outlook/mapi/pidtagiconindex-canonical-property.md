---
title: PidTagIconIndex (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346620"
---
# <a name="pidtagiconindex-canonical-property"></a>PidTagIconIndex (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zahl, die angibt, welches Symbol beim Anzeigen einer Gruppe von E-Mail-Objekten verwendet werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ICON_INDEX  <br/> |
|Kennung:  <br/> |0x1080  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist, falls vorhanden, ein Hinweis an den Client. Der Client kann den Wert dieser Eigenschaft ignorieren. 
  
|**E-Mail-Elementstatus**|**Symbolindex**|
|:-----|:-----|
|Neue E-Mails  <br/> |0xFFFFFFFF  <br/> |
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
|Zustellungs-E-Mails  <br/> |0x00000108  <br/> |
|Lesen von E-Mails  <br/> |0x00000109  <br/> |
|Nondelivery-E-Mails  <br/> |0x0000010A  <br/> |
|Nicht gelesene E-Mails  <br/> |0x0000010B  <br/> |
|Recall_S E-Mail  <br/> |0x0000010C  <br/> |
|Recall_F E-Mail  <br/> |0x0000010D  <br/> |
|Nachverfolgen von E-Mails  <br/> |0x0000010E  <br/> |
|Out-of-Office-E-Mails  <br/> |0x0000011B  <br/> |
|Rückruf von E-Mails  <br/> |0x0000011C  <br/> |
|Nachverfolgte E-Mails  <br/> |0x00000130  <br/> |
|Kontakt  <br/> |0x00000200  <br/> |
|Verteilerliste  <br/> |0x00000202  <br/> |
|Sticky note blue  <br/> |0x00000300  <br/> |
|Sticky note green  <br/> |0x00000301  <br/> |
|Sticky note pink  <br/> |0x00000302  <br/> |
|Klebenotiz gelb  <br/> |0x00000303  <br/> |
|Klebenotiz weiß  <br/> |0x00000304  <br/> |
|Termin für eine einzelne Instanz  <br/> |0x00000400  <br/> |
|Terminserie  <br/> |0x00000401  <br/> |
|Besprechung mit einer instanz  <br/> |0x00000402  <br/> |
|Besprechungsserie:  <br/> |0x00000403  <br/> |
|Besprechungsanfrage  <br/> |0x00000404  <br/> |
|Annehmen  <br/> |0x00000405  <br/> |
|Decline  <br/> |0x00000406  <br/> |
|Tentativ  <br/> |0x00000407  <br/> |
|Stornierung  <br/> |0x00000408  <br/> |
|Informationsupdate  <br/> |0x00000409  <br/> |
|Aufgabe/Aufgabe  <br/> |0x00000500  <br/> |
|Nicht zugewiesene Wiederkehrende Aufgabe  <br/> |0x00000501  <br/> |
|Aufgabe des Assignee  <br/> |0x00000502  <br/> |
|Aufgabe des Assigners  <br/> |0x00000503  <br/> |
|Aufgabenanforderung  <br/> |0x00000504  <br/> |
|Aufgabenakzeptanz  <br/> |0x00000505  <br/> |
|Vorgangsverweigerung  <br/> |0x00000506  <br/> |
|Journal-Unterhaltung  <br/> |0x00000601  <br/> |
|Journal-E-Mail-Nachricht  <br/> |0x00000602  <br/> |
|Journal-Besprechungsanfrage  <br/> |0x00000603  <br/> |
|Journal-Besprechungsantwort  <br/> |0x00000604  <br/> |
|Journal-Aufgabenanforderung  <br/> |0x00000606  <br/> |
|Antwort auf Journalaufgabe  <br/> |0x00000607  <br/> |
|Journalnotiz  <br/> |0x00000608  <br/> |
|Journalfax  <br/> |0x00000609  <br/> |
|Journaltelefonanruf  <br/> |0x0000060A  <br/> |
|Journalbuchstabe  <br/> |0x0000060C  <br/> |
|Journal Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Journal Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Journal Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Journal Microsoft Office Access  <br/> |0x00000610  <br/> |
|Journaldokument  <br/> |0x00000612  <br/> |
|Journal besprechung  <br/> |0x00000613  <br/> |
|Besprechungsabsagen in Journalen  <br/> |0x00000614  <br/> |
|Journal-Remotesitzung  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
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


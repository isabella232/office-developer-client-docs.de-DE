---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 119cd7edc5b9b615a39cea6aa1c405c396ce2afa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793436"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionEndDisplay (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) ist der die Beschreibung für die Zeitzone gespeichert, die verwendet wird, wenn das Ende einer Einzelinstanz-Termin oder eine Besprechungsanfrage ausgewählt ist. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000825F  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Microsoft Office Outlook 2003 oder früher und Lösungen, basieren auf Collaboration Data Objects (CDO) 1.2.1 und, die das Calendar Update-Tool nicht für Microsoft Outlook und Microsoft Exchange Server ausgeführt haben, Speichern der Start- und Endzeit der Einzel-Instanz Termine und Besprechungsanfragen in koordinierter Weltzeit (UTC). Diese Clients speichern keine Informationen für die Zeitzone, in dem die Termin- oder Besprechungsanfragen erstellt wird.
  
Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und CDO 1.2.1-basierter Lösungen, die im Kalender von Outlook oder Exchange Server ausgeführt haben aktualisieren Tool verwenden **DispidApptTZDefEndDisplay** , um die Zeitzone für die Endzeit zu speichern. **DispidApptTZDefEndDisplay** zeigt Termin oder eine Besprechung in der ursprünglichen Zeitzone, die es geplant wurde, und legt fest, ob die Endzeit angepasst werden sollten, wenn die Regeln der Zeitzone ändern. Wenn diese Eigenschaft nicht vorhanden ist, wird der Zeitzone angegeben, die von der **DispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md))-Eigenschaft verwendet. Wenn **DispidApptTZDefStartDisplay** fehlt oder ist ungültig ist, wird davon ausgegangen, dass die aktuellen Ortszeitzone. **DispidApptTZDefEndDisplay** wird nur für die Anzeige verwendet und ist nicht in Serie Erweiterung verwendet. 
  
Ein Parser wird beim Lesen eines Streams von **DispidApptTZDefEndDisplay**abgerufen, oder wenn er in ein Stream-Objekt für eine binäre Eigenschaft wie **DispidApptTZDefEndDisplay**Engagement **TZDEFINITION** beibehalten. Weitere Informationen finden Sie unter [Speichern von TZDEFINITION in ein Stream-Objekt an eine binäre Eigenschaft übermittelt werden](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **DispidApptTZDefEndDisplay** gibt die Informationen zur Zeitzone für die Eigenschaft **DispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). Das Format, Einschränkungen und Berechnung von **DispidApptTZDefEndDisplay** sind identisch mit der in der **DispidApptTZDefStartDisplay** -Eigenschaft angegeben. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


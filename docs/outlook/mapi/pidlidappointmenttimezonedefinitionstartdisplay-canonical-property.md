---
title: Kanonische PidLidAppointmentTimeZoneDefinitionStartDisplay-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793449"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Kanonische PidLidAppointmentTimeZoneDefinitionStartDisplay-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) ist der die Beschreibung für die Zeitzone gespeichert, die verwendet wird, wenn die Anfangszeit der eine Einzelinstanz-Termin oder eine Besprechungsanfrage ausgewählt ist. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000825E  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Microsoft Office Outlook 2003 oder früher und Lösungen, basieren auf Collaboration Data Objects (CDO) 1.2.1 und, die das Calendar Update-Tool nicht für Microsoft Outlook und Microsoft Exchange Server ausgeführt haben, Speichern der Start- und Endzeit der Einzel-Instanz Termine und Besprechungsanfragen in koordinierter Weltzeit (UTC). Diese Clients speichern keine Informationen für die Zeitzone in denen die Termin- oder Besprechungsanfragen erstellt wird.
  
Versionen von Outlook im Vergleich zu Microsoft Office Outlook 2007 und CDO 1.2.1-basierter Lösungen, die Outlook oder Exchange Server-Update Kalendertools ausgeführt haben mit dieser Eigenschaft können Sie um die Zeitzone für die Startzeit zu speichern. Die **DispidApptTZDefStartDisplay** -Eigenschaft zeigt, dass es geplant wurde Termin oder eine Besprechung in der ursprünglichen Zeitzone. Bestimmt, ob die Startzeit angepasst werden sollten, wenn die Regeln der Zeitzone ändern. Wenn diese Eigenschaft nicht vorhanden ist, wird davon ausgegangen, dass die aktuelle lokale Zeitzone. Diese Eigenschaft wird nur für die Anzeige verwendet und ist nicht in Serie Erweiterung verwendet. 
  
Ein Parser wird beim Lesen eines Streams von dieser Eigenschaft abgerufen oder wenn er in ein Stream-Objekt für eine binäre Eigenschaft wie **DispidApptTZDefStartDisplay**Engagement **TZDEFINITION** beibehalten. Weitere Informationen finden Sie unter [Speichern von TZDEFINITION in ein Stream-Objekt an eine binäre Eigenschaft übermittelt werden](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Diese Eigenschaft gibt die Informationen zur Zeitzone für die Eigenschaft **DispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). Der Wert der **DispidApptTZDefStartDisplay** wird verwendet, um das Startdatum und die Uhrzeit aus UTC in die lokale Zeitzone für die Anzeige zu konvertieren. Für jede **TZRULE** von dieser Eigenschaft angegeben wird muss das Flag TZRULE_FLAG_RECUR_CURRENT_TZREG nicht festgelegt werden. Beispielsweise ist der **TZRULE** die effektive Regel, muss der Wert des Felds, **TZRULE** "0 x 0002"; werden Andernfalls müssen sie "0 x 0000" sein. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
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


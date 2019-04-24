---
title: Kanonische Pidlidappointmenttimezonedefinitionstartdisplay (-Eigenschaft
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
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345017"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Kanonische Pidlidappointmenttimezonedefinitionstartdisplay (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Stream, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die verwendet wird, wenn die Startzeit eines einzelnen Termins oder einer Besprechungsanfrage ausgewählt wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x0000825E  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Microsoft Office Outlook 2003 oder früher und Lösungen, die auf Collaboration Data Objects (CDO) 1.2.1 basieren und nicht das Kalender Aktualisierungstool für Outlook oder Microsoft Exchange Server ausgeführt haben, speichern Sie die Startzeit und die Endzeit der einzelnen Instanz. Termine und Besprechungsanfragen in koordinierter weltZeit (UTC). Diese Clients speichern keine Informationen für die Zeitzone, in der der Termin oder die Besprechungsanfrage erstellt wird.
  
Versionen von Outlook seit Microsoft Office Outlook 2007 und auf CDO 1.2.1 basierende Lösungen, die das Outlook-oder Exchange Server-Kalender Aktualisierungstool ausgeführt haben, verwenden Sie diese Eigenschaft, um die Zeitzone für die Startzeit zu speichern. Die **dispidApptTZDefStartDisplay** -Eigenschaft zeigt den Termin oder die Besprechung in der ursprünglich geplanten Zeitzone an. Sie bestimmt, ob die Startzeit angepasst werden soll, wenn sich die Regeln der Zeitzone ändern. Wenn diese Eigenschaft nicht vorhanden ist, wird die aktuelle lokale Zeitzone angenommen. Diese Eigenschaft wird nur zu Anzeigezwecken verwendet und nicht in der Serienerweiterung verwendet. 
  
Ein Parser muss beim Lesen eines Datenstroms, der von dieser Eigenschaft abgerufen wurde, vorsichtig sein, oder wenn er **TZDEFINITION** in einem Stream für die Verpflichtung für eine binäre Eigenschaft wie **dispidApptTZDefStartDisplay**beibehält. Weitere Informationen finden Sie unter [Informationen zum Speichern von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu über](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)nehmen.
  
Diese Eigenschaft gibt Zeitzoneninformationen für die **dispidApptStartWhole** ([pidlidappointmentstartwhole (](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft an. Der Wert von **dispidApptTZDefStartDisplay** wird verwendet, um das Startdatum und die Uhrzeit für Anzeigezwecke von UTC in die lokale Zeitzone zu konvertieren. Für jedes **TZRULE** , das von dieser Eigenschaft angegeben wird, darf das TZRULE_FLAG_RECUR_CURRENT_TZREG-Flag nicht festgelegt werden. Wenn die **TZRULE** beispielsweise die effektive Regel ist, muss der Wert des Felds, **TZRULE** "0x0002" sein. Andernfalls muss es "0x0000" sein. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


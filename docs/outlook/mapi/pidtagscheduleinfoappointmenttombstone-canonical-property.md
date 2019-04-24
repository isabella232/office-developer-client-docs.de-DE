---
title: Kanonische Pidtagscheduleinfoappointmenttombstone (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321322"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Kanonische Pidtagscheduleinfoappointmenttombstone (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Datenblöcke, die Besprechungen darstellen, die abgelehnt wurden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Kennung:  <br/> |0x686A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Datenblöcke beginnen mit einer Kopfzeile von 32-Bit-Werten, die wie folgt definiert sind:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Bezeichner  <br/> |Dieses Feld muss der Wert 0xBEDEAFCD sein.  <br/> |
|Header size  <br/> |Dieses Feld muss den Wert 0x00000014 haben.  <br/> |
|Version  <br/> |Dieses Feld muss den Wert 3 aufweisen.  <br/> |
|RecordsCount  <br/> |Die Anzahl der nachfolgenden Datensätze.  <br/> |
|RecordsSize  <br/> |Dieses Feld muss den Wert 0x00000014 haben.  <br/> |
   
Die Kopfzeile wird gefolgt von **RecordsCount** -Einträgen mit 32-Bit-Werten wie folgt definiert: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|StartTime  <br/> |Die Startzeit des Besprechungs Objekts in Minuten seit Mitternacht, 1. Januar 1601, UTC.  <br/> |
|EndTime  <br/> |Die Endzeit des Besprechungs Objekts in Minuten seit Mitternacht, 1. Januar 1601, UTC.  <br/> |
|GlobalObjectIdSize  <br/> |Die Größe des GlobalObjectId-Felds in Byte.  <br/> |
|GlobalObjectId  <br/> |Der Wert der **LID_GLOBAL_OBJID** ([pidlidglobalobjectid (](pidlidglobalobjectid-canonical-property.md))-Eigenschaft der Besprechung, die dieser Datensatz darstellt.  <br/> |
|UserName  <br/> |Die ersten beiden Bytes sind die Länge der folgenden PT_STRING8-Zeichenfolge.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
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


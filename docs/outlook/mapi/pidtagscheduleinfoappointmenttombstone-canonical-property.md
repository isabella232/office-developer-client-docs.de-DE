---
title: PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)
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
ms.openlocfilehash: 37a6d101f6ee9c04236253e143aff3a51a9208d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795083"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Liste der Datenblöcke, die Besprechungen darstellen, die abgelehnt wurden.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Bezeichner:  <br/> |0x686A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht-Informationen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Datenblöcke beginnen mit einer Kopfzeile der 32-Bit-Werte als definiert:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Bezeichner  <br/> |Dieses Feld muss den Wert 0xBEDEAFCD sein.  <br/> |
|HeaderSize  <br/> |Dieses Feld muss den Wert 0x00000014 haben.  <br/> |
|Version  <br/> |Dieses Feld muss den Wert 3 haben.  <br/> |
|RecordsCount  <br/> |Die Anzahl der Datensätze, die folgen.  <br/> |
|RecordsSize  <br/> |Dieses Feld muss den Wert 0x00000014 haben.  <br/> |
   
Die Kopfzeile folgt **RecordsCount** Einträge der 32-Bit-Werte als definiert: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|StartTime  <br/> |Die Besprechung Objekt Startzeit in Minuten seit Mitternacht, 1. Januar 1601 UTC.  <br/> |
|EndTime  <br/> |Die Besprechung Objekt Endzeit in Minuten seit Mitternacht, 1. Januar 1601 UTC.  <br/> |
|GlobalObjectIdSize  <br/> |Die Größe des Feld GlobalObjectId in Bytes.  <br/> |
|GlobalObjectId  <br/> |Der Wert der Eigenschaft **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) der Besprechung dieser Datensatz darstellt.  <br/> |
|UserName  <br/> |Die ersten beiden Bytes sind die Länge der Zeichenfolge PT_STRING8, die bildet.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
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


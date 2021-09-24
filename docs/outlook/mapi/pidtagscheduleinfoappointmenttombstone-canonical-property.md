---
title: PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e89049186dfe32e6e76cd52324ef9aad37d8a82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550463"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste von Datenblöcken, die abgelehnte Besprechungen darstellen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Kennung:  <br/> |0x686A  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Datenblöcke beginnen mit einem Header mit 32-Bit-Werten, die wie folgt definiert sind:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Bezeichner  <br/> |Dieses Feld muss der Wert 0xBEDEAFCD sein.  <br/> |
|HeaderSize  <br/> |Dieses Feld muss den Wert 0x00000014 aufweisen.  <br/> |
|Version  <br/> |Dieses Feld muss den Wert 3 aufweisen.  <br/> |
|RecordsCount  <br/> |Die Anzahl der nachfolgenden Datensätze.  <br/> |
|RecordsSize  <br/> |Dieses Feld muss den Wert 0x00000014 aufweisen.  <br/> |
   
Auf die Kopfzeile folgen **RecordsCount-Einträge** mit 32-Bit-Werten, die wie folgt definiert sind: 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|StartTime  <br/> |Die Startzeit des Besprechungsobjekts in Minuten seit dem 1. Januar 1601(UTC) um Mitternacht.  <br/> |
|EndTime  <br/> |Die Endzeit des Besprechungsobjekts in Minuten seit dem 1. Januar 1601(UTC) um Mitternacht.  <br/> |
|GlobalObjectIdSize  <br/> |Die Größe des Felds GlobalObjectId in Bytes.  <br/> |
|GlobalObjectId  <br/> |Der Wert der **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) -Eigenschaft der Besprechung, die dieser Datensatz darstellt.  <br/> |
|UserName  <br/> |Die ersten beiden Bytes sind die Länge der folgenden zeichenfolge PT_STRING8.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
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


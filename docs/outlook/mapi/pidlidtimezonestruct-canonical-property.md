---
title: PidLidTimeZoneStruct (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346375"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>PidLidTimeZoneStruct (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem dauerhaften Format einer [TZREG-Struktur](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) zu ordnet, der die Zeitzone beschreibt, die für die Start- und Endzeit einer Termin- oder Besprechungsserie verwendet werden soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTimeZoneStruct  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x00008233  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Microsoft Office Outlook 2003, frühere Versionen von Outlook und Anwendungen, die auf CDO (Collaboration Data Objects) 1.21 basieren, deren Benutzer das von Outlook oder Exchange Server bereitgestellte Kalenderaktualisierungstool nicht ausgeführt haben, speichern die Start- und Endzeit eines Termins oder einer Besprechungsserie als relative Zeit, und speichern Sie die Zeitzone, in der die Termin- oder Besprechungsanfrage in **dispidTimeZoneStruct** erstellt wird. Dieses Schema ignoriert jedoch, dass sich im Laufe der Zeit Zeitzonenregeln ändern können, was zu einigen Terminen und Besprechungen führt, die Benutzer vor der Änderung der Regeln geplant haben und zu falschen Zeiten auftreten. Benutzer und Administratoren, die Windows Vista nicht ausgeführt werden oder die keine automatischen Updates aktiviert haben, sollten die kalenderbasierungstools verwenden, die von Outlook oder Exchange Server bereitgestellt werden, um die Uhrzeit solcher Termine und Besprechungsanfragen anzupassen. Weitere Informationen zu diesen Tools und APIs zum Neubasieren von Kalendern finden Sie unter Informationen zur programmgesteuerten Neubasierung von Kalendern für [Sommerzeit.](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Verwenden Sie das folgende Little-Endian-Format, wenn Sie einen Datenstrom aus **dispidTimeZoneStruct** oder die **TZREG-Struktur** in einem Datenstrom beibehalten, um einen Commit für die **binäre Eigenschaft dispidTimeZoneStruct** zu erstellen. 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Diese Eigenschaft wird für eine Serienserie festgelegt, um Zeitzoneninformationen anzugeben, und gibt an, wie Zeitfelder zwischen Ortszeit und koordinierter Weltzeit (Coordinated Universal Time, UTC) konvertiert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


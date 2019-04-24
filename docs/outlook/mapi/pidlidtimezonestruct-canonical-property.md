---
title: Kanonische Pidlidtimezonestruct (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346375"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Kanonische Pidlidtimezonestruct (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Stream, der dem permanenten Format einer [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) -Struktur zugeordnet wird, die die Zeitzone beschreibt, die für die Start-und Endzeit einer Termin-oder Besprechungsanfrage verwendet werden soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTimeZoneStruct  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x00008233  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Microsoft Office Outlook 2003, frühere Versionen von Outlook und Anwendungen, die auf Collaboration Data Objects (CDO) 1,21, deren Benutzer das von Outlook oder Exchange Server bereitgestellte Kalender Aktualisierungstool nicht ausgeführt haben, speichern die Startzeit und die Endzeit eines wiederkehrende Termin-oder Besprechungsanfrage als relative Zeit, und speichern Sie die Zeitzone, in der der Termin oder die Besprechungsanfrage in **dispidTimeZoneStruct**erstellt wird. Dieses Schema ignoriert jedoch, dass Zeitzonenregeln im Laufe der Zeit geändert werden können, was zu einigen Terminen und Besprechungen führt, die Benutzer vor Änderung der Regeln geplant haben und zu falschen Zeiten stattfinden. Benutzer und Administratoren, die Windows Vista nicht ausführen oder keine automatischen Updates aktiviert haben, sollten die Kalender-Wiederverwendungs Tools von Outlook oder Exchange Server verwenden, um die Uhrzeit solcher Termine und Besprechungsanfragen anzupassen. Weitere Informationen zu diesen Kalender-rebase-Tools und-APIs, die Kalender rebasisisieren, finden Sie unter Informationen zum programmgesteuerten Kalender [für Sommerzeit](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Verwenden Sie das folgende Little-Endian-Format beim Analysieren eines Streams, der von **dispidTimeZoneStruct**abgerufen wurde, oder wenn Sie die **TZREG** -Struktur in einem Stream beibehalten, um einen Commit für die binäre **dispidTimeZoneStruct** -Eigenschaft auszuführen. 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Diese Eigenschaft wird für eine wiederkehrende Reihe festgelegt, um Zeitzoneninformationen anzugeben, und gibt an, wie Zeitfelder zwischen Ortszeit und koordinierter weltZeit (UTC) konvertiert werden.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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


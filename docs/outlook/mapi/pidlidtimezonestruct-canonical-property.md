---
title: Kanonische PidLidTimeZoneStruct-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b7d2e0b7487743edcab993a00607144c36327ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579355"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Kanonische PidLidTimeZoneStruct-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Datenstrom, der dem beibehaltenen Format einer [TZREG-Struktur](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) zugeordnet ist, die die Zeitzone beschreibt, die für die Start- und Endzeit einer Terminserie oder Besprechungsanfrage verwendet werden soll. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTimeZoneStruct  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008233  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Microsoft Office Outlook 2003, frühere Versionen von Outlook und Anwendungen, die auf CDO 1.21 (Collaboration Data Objects) basieren, deren Benutzer das kalenderaktualisierungstool nicht ausgeführt haben, das von Outlook bereitgestellt wird, oder Exchange Server die Start- und Endzeit einer Terminserie oder Besprechungsanfrage als relative Zeit und St. ore the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**. Dieses Schema ignoriert jedoch, dass sich Zeitzonenregeln im Laufe der Zeit ändern können, was zu einigen Terminen und Besprechungen führt, die Benutzer vor der Änderung der Regeln geplant haben und zu falschen Zeiten auftreten. Benutzer und Administratoren, die nicht Windows Vista ausführen oder keine automatischen Updates aktiviert haben, sollten die kalenderbasierten Tools verwenden, die von Outlook oder Exchange Server bereitgestellt werden, um die Uhrzeit solcher Termine und Besprechungsanfragen anzupassen. Weitere Informationen zu diesen Kalender-Tools und APIs, mit denen Kalender neu erstellt werden, finden Sie unter Informationen zum [programmgesteuerten Neubasieren von Kalendern für Sommerzeit.](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Verwenden Sie das folgende Little-Endian-Format beim Analysieren eines von **dispidTimeZoneStruct** abgerufenen Datenstroms oder beim Beibehalten der **TZREG-Struktur** in einem Stream, um einen Commit für die binäre **Eigenschaft dispidTimeZoneStruct** auszuführen. 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Diese Eigenschaft wird für eine Terminserie festgelegt, um Zeitzoneninformationen anzugeben, und gibt an, wie Zeitfelder zwischen Ortszeit und koordinierter Weltzeit (COORDINATED Universal Time, UTC) konvertiert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


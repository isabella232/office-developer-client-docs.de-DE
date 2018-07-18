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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1a96cdb3aed03b9621097f1ef858a09391c0693
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793869"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>PidLidTimeZoneStruct (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) ist die beschreibt die Zeitzone für die Start- und Endzeit Tageszeit in einer Terminserie für einen Termin oder eine Besprechungsanfrage verwendet werden soll. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTimeZoneStruct  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008233  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Microsoft Office Outlook 2003 der Start- und Endzeit der frühere Versionen von Outlook und Anwendungen, die Collaboration Data Objects (CDO) 1.21 basieren, dessen Benutzer das Tool Kalender Update von Outlook oder Exchange Server nicht ausgeführt haben, Speichern einer wiederkehrende Termin oder eine Besprechungsanfrage als relative Zeit, und speichern Sie die Zeitzone, in dem die Termin- oder Besprechungsanfragen in **DispidTimeZoneStruct**erstellt wird. Im Laufe der Zeit Zeitzonenregeln ändern können, was in einigen Termine und Besprechungen geplant wurden, bevor die Regeln geändert und falsche Zeiten auftreten, die Benutzer ignoriert dieses Schema jedoch. Verwenden den Kalender, Neuzuordnen von Tools, die von Outlook oder Exchange Server, um die Zeit solcher Termine und Besprechungsanfragen anzupassen bereitgestellt werden sollten Benutzern und Administratoren, die nicht mit Windows Vista oder besitzen keine automatische Updates aktiviert ist. Weitere Informationen zu diesen Kalender Basisadressen Tools und APIs, die einer Kalender, finden Sie unter [About Basisadressen Kalender für Sommerzeit programmgesteuert](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Verwenden Sie das folgende little-Endian-Format bei der Analyse eines Stream-Objekts abgerufen aus **DispidTimeZoneStruct**oder, wenn die **TZREG** -Struktur in einem Stream-Objekt gespeichert, an die binäre Eigenschaft **DispidTimeZoneStruct** übermittelt werden. 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Diese Eigenschaft ist für eine Terminserie festgelegt, Zeitzone Informationen an und gibt an, wie Uhrzeitfelder zwischen lokaler Zeit und koordinierter Weltzeit (UTC) zu konvertieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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


---
title: Kanonische pidlidappointmentstartwhole (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345374"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a>Kanonische pidlidappointmentstartwhole (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt das Datum und die Uhrzeit für den Beginn eines Termins dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptStartWhole  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x0000820D  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt das Startdatum und die Uhrzeit des Ereignisses an. Diese Eigenschaft muss sich in Coordinated Universal Time (UTC) befinden und kleiner sein als der Wert der **dispidApptEndWhole** ([pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft. Bei einer Terminserie ist diese Eigenschaft das Startdatum und die Uhrzeit der ersten Instanz entsprechend dem Serienmuster.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt eine Eigenschaftssatzes-Definition und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


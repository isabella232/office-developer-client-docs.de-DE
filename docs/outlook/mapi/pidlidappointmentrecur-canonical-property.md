---
title: PidLidAppointmentRecur (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eb481316d905e9b3c33b181600626e2b9d8bcf39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571297"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>PidLidAppointmentRecur (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Datums- und Uhrzeitangaben an, zu denen eine Serienserie mithilfe eines der Serienmuster und -bereiche auftritt, die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)angegeben sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptRecur  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008216  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt die Datums- und Uhrzeitangaben an, zu denen eine Serienserie auftritt, indem eines der Serienmuster und -bereiche verwendet wird, die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)beschrieben sind. Der Wert dieser Eigenschaft enthält auch Informationen zu geänderten und gelöschten Ausnahmen. Informationen wie Datumsangaben, Betreff, Speicherort und verschiedene andere Eigenschaften von Ausnahmen. Die binären Daten in dieser Eigenschaft für wiederkehrende Kalenderelemente werden als **AppointmentRecurrencePattern-Struktur** gespeichert. Diese Eigenschaft darf nicht für Kalenderelemente mit einer einzelnen Instanz vorhanden sein. 
  
Es gibt einige Einschränkungen für Serien:
  
- Mehrere Instanzen dürfen nicht am selben Tag beginnen.
    
- Vorkommen dürfen sich nicht überlappen. Insbesondere muss eine Ausnahme, die das Startdatum einer Instanz in der Terminserie ändert, an einem Datum auftreten, das nach dem Ende der vorherigen Instanz und dem Anfang der nächsten Instanz in der Terminserie liegt. Das gleiche gilt, wenn die vorherigen oder nächsten Instanzen in der Terminserie Ausnahmen sind.
    
Der Zeitplan einer Terminserie wird durch das Serienmuster und den Bereich bestimmt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für E-Mails und andere Objekterinnerungen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


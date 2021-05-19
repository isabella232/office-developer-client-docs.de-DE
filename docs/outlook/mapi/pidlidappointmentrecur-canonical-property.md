---
title: PidLidAppointmentRecur (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331780"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>PidLidAppointmentRecur (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Datums- und Zeitangaben an, zu denen eine Serienserie auftritt, indem eines der serienmäßigen Muster und Bereiche verwendet wird, die in [[MS-OXOCAL] angegeben sind.](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptRecur  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Lange ID (LID):  <br/> |0x00008216  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Datums- und Zeitangaben an, zu denen eine Serienserie auftritt, indem eines der Serienmuster und Bereiche verwendet wird, die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)detailliert angegeben sind. Der Wert dieser Eigenschaft enthält auch Informationen zu geänderten und gelöschten Ausnahmen. Informationen wie Datum, Betreff, Ort und mehrere andere Eigenschaften von Ausnahmen. Die Binärdaten in dieser Eigenschaft für wiederkehrende Kalenderelemente werden als **AppointmentRecurrencePattern-Struktur** gespeichert. Diese Eigenschaft darf in Kalenderelementen einer einzelnen Instanz nicht vorhanden sein. 
  
Es gibt einige Einschränkungen für Wiederholungen:
  
- Mehrere Instanzen dürfen nicht am gleichen Tag gestartet werden.
    
- Vorkommen dürfen nicht überlappen. Insbesondere muss eine Ausnahme, die das Startdatum einer Instanz in der Serienserie ändert, an einem Datum auftreten, das nach dem Ende der vorherigen Instanz und dem Beginn der nächsten Instanz in der Serienserie liegt. Dasselbe gilt, wenn die vorherigen oder nächsten Instanzen in der Serienserie Ausnahmen sind.
    
Der Zeitplan einer Serienserie wird durch das Serienmuster und den Bereich bestimmt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


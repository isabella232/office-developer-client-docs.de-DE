---
title: Kanonische Pidlidappointmentrecur (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331780"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Kanonische Pidlidappointmentrecur (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Datums-und Uhrzeitangaben an, in denen eine wiederkehrende Reihe mit einem der Serienmuster und-Bereiche auftritt, die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)angegeben sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptRecur  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x00008216  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Datums-und Uhrzeitangaben an, in denen eine wiederkehrende Reihe mit einem der Serienmuster und [-Bereiche in [MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)ausgeführt wird. Der Wert dieser Eigenschaft enthält auch Informationen zu geänderten und gelöschten Ausnahmen. Informationen wie Datumsangaben, Betreff, Ort und verschiedene andere Eigenschaften von Ausnahmen. Die Binärdaten in dieser Eigenschaft für wiederkehrende Kalenderelemente werden als **AppointmentRecurrencePattern** -Struktur gespeichert. Diese Eigenschaft darf für Kalenderelemente mit einfacher Instanz nicht vorhanden sein. 
  
Es gibt einige Einschränkungen bei Serien Wiederholungen:
  
- Mehrere Instanzen dürfen nicht am selben Tag beginnen.
    
- Vorkommen dürfen sich nicht überlappen. Insbesondere muss eine Ausnahme, die das Startdatum einer Instanz in der wiederkehrenden Reihe ändert, auf einem Datum auftreten, das sich nach dem Ende der vorherigen Instanz und dem Anfang der nächsten Instanz in der wiederkehrenden Reihe befindet. Das gleiche gilt, wenn die vorherigen oder nächsten Instanzen in der wiederkehrenden Reihe Ausnahmen sind.
    
Der Zeitplan einer wiederkehrenden Reihe wird anhand des Serienmusters und-Umfangs bestimmt.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


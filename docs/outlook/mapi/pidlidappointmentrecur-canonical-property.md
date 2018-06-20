---
title: Kanonische PidLidAppointmentRecur-Eigenschaft
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
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793389"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Kanonische PidLidAppointmentRecur-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt die Datums- und Zeitangaben, tritt eine Terminserie mithilfe einer Serienmuster und Bereiche, die in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)angegeben sind.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidApptRecur  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008216  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Datums- und Zeitangaben – Wenn eine Terminserie erfolgt über die Serienmuster und liegt im Bereich Details in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). Der Wert dieser Eigenschaft enthält auch Informationen zu geänderten und gelöschte Ausnahmen. Informationen wie Datumsangaben, Betreff, Ort und einige andere Eigenschaften von Ausnahmen. Die binären Daten in dieser Eigenschaft für wiederkehrende Kalenderelemente werden als die Struktur **AppointmentRecurrencePattern** gespeichert. Diese Eigenschaft muss in Kalenderelementen Einzelinstanz nicht vorhanden. 
  
Es gibt jedoch einige Einschränkungen auf Wiederholungen:
  
- Mehrere Instanzen darf nicht am gleichen Tag beginnen.
    
- Vorkommen dürfen nicht überlappen. Insbesondere muss eine Ausnahme, die das Startdatum einer Instanz in der Terminserie ändert auf ein Datum auftreten, das nach dem Ende der vorherigen Instanz und den Beginn des nächsten Vorkommen in der sich wiederholenden Reihe liegt. Die gleichen ist True, wenn die vorherigen oder nächsten Instanzen in der Terminserie Ausnahmen sind.
    
Der Zeitplan eines sich wiederholenden Reihe wird durch die Serienmuster und Bereich bestimmt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


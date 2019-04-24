---
title: Kanonische Pidtagscheduleinfoautoacceptappointments (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330093"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>Kanonische Pidtagscheduleinfoautoacceptappointments (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Client oder Server automatisch auf alle Besprechungsanfragen für den Teilnehmer oder die Ressource reagieren soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|Kennung:  <br/> |0x686D  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie Antworten, muss die Antwort akzeptiert werden, es sei denn, eine zusätzliche Einschränkung, die von der **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([Pidtagscheduleinfodisallowrecurringappts (](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) oder PR_SCHDINFO_DISALLOW_ angegeben wird ** OVERLAPPING_APPTS** ([pidtagscheduleinfodisallowoverlappingappts (](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md))-Eigenschaften. Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass ein Client oder Server nicht automatisch Besprechungsanfragen annehmen darf. Dies ist keine erforderliche Eigenschaft.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


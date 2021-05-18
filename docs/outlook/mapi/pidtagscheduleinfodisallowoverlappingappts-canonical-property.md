---
title: PidTagScheduleInfoDisallowOverlappingAppts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330086"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a>PidTagScheduleInfoDisallowOverlappingAppts (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn überlappende Termine nicht zulässig sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS  <br/> |
|Kennung:  <br/> |0x686F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Frei/Gebucht  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur dann sinnvoll, wenn der Wert **der PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) -Eigenschaft TRUE ist. Der Wert TRUE gibt an, dass ein Client oder Server instanzen ablehnen muss, die zuvor geplante Ereignisse überlappen, wenn sie automatisch auf Besprechungsanfragen reagieren. Der Wert FALSE oder das Fehlen dieser Eigenschaft gibt an, dass überlappende Instanzen akzeptiert werden müssen. Dies ist keine erforderliche Eigenschaft.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


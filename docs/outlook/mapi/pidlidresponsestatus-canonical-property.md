---
title: Kanonische Pidlidresponsestatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345759"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Kanonische Pidlidresponsestatus (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Antwortstatus eines Teilnehmers an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidResponseStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Deckel):  <br/> |0x00008218  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Antwortstatus muss einer der Werte in der folgenden Tabelle sein.
  
|**Antwortstatus**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Für dieses Objekt ist keine Antwort erforderlich. Dies gilt für Terminobjekte und Besprechungsantwort Objekte.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Diese Besprechung gehört zum Organisator.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage vorläufig akzeptiert hat.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Dieser Wert in der Besprechung t des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage akzeptiert hat.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage abgelehnt hat.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer noch nicht geantwortet hat. Dieser Wert befindet sich in der Besprechungs-, Besprechungs-und Besprechungs Abbruch.  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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


---
title: Kanonische PidLidResponseStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 62e25b6cb9635aa6598ff912f717ba27239fd3be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624779"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Kanonische PidLidResponseStatus-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Antwortstatus eines Teilnehmers an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidResponseStatus  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008218  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Antwortstatus muss einer der Werte in der folgenden Tabelle sein.
  
|**Antwortstatus**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Für dieses Objekt ist keine Antwort erforderlich. Dies ist bei Terminobjekten und Besprechungsantwortobjekten der Fall.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Diese Besprechung gehört dem Organisator.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage mit Vorbehalt angenommen hat.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt nicht an, dass der Teilnehmer die Besprechungsanfrage angenommen hat.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer die Besprechungsanfrage abgelehnt hat.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Dieser Wert in der Besprechung des Teilnehmers gibt an, dass der Teilnehmer noch nicht geantwortet hat. Dieser Wert hängt von der Besprechungsanfrage, der Besprechungsaktualisierung und dem Abbruch der Besprechung ab.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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


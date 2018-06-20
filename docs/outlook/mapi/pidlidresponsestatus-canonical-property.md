---
title: Kanonische PidLidResponseStatus-Eigenschaft
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
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793762"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Kanonische PidLidResponseStatus-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt den Antwortstatus eines Teilnehmers.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidResponseStatus  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008218  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Antwortstatus muss einen der Werte in der folgenden Tabelle.
  
|**Antwortstatus**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Keine Antwort ist erforderlich für dieses Objekt. Dies ist die Groß-/Kleinschreibung für Terminobjekte und Antwortobjekte meeting.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Diese Besprechung gehört zu organisieren.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Dieser Wert auf den Attendee-Besprechung gibt an, dass der Teilnehmer die Besprechungsanfrage mit Vorbehalt angenommen hat.  <br/> |
|respAccepted  <br/> |0 x 00000003  <br/> |Dieser Wert auf den Teilnehmer Besprechung t gibt an, dass der Teilnehmer die Besprechungsanfrage angenommen hat.  <br/> |
|respDeclined  <br/> |0 x 00000004  <br/> |Dieser Wert auf den Attendee-Besprechung gibt an, dass der Teilnehmer die Besprechungsanfrage wurde abgelehnt wurde.  <br/> |
|respNotResponded  <br/> |0 x 00000005  <br/> |Dieser Wert auf den Attendee-Besprechung gibt an, dass der Teilnehmer noch nicht geantwortet hat. Dieser Wert ist auf die Besprechungsanfrage, besprechungsaktualisierung und Besprechungsabsage.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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


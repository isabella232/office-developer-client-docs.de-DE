---
title: PidTagRecipientTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389890"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>PidTagRecipientTrackStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Status der Antwort vom Teilnehmer zurückgegeben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Kennung:  <br/> |0x5FFF  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Transport-Empfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn dieser Wert nicht festgelegt ist, muss angenommen werden RespNone werden. Anderenfalls müssen sie eine der folgenden sein:
  
|**Antwortstatus**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Keine Antwort ist erforderlich für dieses Objekt. Dies ist die Groß-/Kleinschreibung für Terminobjekte und Antwortobjekte meeting.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Dieser Wert auf den Teilnehmer Besprechung-Objekt gibt an, dass der Teilnehmer die Besprechung mit Vorbehalt angenommen hat Request-Objekt.  <br/> |
|respAccepted  <br/> |0 x 00000003  <br/> |Dieser Wert auf den Teilnehmer Besprechung-Objekt gibt an, dass der Teilnehmer die Besprechung angenommen hat Request-Objekt.  <br/> |
|respDeclined  <br/> |0 x 00000004  <br/> |Dieser Wert auf den Teilnehmer Besprechung-Objekt gibt an, dass der Teilnehmer die Besprechung abgelehnt wurde Request-Objekt.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


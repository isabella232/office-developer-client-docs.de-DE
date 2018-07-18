---
title: PidLidAppointmentColor (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793340"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>PidLidAppointmentColor (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt die Designfarbe zu verwenden, wenn im Kalender anzeigen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidApptColor  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Appointment  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008214  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Farbe zu verwenden, wenn im Kalender anzeigen. Ein Client oder Server sollte diesen Wert für die Abwärtskompatibilität mit älteren Clients festlegen. Sie können stattdessen im Kalender basierend auf dem Wert der Eigenschaft **Schlüsselwörter** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) als angegebenen in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)angezeigt. Bei Festlegung muss der Wert eine der folgenden sein:
  
|**Wert**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Keine  <br/> |
|0x00000001  <br/> |Red  <br/> |
|0x00000002  <br/> |Blau  <br/> |
|0 x 00000003  <br/> |Green  <br/> |
|0 x 00000004  <br/> |Grau  <br/> |
|0 x 00000005  <br/> |Orange  <br/> |
|0 x 00000006  <br/> |Cyan  <br/> |
|0 x 00000007  <br/> |Olive  <br/> |
|0 x 00000008  <br/> |Purple  <br/> |
|0x00000009  <br/> |Teal  <br/> |
|0x0000000A  <br/> |Yellow  <br/> |
   
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


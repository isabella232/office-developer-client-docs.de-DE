---
title: Kanonische PidLidAppointmentColor-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7efffac9dd3a0b4060cd7c2735f2590712ac6868
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600708"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Kanonische PidLidAppointmentColor-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Farbe an, die beim Anzeigen des Kalenders verwendet werden soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidApptColor  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008214  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kalender  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft gibt die Farbe an, die beim Anzeigen des Kalenders verwendet werden soll. Ein Client oder Server sollte diesen Wert für die Abwärtskompatibilität mit älteren Clients festlegen. Stattdessen kann der Kalender basierend auf dem Wert der **Eigenschaft Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) angezeigt werden, wie in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)angegeben. Bei Festlegung muss der Wert einer der folgenden Werte sein:
  
|**Wert**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Keines  <br/> |
|0x00000001  <br/> |Rot  <br/> |
|0x00000002  <br/> |Blau  <br/> |
|0x00000003  <br/> |Grün  <br/> |
|0x00000004  <br/> |Grau  <br/> |
|0x00000005  <br/> |Orange  <br/> |
|0x00000006  <br/> |Cyan  <br/> |
|0x00000007  <br/> |Olive  <br/> |
|0x00000008  <br/> |Purpur  <br/> |
|0x00000009  <br/> |Teal  <br/> |
|0x0000000A  <br/> |Gelb  <br/> |
   
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


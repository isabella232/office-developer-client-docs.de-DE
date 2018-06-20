---
title: Kanonische PidLidMeetingType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e61ce7798c9e41dbb707d0d5773b116f7cce02d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793662"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Kanonische PidLidMeetingType-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt den Typ des einer Besprechungsanfrage oder meeting-Update an.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidMeetingType  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Meeting  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00000026  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft muss auf einen der folgenden festgelegt werden:
  
|**Eigenschaft**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Keine Angabe.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Anfängliche Besprechungsanfrage.  <br/> |
|mtgFull  <br/> |0 x 00010000  <br/> |Vollständige Aktualisierung.  <br/> |
|mtgInfo  <br/> |0 x 00020000  <br/> |Informative Update.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Eine neuere Besprechungsanfrage oder die Besprechungsanfrage wurde nach diesem empfangen.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Dies ist für die Delegator Kopie bei einer Stellvertretung Handles bezüglich Besprechungen Objekte festgelegt.  <br/> |
   
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


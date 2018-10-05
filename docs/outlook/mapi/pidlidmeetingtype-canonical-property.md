---
title: PidLidMeetingType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399634"
---
# <a name="pidlidmeetingtype-canonical-property"></a>PidLidMeetingType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Typ des einer Besprechungsanfrage oder meeting-Update an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidMeetingType  <br/> |
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

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


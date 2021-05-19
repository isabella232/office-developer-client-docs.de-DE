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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331577"
---
# <a name="pidlidmeetingtype-canonical-property"></a>PidLidMeetingType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Typ der Besprechungsanfrage oder Besprechungsaktualisierung an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidMeetingType  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Lange ID (LID):  <br/> |0x00000026  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft muss auf eine der folgenden Werte festgelegt werden:
  
|**Eigenschaft**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Nicht angegeben.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Erste Besprechungsanfrage.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Vollständige Aktualisierung.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Informationsupdate.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Eine neuere Besprechungsanfrage oder Besprechungsaktualisierung wurde nach dieser empfangen.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Dies wird für die Kopie des Delegators festgelegt, wenn eine Stellvertretung besprechungsbezogene Objekte behandelt.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


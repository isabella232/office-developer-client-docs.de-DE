---
title: Kanonische PidLidMeetingType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24b6d94dbd068698914d8bbd96a7b23f7cb2ae65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555734"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Kanonische PidLidMeetingType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Typ der Besprechungsanfrage oder besprechungsaktualisierung an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidMeetingType  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000026  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Besprechungen  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert dieser Eigenschaft muss auf eine der folgenden Werte festgelegt werden:
  
|**Eigenschaft**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Unspecified.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Ursprüngliche Besprechungsanfrage.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Vollständige Aktualisierung.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Informationsaktualisierung.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Eine neuere Besprechungsanfrage oder besprechungsaktualisierung wurde nach dieser empfangen.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Dies wird für die Kopie des Stellvertreters festgelegt, wenn ein Stellvertreter Besprechungsobjekte verarbeitet.  <br/> |
   
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


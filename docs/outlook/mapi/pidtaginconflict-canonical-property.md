---
title: PidTagInConflict (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ecac5736c405f04a92e43230b42ddeeb648b14d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620198"
---
# <a name="pidtaginconflict-canonical-property"></a>PidTagInConflict (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn die Anlage ein alternatives Replikat darstellt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IN_CONFLICT  <br/> |
|Kennung:  <br/> |0x666C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Konflikthinweis  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der E-Mail-Client und der E-Mail-Server müssen eine Konfliktlösungsnachricht generieren, wenn während der Synchronisierung ein Konflikt mit der aktuellen Version einer Nachricht im Replikat erkannt wird. Es ist wichtig zu wissen, dass es möglich ist, dass die aktuelle Version der Nachricht im lokalen Replikat während des aktuellen Synchronisierungsvorgangs übertragen wurde. Dies geschieht, wenn der Konflikt bereits auf dem Server vorhanden ist, bevor eine der widersprüchlichen Nachrichten in das lokale Replikat heruntergeladen wurde. Eine Konfliktlösungsnachricht muss als unabhängige Replikate mit widersprüchlichen PCLs synchronisiert werden. Die Konfliktlösungsnachricht selbst darf nicht zwischen Client und Server synchronisiert werden. nur die unabhängigen Replikate sollten ausgetauscht werden. Der Synchronisierungspartner muss dann eine neue Nachricht generieren, die der Struktur der Konfliktnachricht entspricht. Daher ist es wichtig, dass Client und Server denselben Algorithmus verwenden, um das "Gewinnende"-Element zu erkennen. Die folgenden Regeln müssen angewendet werden, um den "Gewinnenden" zu erkennen:
  
1. Zeitpunkt der letzten Änderung.
    
2. Höhere CN-GUID (mit Speichervergleich), um die Bindung zu unterbrechen.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Nachrichtenobjektdaten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


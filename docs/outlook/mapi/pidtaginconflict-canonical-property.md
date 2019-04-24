---
title: Kanonische Pidtaginconflict (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358534"
---
# <a name="pidtaginconflict-canonical-property"></a>Kanonische Pidtaginconflict (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn die Anlage ein alternatives Replikat darstellt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IN_CONFLICT  <br/> |
|Kennung:  <br/> |0x666C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Konflikt Hinweis  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der e-Mail-Client und der Server müssen eine Konflikt Lösungs Meldung generieren, wenn ein Konflikt mit der aktuellen Version einer Nachricht im Replikat während der Synchronisierung ermittelt wird. Es ist wichtig zu wissen, dass es möglich ist, dass die aktuelle Version der Nachricht im lokalen Replikat während des aktuellen Synchronisierungsvorgangs übertragen wurde. Dies geschieht, wenn der Konflikt bereits auf dem Server vorhanden ist, bevor eine der Konflikt verursachenden Nachrichten in das lokale Replikat heruntergeladen wurde. Eine Nachricht zur Konfliktbehebung muss als unabhängige Replikate mit widersprüchlichen PCLs synchronisiert werden. Die Nachricht zur Konfliktlösung selbst darf nicht zwischen Client und Server synchronisiert werden. nur die unabhängigen Replikate sollten ausgetauscht werden. Der Synchronisierungspartner muss dann eine neue Nachricht generieren, die mit der Struktur der Konfliktmeldung übereinstimmt. Daher ist es wichtig, dass Client und Server den gleichen Algorithmus verwenden, um das Element "Winner" zu identifizieren. Die folgenden Regeln müssen angewendet werden, um den "Gewinner" zu erfassen:
  
1. Zeitpunkt der letzten Änderung.
    
2. Höhere CN-GUID (mit Arbeitsspeicher Vergleich), um Tie zu unterbrechen.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Behandelt das Synchronisieren von Messagingobjekt Daten zwischen einem Server und einem Client.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


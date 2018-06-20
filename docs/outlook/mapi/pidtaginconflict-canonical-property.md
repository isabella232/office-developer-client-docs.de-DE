---
title: Kanonische PidTagInConflict-Eigenschaft
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
ms.openlocfilehash: 573e0ba37d4117d85193933a3a5045b5060fbd3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794481"
---
# <a name="pidtaginconflict-canonical-property"></a>Kanonische PidTagInConflict-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält True, wenn die Anlage eine alternative Replikat darstellt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_IN_CONFLICT  <br/> |
|Bezeichner:  <br/> |0x666C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Conflict-Hinweis  <br/> |
   
## <a name="remarks"></a>Hinweise

Die e-Mail-Client und Server müssen eine Konflikt auflösen Nachricht generieren, wenn einen Konflikt mit der aktuellen Version einer Nachricht in das Replikat während der Synchronisierung zu erkennen. Es ist wichtig zu verstehen, dass es möglich ist, dass die aktuelle Version der Nachricht in dem lokalen Replikat während der aktuellen Synchronisierungsvorgang übermittelt wurde. Das passiert, wenn Sie der Konflikt bereits auf dem Server vorhanden ist, bevor in einer miteinander in Konflikt stehende auf dem lokalen Replikat heruntergeladen wurden. Ein Konflikt beheben, dass die Nachricht als unabhängiger Replikate mit miteinander in Konflikt stehende PCLs synchronisiert werden muss. Der Konflikt aufgelöst werden kann, dass die Nachricht selbst nicht zwischen Client und Server synchronisiert werden muss. nur die unabhängige Replikate sollte ausgetauscht werden. Der Synchronisierungspartner muss dann eine neue Nachricht generieren, die die Struktur der Konfliktnachricht entspricht. Aus diesem Grund ist es wichtig, dass Client und Server den gleichen Algorithmus verwenden, um das Element "Gewinner" zu erkennen. Die folgenden Regeln müssen angewendet werden, um zu ermitteln, den "Gewinner":
  
1. Zeitpunkt der letzten Änderung.
    
2. Höhere CN GUID (Verwendung von Arbeitsspeicher Compare) Tie unterbrochen.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


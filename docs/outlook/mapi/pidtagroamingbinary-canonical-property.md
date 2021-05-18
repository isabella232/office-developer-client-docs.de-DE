---
title: PidTagRoamingBinary (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359563"
---
# <a name="pidtagroamingbinary-canonical-property"></a>PidTagRoamingBinary (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Nachrichtendatenstrom, der einer Unterklasse derIPM.Config **uration-Klasse zugeordnet** ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|Kennung:  <br/> |0x7C09  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Konfiguration  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält den Datenstrom, der einer **IPM.Config-Nachricht zugeordnet** ist. Das Format des Datenstroms hängt von der Nachrichtenklasse ab. Beispielsweise wird eine Nachricht vom Klassentyp **IPM.Configuration. AutoComplete** würde als [AutoComplete Stream formatiert.](autocomplete-stream.md)
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


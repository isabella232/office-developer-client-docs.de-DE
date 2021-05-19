---
title: PidTagSelectable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359017"
---
# <a name="pidtagselectable-canonical-property"></a>PidTagSelectable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Eintrag in der einmal aufgeführten Tabelle ausgewählt werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SELECTABLE  <br/> |
|Kennung:  <br/> |0x3609  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuchcontainer  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird hauptsächlich für die visuelle Formatierung einer einmal verwendeten Tabelle verwendet. Vorlagen können durch Erstellen eines Eintrags, der die Überschrift für die Gruppe angibt, gruppieren. Durch Festlegen dieser Eigenschaft auf FALSE für die Überschrift wird sichergestellt, dass der Benutzer nur die tatsächlichen Vorlagen in der Gruppe und nicht diesen Überschrifteneintrag auswählen kann. 
  
Diese Eigenschaft gilt nur für eine Einmaltabelle und nicht für eine Adressbuchhierarchietabelle. 
  
MAPI ermöglicht es einem Adressbuchanbieter, Elemente auf zwei Arten visuell zu gruppieren. Zunächst können bestimmte Zeilen als Überschriften funktionieren, indem sie nicht ausgewählt werden können. Zweitens können die auswählbaren Elemente relativ zu ihren Überschriften mithilfe der **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) eingezogen werden. Diese Eigenschaft wird in einer solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste ausgewählt werden kann, um eine einmal verwendete Adresse zu erstellen. Wenn ein Client beispielsweise über mehrere Vorlagen zum Erstellen von Faxadressen verfügt, kann er diese wie folgt anzeigen: 
  
FAXvorlagen (Tiefe 0, nicht auswählbar)
  
 Lokal (Tiefe 1, auswählbar) 
  
 Long-Distance (Tiefe 1, auswählbar) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[PidTagFolderType (kanonische Eigenschaft)](pidtagfoldertype-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


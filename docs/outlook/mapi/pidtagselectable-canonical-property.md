---
title: Kanonische Pidtagselectable (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359017"
---
# <a name="pidtagselectable-canonical-property"></a>Kanonische Pidtagselectable (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Eintrag in der einmaligen Tabelle ausgewählt werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SELECTABLE  <br/> |
|Kennung:  <br/> |0x3609  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuchcontainer  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird hauptsächlich zur visuellen Formatierung einer einmaligen Tabelle verwendet. Vorlagen können gruppiert werden, indem ein Eintrag erstellt wird, der die Überschrift für die Gruppe angibt. Wenn Sie diese Eigenschaft für die Überschrift auf FALSE festlegen, wird sichergestellt, dass der Benutzer nur die tatsächlichen Vorlagen in der Gruppe und nicht diesen Überschriften Eintrag auswählen kann. 
  
Diese Eigenschaft gilt nur für eine einmalige Tabelle, nicht für eine Adressbuch-Hierarchietabelle. 
  
MAPI ermöglicht es einem Adressbuchanbieter, Elemente visuell auf zweierlei Weise zu gruppieren. Erstens können bestimmte Zeilen als Überschriften funktionieren, indem Sie nicht ausgewählt werden. Zweitens können die auswählbaren Elemente relativ zu ihren Überschriften eingerückt werden, indem Sie die **PR_DEPTH** ([pidtagdepth (](pidtagdepth-canonical-property.md))-Eigenschaft verwenden. Diese Eigenschaft wird in einer solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste ausgewählt werden kann, um eine einmalige Adresse zu erstellen. Wenn beispielsweise ein Client über mehrere Vorlagen zum Erstellen von Fax-Adressen verfügt, können diese wie folgt angezeigt werden: 
  
FAX-Vorlagen (Tiefe 0, nicht auswählbar)
  
 Local (Tiefe 1, auswählbar) 
  
 Long-Distance (Tiefe 1, auswählbar) 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Kanonische Pidtagfoldertype (-Eigenschaft](pidtagfoldertype-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


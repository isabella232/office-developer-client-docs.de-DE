---
title: PidTagSelectable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 74dfc2b0976f8a27f892caa45de05ff660c5b94b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624503"
---
# <a name="pidtagselectable-canonical-property"></a>PidTagSelectable (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Eintrag in der einmaligen Tabelle ausgewählt werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SELECTABLE  <br/> |
|Kennung:  <br/> |0x3609  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adressbuchcontainer  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in erster Linie für die visuelle Formatierung einer einmaligen Tabelle verwendet. Vorlagen können gruppiert werden, indem Sie einen Eintrag erstellen, der die Überschrift für die Gruppe angibt. Durch Festlegen dieser Eigenschaft auf FALSE für die Überschrift wird sichergestellt, dass der Benutzer nur die tatsächlichen Vorlagen in der Gruppe und nicht diesen Überschrifteneintrag auswählen kann. 
  
Diese Eigenschaft gilt nur für eine einmalige Tabelle, nicht für eine Adressbuchhierarchietabelle. 
  
MapI ermöglicht es einem Adressbuchanbieter, Elemente visuell auf zwei Arten zu gruppieren. Zunächst können bestimmte Zeilen als Überschriften fungieren, indem sie nicht ausgewählt werden können. Zweitens können die auswählbaren Elemente relativ zu ihren Überschriften mithilfe der **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) -Eigenschaft eingezogen werden. Diese Eigenschaft wird in einer solchen Gruppierung verwendet, um anzugeben, ob dieses Element aus einer Liste ausgewählt werden kann, um eine einmalige Adresse zu erstellen. Wenn ein Client beispielsweise über mehrere Vorlagen zum Erstellen von Faxadressen verfügt, kann er diese wie folgt anzeigen: 
  
FAX-Vorlagen (Tiefe 0, nicht auswählbar)
  
 Lokal (Tiefe 1, auswählbar) 
  
 Ferngespräche (Tiefe 1, auswählbar) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Kanonische PidTagFolderType-Eigenschaft](pidtagfoldertype-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: PropertyDefinition-Datenstromstruktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0bf7e617b58da57c784d43156b73be8c2d6d520
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609654"
---
# <a name="propertydefinition-stream-structure"></a>PropertyDefinition-Datenstromstruktur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine PropertyDefinition-Datenstromstruktur [](fielddefinition-stream-structure.md) ist ein Array von FieldDefinition-Datenstromstrukturen, die Definitionen für alle benutzerdefinierten Felder in einem Microsoft Outlook-Element und Datenbindungseinstellungen für einige integrierte Felder enthalten. 
  
Sie können die PropertyDefinition-Datenstromstruktur programmgesteuert bearbeiten. Sie können jedoch ähnliche Ergebnisse erzielen, indem Sie den Outlook Forms Designer und insbesondere das Dialogfeld **Eigenschaften** für ein datengebundenes Steuerelement verwenden. 
  
Felddefinitionen in einer PropertyDefinition-Datenstromstruktur können eines von zwei Formaten sein: PropDefV1 und PropDefV2. Outlook unterstützt sowohl PropDefV1 als auch PropDefV2. Alle Felddefinitionen in einer einzelnen PropertyDefinition-Datenstromstruktur müssen dasselbe Format aufweisen. Weitere Informationen zur Unterschiedlichkeit von PropDefV1 und PropDefV2 finden Sie unter [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
  
Datenelemente in diesem Datenstrom werden in kleiner endischer Bytereihenfolge gespeichert und folgen sich direkt in der unten angegebenen Reihenfolge.
  
- Version: WORD (2 Bytes), das Format der Felddefinitionen in der PropertyDefinition-Datenstromstruktur. In der folgenden Tabelle sind die möglichen Werte aufgelistet.
    
    |**Wert**|**Beschreibung**|
    |:-----|:-----|
    |0x0102  <br/> |Format ist PropDefV1.  <br/> |
    |0x0103  <br/> |Format ist PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Datenstrom. Dies ist die Anzahl der Arrayelemente im FieldDefinitions-Datenelement.
    
- FieldDefinitions: Ein Array von FieldDefinition-Datenstromstrukturen. Die Anzahl dieses Arrays entspricht dem FieldDefinitionCount-Datenelement.
    
## <a name="see-also"></a>Siehe auch

- [Outlook Elemente und Felder](outlook-items-and-fields.md)
- [Hinzufügen einer Definition für ein Neues User-Defined Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [PropertyDefinition-Streambeispiel](propertydefinition-stream-sample.md)
- [Stream-Strukturen](stream-structures.md)


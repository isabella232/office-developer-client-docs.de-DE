---
title: PropertyDefinition-Datenstrom Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438589"
---
# <a name="propertydefinition-stream-structure"></a>PropertyDefinition-Datenstrom Struktur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine PropertyDefinition-Datenstrom Struktur ist ein Array von [FieldDefinition streamstruktur](fielddefinition-stream-structure.md) -Datenstrom Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Microsoft Outlook-Element enthalten, sowie Datenbindungseinstellungen für einige integrierte Felder. 
  
Sie können die PropertyDefinition-Datenstrom Strukturprogramm gesteuert bearbeiten. Sie können jedoch ähnliche Ergebnisse erzielen, indem Sie den Outlook-Formular-Designer und insbesondere das Dialogfeld **Eigenschaften** für ein datengebundenes Steuerelement verwenden. 
  
Felddefinitionen in einer PropertyDefinition-Datenstrom Struktur können eines von zwei Formaten sein: PropDefV1 und PropDefV2. Outlook unterstützt sowohl PropDefV1 als auch PropDefV2. Alle Felddefinitionen in einer einzelnen PropertyDefinition-Datenstrom Struktur müssen das gleiche Format aufweisen. Weitere Informationen dazu, wie PropDefV1 und PropDefV2 unterschiedlich sind, finden Sie unter [FieldDefinition streamstruktur](fielddefinition-stream-structure.md)-streamstruktur.
  
Datenelemente in diesem Stream werden in der Little-Endian-Bytereihenfolge gespeichert, unmittelbar folgen einander in der angegebenen Reihenfolge.
  
- Version: WORD (2 Bytes), das Format der Felddefinitionen in der PropertyDefinition-Datenstrom Struktur. In der folgenden Tabelle sind die möglichen Werte aufgelistet.
    
    |**Wert**|**Beschreibung**|
    |:-----|:-----|
    |0x0102  <br/> |Format ist PropDefV1.  <br/> |
    |0x0103  <br/> |Format ist PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 Bytes), die Anzahl der Felddefinitionen in diesem Stream. Dies ist die Anzahl von Array-Elementen im FieldDefinitions-Datenelement.
    
- FieldDefinitions: ein Array von FieldDefinition streamstruktur-Stream-Strukturen. Die Anzahl dieses Arrays ist gleich dem FieldDefinitionCount-Datenelement.
    
## <a name="see-also"></a>Siehe auch

- [Outlook-Elemente und-Felder](outlook-items-and-fields.md)
- [Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [PropertyDefinition-Stream-Beispiel](propertydefinition-stream-sample.md)
- [Stream-Strukturen](stream-structures.md)


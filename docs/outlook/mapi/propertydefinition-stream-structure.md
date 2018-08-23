---
title: PropertyDefinition Stream-Struktur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b2de22eef455e59b7877524ce998e93a0a708e0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566656"
---
# <a name="propertydefinition-stream-structure"></a>PropertyDefinition Stream-Struktur

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine PropertyDefinition Stream-Struktur ist ein Array von [FieldDefinition](fielddefinition-stream-structure.md) Stream Strukturen, die Definitionen für alle benutzerdefinierten Felder in einem Microsoft Outlook-Element und Datenbindung Einstellungen für einige integrierte Felder enthalten. 
  
Sie können die PropertyDefinition Stream Struktur programmgesteuert bearbeiten. Jedoch können Sie ähnliche Ergebnisse erzielen, mithilfe des Outlook-Formular-Designers und insbesondere das Dialogfeld **Eigenschaften** für ein datengebundenes Steuerelement. 
  
Felddefinitionen in einer PropertyDefinition Stream-Struktur kann eine der folgenden beiden Formate: PropDefV1 und PropDefV2. Outlook unterstützt PropDefV1 und PropDefV2. Alle Felddefinitionen in einer einzelnen PropertyDefinition Stream Struktur müssen das gleiche Format aufweisen. Weitere Informationen dazu, wie PropDefV1 und PropDefV2 unterscheiden finden Sie unter [FieldDefinition Stream Struktur](fielddefinition-stream-structure.md).
  
Data-Elemente in diesem Datenstrom werden in little-Endian-Bytereihenfolge, unmittelbar miteinander in der angegebenen Reihenfolge gespeichert.
  
- Version: WORD (2 Bytes), das Format der Felddefinitionen in der PropertyDefinition stream Struktur. In der folgenden Tabelle sind die möglichen Werte.
    
    |**Wert**|**Beschreibung**|
    |:-----|:-----|
    |0x0102  <br/> |PropDefV1-Format vorliegt.  <br/> |
    |0x0103  <br/> |PropDefV2-Format vorliegt.  <br/> |
   
- FieldDefinitionCount: DWORD-Wert (4 Bytes), die Anzahl der Felddefinitionen in diesen Stream. Dies ist die Anzahl der Elemente in der FieldDefinitions Data-Element.
    
- FieldDefinitions: Ein Array von FieldDefinition Stream Strukturen. Die Anzahl der dieses Array ist gleich der FieldDefinitionCount Data-Element.
    
## <a name="see-also"></a>Siehe auch

- [Elemente und Felder in Outlook](outlook-items-and-fields.md)
- [Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Beispiel für PropertyDefinition-Stream](propertydefinition-stream-sample.md)
- [Streamstrukturen](stream-structures.md)


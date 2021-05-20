---
title: PropertyDefinition-Streamstruktur
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
# <a name="propertydefinition-stream-structure"></a>PropertyDefinition-Streamstruktur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine PropertyDefinition-Streamstruktur ist [](fielddefinition-stream-structure.md) ein Array von FieldDefinition-Streamstrukturen, die Definitionen für alle benutzerdefinierten Felder in einem Microsoft Outlook-Element und Datenbindungseinstellungen für einige integrierte Felder enthalten. 
  
Sie können die PropertyDefinition-Streamstruktur programmgesteuert bearbeiten. Sie können jedoch ähnliche Ergebnisse erzielen, indem Sie den Outlook Forms Designer und insbesondere das Dialogfeld **Eigenschaften** für ein datengebundenes Steuerelement verwenden. 
  
Felddefinitionen in einer PropertyDefinition-Streamstruktur können eines von zwei Formaten sein: PropDefV1 und PropDefV2. Outlook unterstützt sowohl PropDefV1 als auch PropDefV2. Alle Felddefinitionen in einer einzelnen PropertyDefinition-Streamstruktur müssen das gleiche Format haben. Weitere Informationen dazu, wie sich PropDefV1 und PropDefV2 unterscheiden, finden Sie unter [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
  
Datenelemente in diesem Datenstrom werden in der Bytereihenfolge des Little-Endian-Elements gespeichert und folgen sofort in der unten angegebenen Reihenfolge aufeinander.
  
- Version: WORD (2 Byte), das Format der Felddefinitionen in der PropertyDefinition-Streamstruktur. In der folgenden Tabelle sind die möglichen Werte aufgelistet.
    
    |**Wert**|**Beschreibung**|
    |:-----|:-----|
    |0x0102  <br/> |Format ist PropDefV1.  <br/> |
    |0x0103  <br/> |Format ist PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 Byte), die Anzahl der Felddefinitionen in diesem Datenstrom. Dies ist die Anzahl der Arrayelemente im FieldDefinitions-Datenelement.
    
- FieldDefinitions: Ein Array von FieldDefinition-Streamstrukturen. Die Anzahl dieses Arrays entspricht dem FieldDefinitionCount-Datenelement.
    
## <a name="see-also"></a>Siehe auch

- [Outlook Elemente und Felder](outlook-items-and-fields.md)
- [Hinzufügen einer Definition für ein new User-Defined Field](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)
- [Streamstrukturen](stream-structures.md)


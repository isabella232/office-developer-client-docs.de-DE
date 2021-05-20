---
title: Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428165"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie ein benutzerdefiniertes Feld zu einem Microsoft Outlook hinzufügen, fügen Sie der entsprechenden [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md) eine Felddefinition hinzu. Verwenden Sie das folgende Verfahren, um einer PropertyDefinition-Streamstruktur eine neue Felddefinition hinzuzufügen. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu

1. Kopieren Sie die vorhandenen Felddefinitionen der PropertyDefinition-Streamstruktur in ein neues Felddefinitionsarray. 
    
2. Wenn sich vorhandene Felddefinitionen im PropDefV1-Format befinden, konvertieren Sie sie in das PropDefV2-Format. Weitere Informationen zu Felddefinitionsformaten finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) und [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
    
3. Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im PropDefV2-Format, und fügen Sie es dem Array hinzu.
    
4. Legen Sie das Version-Element der PropertyDefinition-Streamstruktur als 0x0103 fest, wenn das Version-Element nicht auf den Wert festgelegt wurde.
    
5. Erhöhen Sie das FieldDefinitionCount-Element um 1.
    
6. Store array als Wert des FieldDefinitions-Elements.
    
## <a name="see-also"></a>Siehe auch

- [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md)


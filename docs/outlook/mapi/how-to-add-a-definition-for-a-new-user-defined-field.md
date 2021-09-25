---
title: Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 40da92fd14036be5b0bdd22596a120bbb4c69b2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561719"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einem Microsoft Outlook-Element ein benutzerdefiniertes Feld hinzufügen, fügen [](propertydefinition-stream-structure.md) Sie der entsprechenden PropertyDefinition-Datenstromstruktur eine Felddefinition hinzu. Verwenden Sie das folgende Verfahren, um einer PropertyDefinition-Datenstromstruktur eine neue Felddefinition hinzuzufügen. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu

1. Kopieren Sie die vorhandenen Felddefinitionen der PropertyDefinition-Datenstromstruktur in ein neues Felddefinitionsarray. 
    
2. Wenn vorhandene Felddefinitionen im PropDefV1-Format vorliegen, konvertieren Sie sie in das PropDefV2-Format. Weitere Informationen zu Felddefinitionsformaten finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) und [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).
    
3. Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im PropDefV2-Format, und fügen Sie es dem Array hinzu.
    
4. Legen Sie das Version-Element der PropertyDefinition-Datenstromstruktur als 0x0103 fest, wenn das Version-Element nicht auf diesen Wert festgelegt wurde.
    
5. Erhöhen Sie das FieldDefinitionCount-Element um 1.
    
6. Store das Array als Wert des FieldDefinitions-Elements.
    
## <a name="see-also"></a>Siehe auch

- [PropertyDefinition-Datenstromstruktur](propertydefinition-stream-structure.md)


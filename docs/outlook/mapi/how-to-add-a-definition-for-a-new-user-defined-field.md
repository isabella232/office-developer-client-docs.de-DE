---
title: Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299069"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einem Microsoft Outlook-Element ein benutzerdefiniertes Feld hinzufügen, fügen Sie der entsprechenden [PropertyDefinition](propertydefinition-stream-structure.md) -Datenstrom Struktur eine Felddefinition hinzu. Verwenden Sie das folgende Verfahren, um einer PropertyDefinition-Datenstrom Struktur eine neue Felddefinition hinzuzufügen. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu

1. Kopieren Sie die vorhandenen Felddefinitionen der PropertyDefinition-Datenstrom Struktur in ein neues Feld Definitions Array. 
    
2. Wenn vorhandene Felddefinitionen im PropDefV1-Format vorliegen, konvertieren Sie Sie in das PropDefV2-Format. Weitere Informationen zu Feld Definitions Formaten finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) und [FieldDefinition streamstruktur Stream Structure](fielddefinition-stream-structure.md).
    
3. Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im PropDefV2-Format, und fügen Sie Sie dem Array hinzu.
    
4. Legen Sie das Version-Element der PropertyDefinition-Datenstrom Struktur als 0x0103 fest, wenn das Version-Element nicht auf diesen Wert festgelegt wurde.
    
5. Inkrementieren Sie das FieldDefinitionCount-Element um 1.
    
6. Speichern Sie das Array als Wert des FieldDefinitions-Elements.
    
## <a name="see-also"></a>Siehe auch

- [PropertyDefinition-Datenstrom Struktur](propertydefinition-stream-structure.md)


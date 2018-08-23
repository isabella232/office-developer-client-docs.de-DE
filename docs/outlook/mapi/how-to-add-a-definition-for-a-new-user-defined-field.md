---
title: Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592717"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie ein benutzerdefiniertes Feld mit einem Microsoft Outlook-Element hinzufügen, fügen Sie eine Definition für ein Feld in der entsprechenden [PropertyDefinition](propertydefinition-stream-structure.md) Stream-Struktur. Verwenden Sie das folgende Verfahren so eine PropertyDefinition Stream-Struktur einer neuen Definition für ein Feld hinzu. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu

1. Kopieren Sie die vorhandenen Felddefinitionen der Struktur PropertyDefinition Stream in ein neues Feld Definitionen Array. 
    
2. Wenn alle vorhandenen Felddefinitionen im Format PropDefV1 sind, konvertieren Sie sie in das PropDefV2-Format. Weitere Informationen zu Feldformate Definition finden Sie unter [PropertyDefinition Stream](propertydefinition-stream-structure.md) auch [FieldDefinition Stream Struktur](fielddefinition-stream-structure.md).
    
3. Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im Format PropDefV2 und fügen Sie es in das Array.
    
4. Legen Sie das Version-Element der Struktur Stream PropertyDefinition als 0x0103, wenn das Version-Element mit diesem Wert nicht festgelegt wurde.
    
5. Das Element FieldDefinitionCount um 1 erhöht.
    
6. Speichern Sie das Array als Wert des FieldDefinitions-Elements.
    
## <a name="see-also"></a>Siehe auch

- [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md)


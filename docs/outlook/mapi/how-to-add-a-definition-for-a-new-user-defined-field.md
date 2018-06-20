---
title: Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791834"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu
 
**Betrifft**: Outlook 
  
Wenn Sie ein benutzerdefiniertes Feld mit einem Microsoft Outlook-Element hinzufügen, fügen Sie eine Definition für ein Feld in der entsprechenden [PropertyDefinition](propertydefinition-stream-structure.md) Stream-Struktur. Verwenden Sie das folgende Verfahren so eine PropertyDefinition Stream-Struktur einer neuen Definition für ein Feld hinzu. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu

1. Kopieren Sie die vorhandenen Felddefinitionen der Struktur PropertyDefinition Stream in ein neues Feld Definitionen Array. 
    
2. Wenn alle vorhandenen Felddefinitionen im Format PropDefV1 sind, konvertieren Sie sie in das PropDefV2-Format. Weitere Informationen zu Feldformate Definition finden Sie unter [PropertyDefinition Stream](propertydefinition-stream-structure.md) auch [FieldDefinition Stream Struktur](fielddefinition-stream-structure.md).
    
3. Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im Format PropDefV2 und fügen Sie es in das Array.
    
4. Legen Sie das Version-Element der Struktur Stream PropertyDefinition als 0x0103, wenn das Version-Element mit diesem Wert nicht festgelegt wurde.
    
5. Das Element FieldDefinitionCount um 1 erhöht.
    
6. Speichern Sie das Array als Wert des FieldDefinitions-Elements.
    
## <a name="see-also"></a>Siehe auch

- [PropertyDefinition Stream-Struktur](propertydefinition-stream-structure.md)


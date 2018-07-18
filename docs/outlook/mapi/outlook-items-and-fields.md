---
title: Elemente und Felder in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793329"
---
# <a name="outlook-items-and-fields"></a>Elemente und Felder in Outlook

  
  
**Betrifft**: Outlook 
  
Microsoft Outlook bietet Elementtypen, die speziell auf ihre Funktionalität (beispielsweise e-Mail-Elementen, Termine, Kontakte, Aufgaben und Notizen) sind. Outlook bietet Standardfelder für jede Art von Element als integrierte Felder bezeichnet. Outlook kann der Benutzer zum Erstellen von benutzerdefinierter Feldern, als benutzerdefinierte Felder bezeichnet. Jedes Feld ist einen Datentyp und einen Wert zugeordnet. Beispiele für Datentypen sind **Währung**, **Datum/Uhrzeit**, **Dauer**, **ganze Zahl**, **Schlüsselwörter**und **Text**. Benutzer können benutzerdefinierte Felder im Formular-Designer in Outlook mit definieren.
  
Auf Ebene der Programmierbarkeit wird jedes Element durch ein [IMessage](imessageimapiprop.md) -Objekt dargestellt. Jedes benutzerdefinierte Feld ist eine Definition für ein Feld und einen Wert zugeordnet. 
  
### <a name="field-definition"></a>Definition für ein Feld

Eine Definition für ein Feld enthält den Namen, Datentyp und andere Informationen über das Feld. Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts. Die **PidLidPropertyDefinitionStream** -Eigenschaft enthält einen binären Datenstrom bekannt als [PropertyDefinition](propertydefinition-stream-structure.md) , die die Felddefinitionen enthält. Weitere Informationen zu Stream Strukturen Felddefinitionen finden Sie unter [Stream-Strukturen](stream-structures.md).
  
### <a name="field-value"></a>Feldwert

Jedes benutzerdefinierte Feld eines Elements ist einen Wert, der in einer entsprechenden benannten Eigenschaft gespeichert ist. Mit dem Namen der Eigenschaft in die PS_PUBLIC_STRINGS-Eigenschaft festgelegt ist und eine Unicode-Zeichenfolge als Eigenschaftenname hat. Der Datentyp der Eigenschaft entspricht dem Typ des Felds. Wenn die Eigenschaft nicht im **IMessage** -Objekt vorhanden ist, geht Outlook einen angemessene Standardwert für die Eigenschaft aus. Beispielsweise wird vorausgesetzt für einen Typ String Outlook eine leere Zeichenfolge, wenn die Eigenschaft nicht vorhanden ist. 
  
## <a name="see-also"></a>Siehe auch



[Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Beispiel für PropertyDefinition-Stream](propertydefinition-stream-sample.md)
  
[Streamstrukturen](stream-structures.md)
  
[PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md)
  
[FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)
  
[SkipBlock-Streamstruktur](skipblock-stream-structure.md)
  
[FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString-Streamstruktur](packedansistring-stream-structure.md)
  
[PackedUnicodeString-Streamstruktur](packedunicodestring-stream-structure.md)


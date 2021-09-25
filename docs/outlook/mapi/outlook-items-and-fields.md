---
title: Outlook Elemente und Felder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b33f42e4203afeaa5d2f14bc46c84e8db060c468
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584000"
---
# <a name="outlook-items-and-fields"></a>Outlook Elemente und Felder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook bietet Elementtypen, die auf ihre Funktionalität spezialisiert sind (z. B. E-Mail-Elemente, Termine, Kontakte, Aufgaben und Notizen). Outlook stellt Standardfelder für jeden Elementtyp bereit, die allgemein als integrierte Felder bezeichnet werden. Outlook ermöglicht Es Benutzern auch, benutzerdefinierte Felder zu erstellen, die häufig als benutzerdefinierte Felder bezeichnet werden. Jedes Feld ist einem Datentyp und einem Wert zugeordnet. Beispiele für Datentypen sind **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords** und **Text**. Benutzer können benutzerdefinierte Felder mithilfe des Formular-Designers in Outlook definieren.
  
Auf der Programmierebene wird jedes Element durch ein [IMessage-Objekt](imessageimapiprop.md) dargestellt. Jedes benutzerdefinierte Feld ist einer Felddefinition und einem Wert zugeordnet. 
  
### <a name="field-definition"></a>Felddefinition

Eine Felddefinition enthält den Namen, den Datentyp und andere Informationen zum Feld. Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) des entsprechenden **IMessage-Objekts.** Die **PidLidPropertyDefinitionStream-Eigenschaft** enthält einen binären Datenstrom namens [PropertyDefinition,](propertydefinition-stream-structure.md) der die Felddefinitionen enthält. Weitere Informationen zu Datenstromstrukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).
  
### <a name="field-value"></a>Feldwert

Jedes benutzerdefinierte Feld eines Elements hat einen Wert, der in einer entsprechenden benannten Eigenschaft gespeichert ist. Diese benannte Eigenschaft befindet sich im PS_PUBLIC_STRINGS Eigenschaftensatz und hat eine Unicode-Zeichenfolge als Eigenschaftennamen. Der Datentyp der Eigenschaft entspricht dem Feldtyp. Wenn die Eigenschaft im **IMessage-Objekt** nicht vorhanden ist, geht Outlook von einem angemessenen Standardwert für die Eigenschaft aus. Bei einem Zeichenfolgentyp nimmt Outlook beispielsweise eine leere Zeichenfolge an, wenn die Eigenschaft nicht vorhanden ist. 
  
## <a name="see-also"></a>Siehe auch



[Hinzufügen einer Definition für ein Neues User-Defined Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Streambeispiel](propertydefinition-stream-sample.md)
  
[Stream-Strukturen](stream-structures.md)
  
[PropertyDefinition-Datenstromstruktur](propertydefinition-stream-structure.md)
  
[FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)
  
[SkipBlock-Streamstruktur](skipblock-stream-structure.md)
  
[FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString-Datenstromstruktur](packedansistring-stream-structure.md)
  
[PackedUnicodeString-Datenstromstruktur](packedunicodestring-stream-structure.md)


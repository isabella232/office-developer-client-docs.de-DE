---
title: Outlook-Elemente und-Felder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348545"
---
# <a name="outlook-items-and-fields"></a>Outlook-Elemente und-Felder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook bietet Elementtypen, die sich auf ihre Funktionalität spezialisiert haben (beispielsweise e-Mail-Elemente, Termine, Kontakte, Aufgaben und Notizen). Outlook bietet Standardfelder für jeden Elementtyp, die gemeinhin als integrierte Felder bezeichnet werden. Outlook ermöglicht Benutzern auch das Erstellen benutzerdefinierter Felder, die gemeinhin als benutzerdefinierte Felder bezeichnet werden. Jedes Feld ist einem Datentyp und einem Wert zugeordnet. Beispiele für Datentypen sind **Currency**, **Date/Time**, **Duration**, **Integer**, **Schlüsselwörter**und **Text**. Benutzer können benutzerdefinierte Felder mithilfe des Formular-Designers in Outlook definieren.
  
Auf der Programmierebene wird jedes Element durch ein [IMessage](imessageimapiprop.md) -Objekt dargestellt. Jedes benutzerdefinierte Feld ist einer Felddefinition und einem Wert zugeordnet. 
  
### <a name="field-definition"></a>Feld Definition

Eine Felddefinition enthält den Namen, den Datentyp und weitere Informationen zum Feld. Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [pidlidpropertydefinitionstream (](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts. Die **pidlidpropertydefinitionstream (** -Eigenschaft enthält einen binären Datenstrom, der als [PropertyDefinition](propertydefinition-stream-structure.md) bekannt ist und die Felddefinitionen enthält. Weitere Informationen zu Stream-Strukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).
  
### <a name="field-value"></a>Feldwert

Jedes benutzerdefinierte Feld eines Elements hat einen Wert, der in einer entsprechenden benannten Eigenschaft gespeichert ist. Diese benannte Eigenschaft befindet sich im PS_PUBLIC_STRINGS-Eigenschaftensatz und verfügt über eine Unicode-Zeichenfolge als Eigenschaftennamen. Der Datentyp der Eigenschaft entspricht dem Typ des Felds. Wenn die Eigenschaft nicht im **IMessage** -Objekt vorhanden ist, übernimmt Outlook einen angemessenen Standardwert für die Eigenschaft. Bei einem String-Typ nimmt Outlook beispielsweise eine leere Zeichenfolge an, wenn die Eigenschaft nicht vorhanden ist. 
  
## <a name="see-also"></a>Siehe auch



[Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Stream-Beispiel](propertydefinition-stream-sample.md)
  
[Stream-Strukturen](stream-structures.md)
  
[PropertyDefinition-Datenstrom Struktur](propertydefinition-stream-structure.md)
  
[FieldDefinition streamstruktur-Datenstrom Struktur](fielddefinition-stream-structure.md)
  
[SkipBlock streamstruktur-Datenstrom Struktur](skipblock-stream-structure.md)
  
[Firstskipblockcontent streamstruktur-Datenstrom Struktur](firstskipblockcontent-stream-structure.md)
  
[Packedansistring streamstruktur-Datenstrom Struktur](packedansistring-stream-structure.md)
  
[Packedunicodestring streamstruktur-Datenstrom Struktur](packedunicodestring-stream-structure.md)


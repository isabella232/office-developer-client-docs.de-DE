---
title: Outlook Elemente und Felder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409118"
---
# <a name="outlook-items-and-fields"></a>Outlook Elemente und Felder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook bietet Elementtypen, die auf ihre Funktionalität spezialisiert sind (z. B. E-Mail-Elemente, Termine, Kontakte, Aufgaben und Notizen). Outlook standard fields for each type of item, allgemein als integrierte Felder bezeichnet. Outlook können Benutzer auch benutzerdefinierte Felder erstellen, die häufig als benutzerdefinierte Felder bezeichnet werden. Jedes Feld ist einem Datentyp und einem Wert zugeordnet. Beispiele für Datentypen sind Currency ,  **Date/Time**,  **Duration**, Integer , **Keywords** und **Text**. Benutzer können benutzerdefinierte Felder mithilfe des Formular-Designers in Outlook.
  
Auf der Programmierbarkeitsebene wird jedes Element durch ein [IMessage-Objekt](imessageimapiprop.md) dargestellt. Jedes benutzerdefinierte Feld ist einer Felddefinition und einem Wert zugeordnet. 
  
### <a name="field-definition"></a>Felddefinition

Eine Felddefinition enthält den Namen, den Datentyp und andere Informationen zu dem Feld. Für jedes Element speichert Outlook definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) des entsprechenden **IMessage-Objekts.** Die **PidLidPropertyDefinitionStream-Eigenschaft** enthält einen binären Datenstrom, [der als PropertyDefinition](propertydefinition-stream-structure.md) bezeichnet wird und die Felddefinitionen enthält. Weitere Informationen zu Streamstrukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).
  
### <a name="field-value"></a>Feldwert

Jedes benutzerdefinierte Feld eines Elements hat einen Wert, der in einer entsprechenden benannten Eigenschaft gespeichert ist. Diese benannte Eigenschaft befindet sich im PS_PUBLIC_STRINGS und hat eine Unicode-Zeichenzeichenfolge als Eigenschaftsname. Der Datentyp der Eigenschaft entspricht dem Typ des Felds. Wenn die Eigenschaft nicht im **IMessage-Objekt** vorhanden ist, wird Outlook einen angemessenen Standardwert für die Eigenschaft angenommen. Beispielsweise wird für einen Zeichenfolgentyp Outlook eine leere Zeichenfolge angenommen, wenn die Eigenschaft nicht vorhanden ist. 
  
## <a name="see-also"></a>Siehe auch



[Hinzufügen einer Definition für ein new User-Defined Field](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)
  
[Streamstrukturen](stream-structures.md)
  
[PropertyDefinition Stream Structure](propertydefinition-stream-structure.md)
  
[FieldDefinition Stream Structure](fielddefinition-stream-structure.md)
  
[SkipBlock Stream Structure](skipblock-stream-structure.md)
  
[FirstSkipBlockContent Stream Structure](firstskipblockcontent-stream-structure.md)
  
[PackedAnsiString-Streamstruktur](packedansistring-stream-structure.md)
  
[PackedUnicodeString-Datenstromstruktur](packedunicodestring-stream-structure.md)


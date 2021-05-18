---
title: Streamstrukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407823"
---
# <a name="stream-structures"></a>Streamstrukturen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook werden in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) gespeichert. Der Wert dieser Eigenschaft ist ein binärer Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen für integrierte Felder für das Outlook enthält. Dieser Abschnitt enthält Informationen zur Struktur des binären Datenstroms, die in den folgenden Datenstromstrukturen aufgeschlüsselt sind. 
  
> [!NOTE]
> Die Namen dieser Streamstrukturen (z. B. PropertyDefinition, FieldDefinition und SkipBlock) und deren Datenelemente sind technisch nicht Teil der Programmierschnittstelle der Messaging-API (MAPI) und werden hier nur zu Dokumentationszwecken der tatsächlichen Streamstrukturen bereitgestellt. Entwickler können diese Datenstromstrukturen und Datenelemente in ihren Anwendungen nach Wahl beschriften. 
  
- [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md)
    
- [FieldDefinition Stream Structure](fielddefinition-stream-structure.md)
    
- [SkipBlock Stream Structure](skipblock-stream-structure.md)
    
- [FirstSkipBlockContent Stream Structure](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString-Streamstruktur](packedansistring-stream-structure.md)
    
- [PackedUnicodeString-Datenstromstruktur](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein new User-Defined Field](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)


---
title: Stream-Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 249910bcf29ca532359331fa712e8c3e65fd4a0d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549903"
---
# <a name="stream-structures"></a>Stream-Strukturen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definitionen benutzerdefinierter Felder eines Microsoft Outlook Elements werden in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) gespeichert. Der Wert dieser Eigenschaft ist ein binärer Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen für integrierte Felder für das Outlook Element enthält. Dieser Abschnitt enthält Informationen zur Struktur des binären Datenstroms, die in den folgenden Datenstromstrukturen unterteilt sind. 
  
> [!NOTE]
> Die Namen dieser Datenstromstrukturen (z. B. PropertyDefinition, FieldDefinition und SkipBlock) und deren Datenelemente sind technisch nicht Teil der Programmierschnittstelle der Messaging-API (MAPI) und werden hier nur für Dokumentationszwecke der tatsächlichen Datenstromstrukturen bereitgestellt. Entwickler können diese Datenstromstrukturen und Datenelemente in ihren Anwendungen nach Bedarf bezeichnen. 
  
- [PropertyDefinition-Datenstromstruktur](propertydefinition-stream-structure.md)
    
- [FieldDefinition-Datenstromstruktur](fielddefinition-stream-structure.md)
    
- [SkipBlock-Streamstruktur](skipblock-stream-structure.md)
    
- [FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString-Datenstromstruktur](packedansistring-stream-structure.md)
    
- [PackedUnicodeString-Datenstromstruktur](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein Neues User-Defined Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Streambeispiel](propertydefinition-stream-sample.md)


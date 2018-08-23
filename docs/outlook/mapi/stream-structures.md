---
title: Streamstrukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581580"
---
# <a name="stream-structures"></a>Streamstrukturen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook-Elements werden in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft gespeichert. Der Wert dieser Eigenschaft ist einen binären Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindung Einstellungen für integrierte Felder sind für das Outlook-Element enthält. Dieser Abschnitt enthält Informationen zur Struktur der binären Stream-Objekts, in den folgenden Stream Strukturen aufgeschlüsselt an. 
  
> [!NOTE]
> Die Namen der diese Stream-Strukturen (beispielsweise PropertyDefinition FieldDefinition und SkipBlock) und ihre Datenelemente sind nicht technisch gesehen Teil der von der Messaging-API (MAPI)-Programmierschnittstelle und hier nur zu Dokumentationszwecken bereitgestellt werden die tatsächlichen Stream Strukturen Zwecke. Entwickler können diese Stream Strukturen und Daten der Elemente in ihren Anträgen bezeichnen, wie sie auswählen. 
  
- [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md)
    
- [FieldDefinition-Streamstruktur](fielddefinition-stream-structure.md)
    
- [SkipBlock-Streamstruktur](skipblock-stream-structure.md)
    
- [FirstSkipBlockContent-Streamstruktur](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString-Streamstruktur](packedansistring-stream-structure.md)
    
- [PackedUnicodeString-Streamstruktur](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Siehe auch



[Elemente und Felder in Outlook](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Beispiel für PropertyDefinition-Stream](propertydefinition-stream-sample.md)


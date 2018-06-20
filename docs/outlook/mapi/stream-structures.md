---
title: Stream-Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795644"
---
# <a name="stream-structures"></a>Stream-Strukturen

  
  
**Betrifft**: Outlook 
  
Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook-Elements werden in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft gespeichert. Der Wert dieser Eigenschaft ist einen binären Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindung Einstellungen für integrierte Felder sind für das Outlook-Element enthält. Dieser Abschnitt enthält Informationen zur Struktur der binären Stream-Objekts, in den folgenden Stream Strukturen aufgeschlüsselt an. 
  
> [!NOTE]
> Die Namen der diese Stream-Strukturen (beispielsweise PropertyDefinition FieldDefinition und SkipBlock) und ihre Datenelemente sind nicht technisch gesehen Teil der von der Messaging-API (MAPI)-Programmierschnittstelle und hier nur zu Dokumentationszwecken bereitgestellt werden die tatsächlichen Stream Strukturen Zwecke. Entwickler können diese Stream Strukturen und Daten der Elemente in ihren Anträgen bezeichnen, wie sie auswählen. 
  
- [PropertyDefinition Stream-Struktur](propertydefinition-stream-structure.md)
    
- [FieldDefinition Stream-Struktur](fielddefinition-stream-structure.md)
    
- [SkipBlock Stream-Struktur](skipblock-stream-structure.md)
    
- [FirstSkipBlockContent Stream-Struktur](firstskipblockcontent-stream-structure.md)
    
- [PackedAnsiString Stream-Struktur](packedansistring-stream-structure.md)
    
- [PackedUnicodeString Stream-Struktur](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und Felder](outlook-items-and-fields.md)
  
[Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu.](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream-Beispiel](propertydefinition-stream-sample.md)


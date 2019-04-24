---
title: Stream-Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327440"
---
# <a name="stream-structures"></a>Stream-Strukturen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook-Elements werden in der [pidlidpropertydefinitionstream (](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft gespeichert. Der Wert dieser Eigenschaft ist ein binärer Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen für integrierte Felder für das Outlook-Element enthält. Dieser Abschnitt enthält Informationen zur Struktur des binären Streams, aufgeschlüsselt in den folgenden Stream-Strukturen. 
  
> [!NOTE]
> Die Namen dieser Stream-Strukturen (beispielsweise PropertyDefinition, FieldDefinition streamstruktur und SkipBlock streamstruktur) und ihre Datenelemente sind technisch nicht Teil der Programmierschnittstelle der Messaging-API (MAPI) und werden hier nur für die Dokumentation bereitgestellt. Zwecke der tatsächlichen Stream-Strukturen. Entwickler können diese Stream-Strukturen und Datenelemente in Ihren Anwendungen bei Ihrer Auswahl beschriften. 
  
- [PropertyDefinition-Datenstrom Struktur](propertydefinition-stream-structure.md)
    
- [FieldDefinition streamstruktur-Datenstrom Struktur](fielddefinition-stream-structure.md)
    
- [SkipBlock streamstruktur-Datenstrom Struktur](skipblock-stream-structure.md)
    
- [Firstskipblockcontent streamstruktur-Datenstrom Struktur](firstskipblockcontent-stream-structure.md)
    
- [Packedansistring streamstruktur-Datenstrom Struktur](packedansistring-stream-structure.md)
    
- [Packedunicodestring streamstruktur-Datenstrom Struktur](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und-Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Stream-Beispiel](propertydefinition-stream-sample.md)


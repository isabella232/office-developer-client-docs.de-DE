---
title: Kanonische Pidtaguserfields (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360739"
---
# <a name="pidtaguserfields-canonical-property"></a>Kanonische Pidtaguserfields (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen, den Datentyp und andere Informationen zu einem benutzerdefinierten Feld.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_USERFIELDS  <br/> |
|Kennung:  <br/> |0x36E3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [pidlidpropertydefinitionstream (](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts. Die **pidlidpropertydefinitionstream (** -Eigenschaft enthält einen binären Datenstrom, der als [PropertyDefinition](propertydefinition-stream-structure.md)bekannt ist und die Felddefinitionen enthält. Weitere Informationen zu Stream-Strukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).
  
Für jeden Ordner speichert Outlook die Definitionen aller benutzerdefinierten Felder in diesem Ordner in der **pidtaguserfields (** -Eigenschaft einer zugeordneten Nachricht der nachrichtenklasse IPC.ms. REN. USERFIELDS-jeder Ordner, der davon ausgeht, dass er in der Tabelle mit den zugeordneten Inhalten nicht mehr als eine Nachricht dieser Klasse enthält. 
  
> [!NOTE]
> Die Gruppe von benutzerdefinierten Feldern in einem Ordner stimmt möglicherweise nicht unbedingt mit den Sätzen von benutzerdefinierten Feldern in den einzelnen Elementen überein. 
  
Die Gruppe von benutzerdefinierten Feldern in einem Ordner wird an verschiedenen Stellen in der Outlook-Benutzeroberfläche angezeigt, beispielsweise in der Feldauswahl des Ordners. Die **pidtaguserfields (** -Eigenschaft der Nachricht enthält einen binären Stream **Beispiel für folderuserfields**, der die Ordner Felddefinitionen enthält. Weitere Informationen zu Stream-Strukturen für Ordner Felddefinitionen finden Sie unter [Folder Fields Stream Structures](folder-fields-stream-structures.md) und The [Beispiel für folderuserfields Stream Sample](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Abschnittsüberschrift

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und-Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Stream-Beispiel](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidTagUserFields (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2b06d1e4144335a483a08feedd75210f40f3823
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591353"
---
# <a name="pidtaguserfields-canonical-property"></a>PidTagUserFields (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen, den Datentyp und andere Informationen zu einem benutzerdefinierten Feld.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_USERFIELDS  <br/> |
|Kennung:  <br/> |0x36E3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) des entsprechenden **IMessage-Objekts.** Die **PidLidPropertyDefinitionStream-Eigenschaft** enthält einen binären Datenstrom, der als [PropertyDefinition](propertydefinition-stream-structure.md)bezeichnet wird und die Felddefinitionen enthält. Weitere Informationen zu Datenstromstrukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).
  
Für jeden Ordner speichert Outlook die Definitionen aller benutzerdefinierten Felder in diesem Ordner in der **PidTagUserFields-Eigenschaft** einer zugeordneten Nachricht der Nachrichtenklasse IPC.MS. REN. USERFIELDS – jeder Ordner, in dem davon ausgegangen wird, dass er nicht mehr als eine Nachricht dieser Klasse in der zugehörigen Inhaltstabelle enthält. 
  
> [!NOTE]
> Der Satz benutzerdefinierter Felder in einem Ordner stimmt möglicherweise nicht unbedingt mit den Sätzen benutzerdefinierter Felder in jedem seiner Elemente überein. 
  
Der Satz benutzerdefinierter Felder in einem Ordner wird an verschiedenen Stellen in der Outlook Ui angezeigt, z. B. in der Feldauswahl des Ordners. Die **PidTagUserFields** -Eigenschaft der Nachricht enthält einen binären Datenstrom, **FolderUserFields**, der die Ordnerfelddefinitionen enthält. Weitere Informationen zu Datenstromstrukturen für Ordnerfelddefinitionen finden Sie unter [Folder Fields Stream Structures](folder-fields-stream-structures.md) und [folderUserFields Stream Sample](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Abschnittsüberschrift

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein Neues User-Defined Feld](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition-Streambeispiel](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


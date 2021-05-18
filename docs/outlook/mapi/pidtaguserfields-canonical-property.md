---
title: PidTagUserFields (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360739"
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
   
## <a name="remarks"></a>Hinweise

Für jedes Element speichert Outlook definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) des entsprechenden **IMessage-Objekts.** Die **PidLidPropertyDefinitionStream-Eigenschaft** enthält einen binären Datenstrom mit dem Namen [PropertyDefinition](propertydefinition-stream-structure.md), der die Felddefinitionen enthält. Weitere Informationen zu Streamstrukturen für Felddefinitionen finden Sie unter [Stream Structures](stream-structures.md).
  
Für jeden Ordner speichert Outlook die Definitionen aller benutzerdefinierten Felder in diesem Ordner in der **PidTagUserFields-Eigenschaft** einer zugeordneten Nachricht der Nachrichtenklasse IPC.MS. REN. USERFIELDS – Jeder Ordner, der davon ausgegangen wird, dass er nur eine Nachricht dieser Klasse in der zugehörigen Inhaltstabelle enthält. 
  
> [!NOTE]
> Der Satz von benutzerdefinierten Feldern in einem Ordner ist möglicherweise nicht unbedingt mit den Benutzerdefinierten Feldern in den einzelnen Elementen übereinstimmen. 
  
Der Satz von benutzerdefinierten Feldern in einem Ordner wird an verschiedenen Stellen in der benutzerdefinierten Outlook angezeigt, z. B. an der Feld-Auswahl des Ordners. Die **PidTagUserFields-Eigenschaft** der Nachricht enthält einen binären **Datenstrom, FolderUserFields**, der die Ordnerfelddefinitionen enthält. Weitere Informationen zu Streamstrukturen für Ordnerfelddefinitionen finden Sie unter [Folder Fields Stream Structures](folder-fields-stream-structures.md) und [folderUserFields Stream Sample](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Abschnittsüberschrift

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Outlook Elemente und Felder](outlook-items-and-fields.md)
  
[Hinzufügen einer Definition für ein new User-Defined Field](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


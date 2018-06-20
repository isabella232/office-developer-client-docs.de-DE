---
title: Kanonische PidTagUserFields-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795276"
---
# <a name="pidtaguserfields-canonical-property"></a>Kanonische PidTagUserFields-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält den Namen, Datentyp und andere Informationen zu einem benutzerdefinierten Feld.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_USERFIELDS  <br/> |
|Bezeichner:  <br/> |0x36E3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Ordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Für jedes Element speichert Outlook die Definitionen aller benutzerdefinierten Felder in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft des entsprechenden **IMessage** -Objekts. Die **PidLidPropertyDefinitionStream** -Eigenschaft enthält einen binären Datenstrom bekannt als [PropertyDefinition](propertydefinition-stream-structure.md), die die Felddefinitionen enthält. Weitere Informationen zu Stream Strukturen Felddefinitionen finden Sie unter [Stream-Strukturen](stream-structures.md).
  
Für jeden Ordner speichert Outlook die Definitionen aller benutzerdefinierten Felder in dem Ordner, in der **PidTagUserFields** -Eigenschaft einer zugeordneten Nachricht der Nachrichtenklasse IPC.MS. REN. BENUTZERFELDER - davon ausgegangen, dass jeder Ordner nicht mehr als eine Nachricht dieser Klasse in der Inhaltstabelle zugeordneten enthalten. 
  
> [!NOTE]
> Der Satz von benutzerdefinierten Feldern in einem Ordner möglicherweise nicht unbedingt die Sätze von benutzerdefinierten Feldern in den einzelnen Elemente überein. 
  
An verschiedenen Stellen in der Outlook-Benutzeroberfläche, wie des Ordners Feldauswahl wird der Satz von benutzerdefinierten Feldern in einem Ordner angezeigt. Die Nachricht **PidTagUserFields** -Eigenschaft enthält einen binären Datenstrom, **FolderUserFields**, die Felddefinitionen Ordner enthält. Weitere Informationen zu Stream Strukturen für Ordner Felddefinitionen finden Sie unter [Ordner Felder Stream Strukturen](folder-fields-stream-structures.md) und die [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Abschnittsüberschrift

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[Outlook-Elemente und Felder](outlook-items-and-fields.md)
  
[Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu.](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream-Beispiel](propertydefinition-stream-sample.md)
  
[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


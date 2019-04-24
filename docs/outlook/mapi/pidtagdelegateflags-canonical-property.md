---
title: Kanonische Pidtagdelegateflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359899"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Kanonische Pidtagdelegateflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob ein Delegat die privaten Nachrichtenobjekte des delegators anzeigen kann.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Kennung:  <br/> |0x686B  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenklassen definierte transmitable  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Jeder Eintrag dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden.
  
|**Wert**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Der Delegat sollte keine privaten Nachrichtenobjekte anzeigen dürfen.  <br/> |
|ShowPrivate  <br/> |1  <br/> |Der Stellvertreter sollte private Nachrichtenobjekte anzeigen dürfen.  <br/> |
   
Diese Eigenschaft muss im Delegate Information-Objekt festgelegt werden. Der Wert "ShowPrivate" gibt an, dass der delegator private Nachrichtenobjekte sichtbar machen möchte. Diese Einstellung gilt für alle Ordner, für die der Stellvertreter eine Rolle als Prüfer, Autor oder Editor aufweist.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: PidTagDelegateFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359899"
---
# <a name="pidtagdelegateflags-canonical-property"></a>PidTagDelegateFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob ein Stellvertreter die privaten Nachrichtenobjekte des Delegators anzeigen kann.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Kennung:  <br/> |0x686B  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Durch nachrichtenklassendefinierte übertragungsfähige Nachrichten  <br/> |
   
## <a name="remarks"></a>Hinweise

Jeder Eintrag dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden.
  
|**Wert**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Der Stellvertretung sollte das Anzeigen privater Nachrichtenobjekte nicht gestattet werden.  <br/> |
|ShowPrivate  <br/> |1  <br/> |Der Delegat sollte private Nachrichtenobjekte anzeigen dürfen.  <br/> |
   
Diese Eigenschaft muss im Stellvertretungsinformationsobjekt festgelegt werden. Der Wert von "ShowPrivate" gibt an, dass der Delegator private Nachrichtenobjekte sichtbar machen möchte. Diese Einstellung gilt für alle Ordner, für die der Stellvertretung eine Rolle als Bearbeiter, Autor oder Editor zufällt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


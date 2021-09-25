---
title: PidTagDelegateFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c8878175c5eff6ffebe32d1cda6baef7ab91c49a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579131"
---
# <a name="pidtagdelegateflags-canonical-property"></a>PidTagDelegateFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob ein Delegat die privaten Nachrichtenobjekte des Delegators anzeigen kann.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Kennung:  <br/> |0x686B  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Nachrichtenklassendefiniert datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Jeder Eintrag dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden.
  
|**Wert**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Der Delegat sollte keine privaten Nachrichtenobjekte anzeigen dürfen.  <br/> |
|ShowPrivate  <br/> |1  <br/> |Der Delegat sollte private Nachrichtenobjekte anzeigen dürfen.  <br/> |
   
Diese Eigenschaft muss im Delegatinformationsobjekt festgelegt werden. Der Wert von "ShowPrivate" gibt an, dass der Delegator private Nachrichtenobjekte sichtbar machen möchte. Diese Einstellung gilt für alle Ordner, für die der Delegat eine Rolle als Prüfer, Autor oder Editor hat.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden mit und Konfigurieren von Postfächern als Stellvertretungen und Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers handeln.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


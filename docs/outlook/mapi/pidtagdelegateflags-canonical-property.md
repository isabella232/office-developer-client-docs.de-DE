---
title: Kanonische PidTagDelegateFlags-Eigenschaft
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
ms.openlocfilehash: 160ddc53edf3d9681adf6f9d536a488c0c345a07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794288"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Kanonische PidTagDelegateFlags-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt an, ob eine Stellvertretung den Delegator privaten Message Objekte anzeigen kann.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Bezeichner:  <br/> |0x686B  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Nachricht-Klasse definiert Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>Hinweise

Jeder Eintrag in dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden.
  
|**Wert**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Die Stellvertretung sollte nicht möglich, zum Anzeigen von privaten Message-Objekten.  <br/> |
|ShowPrivate  <br/> |1  <br/> |Die Stellvertretung sollte zum Anzeigen von Objekten private Nachricht zugelassen werden.  <br/> |
   
Diese Eigenschaft muss im Delegaten Informationen-Objekt festgelegt werden. Der Wert der "ShowPrivate" gibt an, dass Stellvertreters private Nachrichtenobjekte sichtbar machen möchte. Diese Einstellung gilt für alle Ordner, für die die Stellvertretung die Rolle des Reviewer, Autor oder Editor verfügt.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


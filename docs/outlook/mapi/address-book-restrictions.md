---
title: Adressbucheinschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576512"
---
# <a name="address-book-restrictions"></a>Adressbucheinschränkungen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Von adressbuchanbietern implementierte sind zur Unterstützung von drei Arten von Einschränkungen für die Tabellen Inhalt, der ihre Container erforderlich:
  
- Mehrdeutiger Name eigenschaftseinschränkungen
    
- Wichtige eigenschaftseinschränkungen Instanz
    
- Als Präfix Display Name Content Einschränkungen
    
Mehrdeutiger Name Einschränkungen sind Suchkriterien in Eigenschaft mithilfe der **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaft Empfängernamen mit Einträgen in Address Book Containern übereinstimmen. Die Einschränkung der **PR_ANR** -Eigenschaft ist ein "am besten erraten" suchen, bei dem adressbuchanbietern implementierte übereinstimmende Eigenschaft auswählen können, die am besten für ihre Container. Beispielsweise kann eine Adressbuchanbieter die Einschränkung **PR_ANR** nach übereinstimmenden Empfängernamen anhand der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Eigenschaft jedes Container-Eintrags implementieren, während einen anderen Anbieter **PR_DISPLAY verwenden könnten Dann zur Name** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI empfiehlt, Implementierungen der Einschränkung **PR_ANR** ein Gleichgewicht zwischen eine angemessene Leistung und Benutzerzufriedenheit hergestellt werden. Bei der Adressbuch-Dienstanbieter die Einschränkung wieder in einem solchen implementiert Benutzerzufriedenheit gewährleistet eine Möglichkeit, die zu wenige oder zu viele Treffer gefunden werden. Einige adressbuchanbietern implementierte unterstützen, was als Name eines definierten oder selten, bekannt ist, die ist nicht in einem Dialogfeld anzeigbaren aber kann eine Einschränkung mehrdeutiger Name übereinstimmen. 
  
Eine typische Implementierung möglicherweise zum Analysieren der Anzeigename des Empfängers in Wörter, gleicht alle Einträge, die alle Wörter enthält. Aufmerksamkeit auf Details wie etwa Empfindlichkeit gegenüber Word Position, gibt an, ob nicht aufeinander folgende Wörter abgeglichen werden und welche Trennzeichen können variieren. Beispielsweise ist der Name aufgelöst werden "Bill L", würde eine typische **PR_ANR** Einschränkung die folgenden Einträge als Entsprechung aktivieren: 
  
- Frank Larson
    
- Bill Kelly
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Wichtige Einschränkungen Instanz oder Suchkriterien in Eigenschaft **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), werden in der Implementierung von Listenfeldern verwendet, die in Clientanwendungen für die Anzeige von MAPI-Tabellen verwendet werden. Einige Liste Feld Implementierungen zulassen, dass Benutzer mehrere treffen, einen Bildlauf nach oben oder nach unten und Zurücksetzen auf das erste Element ausgewählt. Um dieses Verhalten zu implementieren, rufen Clients [IMAPITable](imapitable-findrow.md), eine eigenschaftseinschränkung auf die **PR_INSTANCE_KEY** -Eigenschaft der-Methode übergeben. Von adressbuchanbietern implementierte sind erforderlich, um diese Einschränkung zu unterstützen. 
  
Ein weiteres Feature von Listenfeldern verwendet für die Anzeige der Tabelle ist die Möglichkeit zum Positionieren des Cursors basierend auf einem Satz von Anfangszeichen. Wie der Benutzer Präfixzeichen eingeben startet, verschiebt der Client den Cursor auf das erste Element, das mit diesen Zeichen beginnt. Clients implementieren dieses Feature mit einer Content Einschränkung basierend auf der **PR_DISPLAY_NAME** -Eigenschaft und die FL_PREFIX fuzzy-Ebene. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)


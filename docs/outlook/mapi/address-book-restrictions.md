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
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432800"
---
# <a name="address-book-restrictions"></a>Adressbucheinschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter müssen drei Arten von Einschränkungen für die Inhaltstabellen ihrer Container unterstützen:
  
- Einschränkungen für mehrdeutige Name-Eigenschaften
    
- Eigenschafteneinschränkungen für Instanzschlüssel
    
- Inhaltseinschränkungen für Den Anzeigenamen mit Präfix
    
Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers. Die  PR_ANR-Eigenschaftseinschränkung ist eine Art der Suche, bei der Adressbuchanbieter die passende Eigenschaft auswählen können, die für ihren Container am besten funktioniert. Beispielsweise kann ein Adressbuchanbieter die **PR_ANR-Einschränkung** implementieren, indem empfängernamen mit der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Eigenschaft jedes Containereintrags übereinstimmen, während ein anderer Anbieter **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) verwendet.
  
MAPI empfiehlt, dass implementierungen der **PR_ANR** ein Gleichgewicht zwischen ausreichender Leistung und Benutzerzufriedenheit finden. Die Benutzerzufriedenheit kann beeinträchtigt werden, wenn ein Adressbuchanbieter die Einschränkung so implementiert, dass zu wenige oder zu viele Übereinstimmungen gefunden werden. Einige Adressbuchanbieter unterstützen einen so bezeichneten oder allgemeinen Namen, der in einem Dialogfeld nicht angezeigt werden kann, aber einer mehrdeutigen Namenseinschränkung entsprechen kann. 
  
Eine typische Implementierung kann sein, den Anzeigenamen des Empfängers in Wörter zu analysieren, die mit jedem Eintrag übereinstimmen, der alle Wörter enthält. Achten Sie auf Details wie z. B. vertraulichkeit für die Wortposition, ob nicht übereinstimmende Wörter übereinstimmen und die Auswahl der Trennzeichen variieren kann. Wenn der zu auflösende Name beispielsweise "Bill L"  ist, würde eine typische PR_ANR die folgenden Einträge als übereinstimmend auswählen: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Instanzschlüsseleinschränkungen oder **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaftseinschränkungen werden bei der Implementierung von Listenfeldern verwendet, die in Clientanwendungen zum Anzeigen von #A0 verwendet werden. Bei einigen Listenfeldimplementierungen können Benutzer mehrere Auswahlen treffen, einen Bildlauf nach oben oder unten durchführen und zum ersten ausgewählten Element zurückkehren. Um dieses Verhalten zu implementieren, rufen Clients [IMAPITable::FindRow auf](imapitable-findrow.md)und übergeben eine Eigenschaftseinschränkung für die **PR_INSTANCE_KEY-Eigenschaft** an die -Methode. Adressbuchanbieter müssen diese Einschränkung unterstützen. 
  
Ein weiteres Feature von Listenfeldern, die für die Tabellenanzeige verwendet werden, ist die Möglichkeit, den Cursor basierend auf einer Reihe von Präfixzeichen zu positionieren. Wenn der Benutzer mit der Eingabe von Präfixzeichen beginnt, verschiebt der Client den Cursor zum ersten Element, das mit diesen Zeichen beginnt. Clients implementieren dieses Feature mit einer Inhaltseinschränkung, die auf der **PR_DISPLAY_NAME-Eigenschaft** und der FL_PREFIX Fuzzy-Ebene basiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)


---
title: Adressbucheinschränkungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: decd8a746db45f60c96b008665d503eac5e3ec4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564428"
---
# <a name="address-book-restrictions"></a>Adressbucheinschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter müssen drei Arten von Einschränkungen für die Inhaltsverzeichnisse ihrer Container unterstützen:
  
- Einschränkungen der Eigenschaft "Mehrdeutiger Name"
    
- Einschränkungen für Instanzenschlüsseleigenschaften
    
- Inhaltseinschränkungen für Präfixanzeigenamen
    
Mehrdeutige Namenseinschränkungen sind Eigenschaftseinschränkungen, die die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaft verwenden, um Empfängernamen mit Einträgen in Adressbuchcontainern zuzuordnen. Die **PR_ANR** Eigenschaftseinschränkung ist ein "Best Guess"-Suchtyp, bei dem Adressbuchanbieter die übereinstimmende Eigenschaft auswählen können, die für ihren Container am besten geeignet ist. Beispielsweise kann ein Adressbuchanbieter die **PR_ANR** Einschränkung implementieren, indem Empfängernamen mit der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) -Eigenschaft jedes Containereintrags verglichen werden, während ein anderer Anbieter **möglicherweise PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) verwendet.
  
Die MAPI empfiehlt, dass die Implementierung der **PR_ANR** Einschränkung ein Gleichgewicht zwischen einer angemessenen Leistung und der Benutzerzufriedenheit gewährleistet. Die Benutzerzufriedenheit kann beeinträchtigt werden, wenn ein Adressbuchanbieter die Einschränkung so implementiert, dass zu wenige oder zu viele Übereinstimmungen gefunden werden. Einige Adressbuchanbieter unterstützen einen so genannten distinguished- oder common-Namen, der nicht in einem Dialogfeld angezeigt werden kann, aber einer mehrdeutigen Namenseinschränkung entsprechen kann. 
  
Eine typische Implementierung kann das Analysieren des Anzeigenamens des Empfängers in Wörter sein, die mit jedem Eintrag übereinstimmen, der alle Wörter enthält. Achten Sie auf Details wie z. B. die Vertraulichkeit der Wortposition, darauf, ob nicht übereinstimmende Wörter gefunden werden, und die Auswahl der Trennzeichen kann variieren. Wenn beispielsweise der zu lösende Name "Bill L" lautet, würde eine typische **PR_ANR** Einschränkung die folgenden Einträge als übereinstimmend auswählen: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Instanzenschlüsseleinschränkungen oder **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaftseinschränkungen werden bei der Implementierung von Listenfeldern verwendet, die in Clientanwendungen zum Anzeigen von MAPI-Tabellen verwendet werden. Einige Listenfeldimplementierungen ermöglichen Es Benutzern, mehrere Auswahlen zu treffen, einen Bildlauf nach oben oder unten durchzuführen und zum ersten ausgewählten Element zurückzukehren. Um dieses Verhalten zu implementieren, rufen Clients [IMAPITable::FindRow](imapitable-findrow.md)auf und übergeben eine Eigenschaftseinschränkung für die **PR_INSTANCE_KEY-Eigenschaft** an die Methode. Adressbuchanbieter müssen diese Einschränkung unterstützen. 
  
Ein weiteres Feature von Listenfeldern, die für die Tabellenansicht verwendet werden, ist die Möglichkeit, den Cursor basierend auf einer Reihe von Präfixzeichen zu positionieren. Wenn der Benutzer mit der Eingabe von Präfixzeichen beginnt, verschiebt der Client den Cursor zum ersten Element, das mit diesen Zeichen beginnt. Clients implementieren dieses Feature mit einer Inhaltseinschränkung, die auf der **PR_DISPLAY_NAME-Eigenschaft** und der FL_PREFIX Fuzzy-Ebene basiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)


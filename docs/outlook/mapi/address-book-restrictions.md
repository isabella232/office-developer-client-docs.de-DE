---
title: Adressbuch Einschränkungen
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
# <a name="address-book-restrictions"></a>Adressbuch Einschränkungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter müssen drei Arten von Einschränkungen für die Inhaltstabellen ihrer Container unterstützen:
  
- Eigenschafteneinschränkungen für mehrdeutige Namen
    
- Eigenschafteneinschränkungen für Instanzenschlüssel
    
- Inhaltseinschränkungen für vordefinierte Anzeigename
    
Einschränkungen bei mehrdeutigen Namen sind Eigenschaftseinschränkungen mithilfe der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaft, um Empfängernamen mit Einträgen in Adressbuch Containern abzugleichen. Die **PR_ANR** -Eigenschaftseinschränkung ist ein "Best Guess"-Suchtyp, bei dem Adressbuchanbieter die passende Eigenschaft auswählen können, die für ihren Container am besten geeignet ist. Beispielsweise kann ein Adressbuchanbieter die **PR_ANR** -Einschränkung implementieren, indem Empfängernamen mit der **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))-Eigenschaft der einzelnen Container Einträge verglichen werden, während ein anderer Anbieter PR_DISPLAY verwenden kann. ** _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI empfiehlt, dass Implementierungen der **PR_ANR** -Einschränkung eine Balance zwischen adäquater Leistung und Benutzerzufriedenheit finden. Die Benutzerzufriedenheit kann beeinträchtigt werden, wenn ein Adressbuchanbieter die Einschränkung so implementiert, dass zu wenige oder zu viele Übereinstimmungen gefunden werden. Einige Adressbuchanbieter unterstützen den Namen Distinguished oder Common, der nicht in einem Dialogfeld angezeigt werden kann, jedoch mit einer Einschränkung für mehrdeutige Namen übereinstimmt. 
  
Eine typische Implementierung besteht darin, den Anzeigenamen des Empfängers in Wörter zu analysieren, die mit allen Wörtern übereinstimmen. Beachten Sie Details wie die Vertraulichkeit der Wortposition, ob nicht aufeinanderfolgende Wörter übereinstimmen, und die Auswahl von Trennzeichen kann variieren. Wenn beispielsweise der zu lösende Name "Bill L" lautet, würde eine typische **PR_ANR** -Einschränkung die folgenden Einträge als Abgleich auswählen: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Instanzenschlüssel Einschränkungen oder **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaftseinschränkungen werden bei der Implementierung von Listenfeldern verwendet, die in clientANWENDUNGEN zum Anzeigen von MAPI-Tabellen verwendet werden. In einigen Listenfeld Implementierungen können Benutzer mehrere Optionen auswählen, nach oben oder unten scrollen und zum ersten ausgewählten Element zurückkehren. Um dieses Verhalten zu implementieren, rufen die Clients [IMAPITable:: FindRow](imapitable-findrow.md)auf und übergeben eine Eigenschaftseinschränkung für die **PR_INSTANCE_KEY** -Eigenschaft an die Methode. Adressbuchanbieter sind zur Unterstützung dieser Einschränkung erforderlich. 
  
Ein weiteres Feature von Listenfeldern, die für die Tabellenanzeige verwendet werden, ist die Möglichkeit, den Cursor auf der Grundlage einer Reihe von Präfixzeichen zu positionieren. Wenn der Benutzer mit dem Eingeben von Präfixzeichen beginnt, verschiebt der Client den Cursor auf das erste Element, das mit diesen Zeichen beginnt. Clients implementieren dieses Feature mit einer Inhaltseinschränkung, die auf der **PR_DISPLAY_NAME** -Eigenschaft und der FL_PREFIX-Fuzzy-Ebene basiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)


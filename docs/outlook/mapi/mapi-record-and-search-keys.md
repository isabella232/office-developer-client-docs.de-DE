---
title: MAPI-Datensatz und Suchschlüssel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 25288eaf1bd58e786a9d9ade788e8acccbc07c76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579509"
---
# <a name="mapi-record-and-search-keys"></a>MAPI-Datensatz und Suchschlüssel

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Datensatzschlüssel und Suchschlüssel sind binäre Bezeichner, die vielen MAPI-Objekten zugewiesen sind. Im Gegensatz zum Eintragsbezeichner eines Objekts ist der Datensatz oder Suchschlüssel direkt vergleichbar und kann übertragen werden. 
  
## <a name="record-keys"></a>Datensatzschlüssel

Ein Datensatzschlüssel wird verwendet, um zwei Objekte zu vergleichen. Nachrichtenspeicher- und Adressbuchobjekte müssen Über Datensatzschlüssel verfügen, die in ihrer **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) -Eigenschaft gespeichert sind. Da ein Datensatzschlüssel ein Objekt und nicht seine Daten identifiziert, verfügt jede Instanz eines Objekts über einen eindeutigen Datensatzschlüssel. Der Bereich eines Datensatzschlüssels für Ordner und Nachrichten ist der Nachrichtenspeicher. Der Bereich für Adressbuchcontainer, Messagingbenutzer und Verteilerlisten ist der Satz von Containern auf oberster Ebene, die von der MAPI für die Verwendung im integrierten Adressbuch bereitgestellt werden.
  
Datensatzschlüssel können in einer anderen Ressource dupliziert werden. Beispielsweise können unterschiedliche Nachrichten in zwei verschiedenen Nachrichtenspeichern denselben Datensatzschlüssel aufweisen. Dies unterscheidet sich von langfristigen Eintragsbezeichnern. Da langfristige Eintragsbezeichner einen Verweis auf den Dienstanbieter enthalten, haben sie einen größeren Bereich. Der Datensatzschlüssel eines Nachrichtenspeichers ähnelt im Bereich einem langfristigen Eintragsbezeichner. Es sollte für alle Nachrichtenspeicheranbieter eindeutig sein. Um diese Eindeutigkeit zu gewährleisten, legen Nachrichtenspeicheranbieter in der Regel ihren Datensatzschlüssel auf einen Wert fest, der die Kombination aus ihrer **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) -Eigenschaft und einem Bezeichner darstellt, der für den Nachrichtenspeicher eindeutig ist.
  
## <a name="search-keys"></a>Suchschlüssel

Ein Suchschlüssel wird verwendet, um die Daten in zwei Objekten zu vergleichen. Der Suchschlüssel eines Objekts wird in seiner **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft gespeichert. Da ein Suchschlüssel die Daten eines Objekts und nicht das Objekt selbst darstellt, können zwei verschiedene Objekte mit denselben Daten denselben Suchschlüssel haben. Wenn z. B. ein Objekt kopiert wird, verfügen sowohl das ursprüngliche Objekt als auch seine Kopie über dieselben Daten und denselben Suchschlüssel.
  
Nachrichten- und Messagingbenutzer verfügen über Suchschlüssel. Der Suchschlüssel einer Nachricht ist ein eindeutiger Bezeichner der Nachrichtendaten. Nachrichtenspeicheranbieter stellen die **PR_SEARCH_KEY** Eigenschaft einer Nachricht zum Zeitpunkt der Nachrichtenerstellung bereit. Der Suchschlüssel eines Adressbucheintrags wird anhand seines Adresstyps (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) und der Adresse (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) berechnet. Wenn der Adressbucheintrag schreibbar ist, ist sein Suchschlüssel möglicherweise erst verfügbar, nachdem der Adresstyp und die Adresse mithilfe der [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) festgelegt wurden und der Eintrag mithilfe der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) gespeichert wurde. Wenn sich diese Adresseigenschaften ändern, kann der entsprechende Suchschlüssel nicht mit den neuen Werten synchronisiert werden, bis für die Änderungen ein Commit mit einem **SaveChanges-Aufruf** ausgeführt wurde. 
  
Der Wert des Datensatzschlüssels eines Objekts kann je nach Dienstanbieter mit dem Wert des Suchschlüssels übereinstimmen oder vom Wert des Suchschlüssels abweichen. Einige Dienstanbieter verwenden denselben Wert für den Suchschlüssel, den Datensatzschlüssel und den Eintragsbezeichner eines Objekts. Andere Dienstanbieter weisen eindeutige Werte für die Bezeichner der einzelnen Objekte zu. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)


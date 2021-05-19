---
title: MAPI-Eintrags- und Suchschlüssel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434564"
---
# <a name="mapi-record-and-search-keys"></a>MAPI-Eintrags- und Suchschlüssel

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Datensatzschlüssel und Suchschlüssel sind binäre Bezeichner, die vielen MAPI-Objekten zugewiesen sind. Im Gegensatz zum Eintragsbezeichner eines Objekts ist sein Datensatz oder Suchschlüssel direkt vergleichbar und kann auch übertragen werden. 
  
## <a name="record-keys"></a>Datensatzschlüssel

Zum Vergleichen von zwei Objekten wird ein Datensatzschlüssel verwendet. Nachrichtenspeicher- und Adressbuchobjekte müssen über Datensatzschlüssel verfügen, die in ihrer **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) -Eigenschaft gespeichert sind. Da ein Datensatzschlüssel ein Objekt und nicht seine Daten identifiziert, verfügt jede Instanz eines Objekts über einen eindeutigen Datensatzschlüssel. Der Bereich eines Datensatzschlüssels für Ordner und Nachrichten ist der Nachrichtenspeicher. Der Bereich für Adressbuchcontainer, Messagingbenutzer und Verteilerlisten ist der Satz von Containern auf oberster Ebene, die von MAPI zur Verwendung im integrierten Adressbuch bereitgestellt werden.
  
Datensatzschlüssel können in einer anderen Ressource dupliziert werden. Beispielsweise können unterschiedliche Nachrichten in zwei verschiedenen Nachrichtenspeichern denselben Datensatzschlüssel haben. Dies ist anders als bei langfristigen Eintragsbezeichnern. Da langfristige Eintragsbezeichner einen Verweis auf den Dienstanbieter enthalten, haben sie einen größeren Bereich. Der Datensatzschlüssel eines Nachrichtenspeichers ist im Bereich mit einer langfristigen Eintrags-ID vergleichbar. Sie sollte für alle Nachrichtenspeicheranbieter eindeutig sein. Um diese Eindeutigkeit sicherzustellen, legen Nachrichtenspeicheranbieter ihren Datensatzschlüssel in der Regel auf einen Wert fest, der die Kombination aus seiner **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))-Eigenschaft und einem bezeichner ist, der für den Nachrichtenspeicher eindeutig ist.
  
## <a name="search-keys"></a>Suchschlüssel

Ein Suchschlüssel wird verwendet, um die Daten in zwei Objekten zu vergleichen. Der Suchschlüssel eines Objekts wird in seiner **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) gespeichert. Da ein Suchschlüssel die Daten eines Objekts und nicht das Objekt selbst darstellt, können zwei verschiedene Objekte mit denselben Daten denselben Suchschlüssel haben. Wenn beispielsweise ein Objekt kopiert wird, verfügen sowohl das ursprüngliche Objekt als auch seine Kopie über dieselben Daten und denselben Suchschlüssel.
  
Nachrichten und Messagingbenutzer verfügen über Suchschlüssel. Der Suchschlüssel einer Nachricht ist ein eindeutiger Bezeichner der Nachrichtendaten. Nachrichtenspeicheranbieter bieten die **PR_SEARCH_KEY-Eigenschaft** einer Nachricht zum Zeitpunkt der Nachrichtenerstellung an. Der Suchschlüssel eines Adressbucheintrags wird anhand seines Adresstyps (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) und der Adresse (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) berechnet. Wenn der Adressbucheintrag schreibbar ist, steht der Suchschlüssel möglicherweise erst zur Verfügung, wenn der Adresstyp und die Adresse mithilfe der [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) festgelegt wurden und der Eintrag mithilfe der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) gespeichert wurde. Wenn sich diese Adresseigenschaften ändern, kann der entsprechende Suchschlüssel erst mit den neuen Werten synchronisiert werden, wenn die Änderungen mit einem **SaveChanges-Aufruf** vorgenommen wurden. 
  
Der Wert des Datensatzschlüssels eines Objekts kann je nach Dienstanbieter mit dem Wert des Suchschlüssels identisch oder unterschiedlich sein. Einige Dienstanbieter verwenden denselben Wert für den Suchschlüssel, den Datensatzschlüssel und die Eintrags-ID eines Objekts. Andere Dienstanbieter weisen eindeutige Werte für die Bezeichner der einzelnen Objekte zu. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)


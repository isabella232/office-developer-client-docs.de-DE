---
title: MAPI-Datensatz und Suche Schlüssel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4aa641ad0a41ff8015d2ece717d5a4cb3a7c4edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587313"
---
# <a name="mapi-record-and-search-keys"></a>MAPI-Datensatz und Suche Schlüssel

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aufzeichnen Tasten und die Suche Tasten sind binäre IDs, die viele MAPI-Objekten zugewiesen sind. Im Gegensatz zu Eintrags-ID für ein Objekt ist seine Datensatz oder in den Schlüssel direkt vergleichbare sowie Übertragungseinehit. 
  
## <a name="record-keys"></a>Aufzeichnen Schlüssel

Eine Taste Datensatz wird zum Vergleichen von zwei Objekte verwendet. Nachrichtenspeicher und Address Book-Objekten benötigen Datensatzschlüssel, die in der **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))-Eigenschaft gespeichert werden. Da ein Datensatzschlüssel ein Objekt und nicht auf seine Daten identifiziert, hat jede Instanz eines Objekts einen eindeutigen Datensatzes-Schlüssel an. Der Bereich eines Schlüssels Datensatz für Ordner und Nachrichten ist die Nachrichtenspeicher. Der Bereich für Address Book Container, messaging-Benutzern und Verteilerlisten ist der Satz der Container auf oberster Ebene für die Verwendung im integrierten Adressbuch von MAPI bereitgestellt.
  
Aufzeichnen Schlüssel können in eine andere Ressource dupliziert werden. Beispielsweise können verschiedene Nachrichten in zwei verschiedenen Nachrichtenspeicher den gleichen Datensatzschlüssel verfügen. Dies unterscheidet sich von langfristige-Eintragsbezeichner; Da langfristige-Eintragsbezeichner einen Verweis auf den Dienstanbieter enthalten, weisen sie einen größeren Bereich. Einen Nachrichtenspeicher aufzeichnen Schlüssel ist ähnlich wie im Bereich zu einer langfristige Eintrags-ID; Es sollte für alle Anbieter für Nachricht Store eindeutig sein. Um diese Eindeutigkeit sicherzustellen, festgelegt Nachricht-Anbieter in der Regel ihre Datensatzschlüssel auf einen Wert, der ist die Kombination von deren Eigenschaft **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) und einen Bezeichner, der mit dem Nachrichtenspeicher eindeutig ist.
  
## <a name="search-keys"></a>Search-Schlüssel

Ein Search-Schlüssel verwendet, die Daten in zwei Objekte verglichen werden soll. Ein Objekt Suche Schlüssel wird in der Eigenschaft **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) gespeichert. Da ein Search-Schlüssel Daten eines Objekts und nicht das Objekt selbst darstellt, können zwei verschiedene Objekte mit denselben Daten den gleichen Suche Schlüssel verfügen. Wenn ein Objekt kopiert werden, haben beispielsweise das ursprüngliche-Objekt und seine Kopie dieselben Daten und die gleiche suchen-Taste.
  
Nachrichten und messaging-Benutzern besitzen Suchschlüssel. Die suchen-Taste einer Nachricht ist ein eindeutiger Bezeichner, der die Daten der Nachricht. Nachricht Anbieter sind eine Nachricht **PR_SEARCH_KEY** -Eigenschaft zum Zeitpunkt der Erstellung Nachricht. Die suchen-Taste eines Adresseintrags Adressbuch wird von der Adresstyp (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) und Adresse (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) berechnet. Wenn der Adresseintrag Adressbuch nicht schreibgeschützt ist, seinen Search-Schlüssel möglicherweise nicht verfügbar, bis der Adresstyp und Adresse mithilfe der [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode festgelegt haben und der Eintrag wurde mithilfe der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode gespeichert. Wenn diese Adresseigenschaften ändern, ist es möglich, für den entsprechenden Suche Schlüssel nicht mit den neuen Werten synchronisiert werden, bis die Änderungen mit einem Aufruf der **SaveChanges** übernommen wurden. 
  
Der Wert des Schlüssels für ein Objekt Datensatz kann anders als der Wert der deren Search-Schlüssel, je nach den Dienstanbieter oder mit diesem identisch sein. Einige Dienstanbieter verwenden denselben Wert für ein Objekt suchen-Taste, Datensatzschlüssel und Eintrags-ID an. Andere Dienstanbieter weisen eindeutige Werte für die einzelnen Objekte Bezeichner. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)


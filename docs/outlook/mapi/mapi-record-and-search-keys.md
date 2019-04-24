---
title: MAPI-Eintrags-und-Suchschlüssel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328133"
---
# <a name="mapi-record-and-search-keys"></a>MAPI-Eintrags-und-Suchschlüssel

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Datensatzschlüssel und Suchschlüssel sind binäre Bezeichner, die vielen MAPI-Objekten zugewiesen sind. Im Gegensatz zur Eintrags-ID eines Objekts ist der Record-oder der Suchschlüssel direkt vergleichbar sowie transmitable. 
  
## <a name="record-keys"></a>Datensatzschlüssel

Ein Record-Schlüssel wird verwendet, um zwei Objekte zu vergleichen. Nachrichtenspeicher-und Adressbuch Objekte müssen Datensatzschlüssel enthalten, die in Ihrer **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md))-Eigenschaft gespeichert werden. Da ein Datensatzschlüssel ein Objekt und nicht dessen Daten identifiziert, verfügt jede Instanz eines Objekts über einen eindeutigen Record-Schlüssel. Der Bereich eines Daten Satz Schlüssels für Ordner und Nachrichten ist der Nachrichtenspeicher. Der Bereich für Adressbuchcontainer, Messagingbenutzer und Verteilerlisten ist die Gruppe von Containern auf oberster Ebene, die von MAPI zur Verwendung im integrierten Adressbuch bereitgestellt werden.
  
Datensatzschlüssel können in einer anderen Ressource dupliziert werden. Beispielsweise können unterschiedliche Nachrichten in zwei verschiedenen Nachrichten speichern denselben Record-Schlüssel aufweisen. Dies unterscheidet sich von langfristigen Eintrags Bezeichnern; Da langfristige Eintrags-IDs einen Verweis auf den Dienstanbieter enthalten, haben Sie einen größeren Bereich. Der Datensatzschlüssel eines Nachrichtenspeichers ähnelt dem Gültigkeitsbereich einer langfristigen Eintrags-ID. Sie sollte in allen Nachrichtenspeicher Anbietern eindeutig sein. Um diese Eindeutigkeit sicherzustellen, legen Nachrichtenspeicher Anbieter ihren Record-Schlüssel in der Regel auf einen Wert fest, der die Kombination ihrer **PR_MDB_PROVIDER** ([pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))-Eigenschaft und eines Bezeichners ist, der für den Nachrichtenspeicher eindeutig ist.
  
## <a name="search-keys"></a>Suchschlüssel

Ein Suchschlüssel wird verwendet, um die Daten in zwei Objekten zu vergleichen. Der Suchschlüssel eines Objekts wird in seiner **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft gespeichert. Da ein Suchschlüssel die Daten eines Objekts und nicht das Objekt selbst darstellt, können zwei verschiedene Objekte mit denselben Daten denselben Suchschlüssel aufweisen. Wenn ein Objekt kopiert wird, haben beispielsweise sowohl das ursprüngliche Objekt als auch die Kopie dieselben Daten und denselben Suchschlüssel.
  
Nachrichten und Messagingbenutzer haben Suchschlüssel. Der Suchschlüssel einer Nachricht ist ein eindeutiger Bezeichner der Daten der Nachricht. Nachrichtenspeicher Anbieter stellen die **PR_SEARCH_KEY** -Eigenschaft einer Nachricht zur Erstellungszeit der Nachricht bereit. Der Suchschlüssel eines Adressbucheintrags wird anhand des Adresstyps (**PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))) und der Adresse (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))) berechnet. Wenn der Adressbucheintrag beschreibbar ist, ist der Suchschlüssel möglicherweise erst verfügbar, wenn der Adresstyp und die Adresse mithilfe der [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode festgelegt wurden und der Eintrag mithilfe der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode gespeichert wurde. Wenn sich diese Adresseigenschaften ändern, ist es möglich, dass der entsprechende Suchschlüssel nicht mit den neuen Werten synchronisiert wird, bis die Änderungen mit einem **SaveChanges** -Aufruf übergeben wurden. 
  
Der Wert des Record-Schlüssels eines Objekts kann in Abhängigkeit vom Dienstanbieter mit oder unterschiedlich sein. Einige Dienstanbieter verwenden den gleichen Wert für die Such-, Daten Satz-und Eintrags-ID eines Objekts. Andere Dienstanbieter weisen für jeden Bezeichner der Objekte eindeutige Werte zu. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Anwendungsentwicklung](mapi-application-development.md)


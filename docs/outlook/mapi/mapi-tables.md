---
title: MAPI-Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6393de45dbfd130e15a0678f2b6a7f18968dfa03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573215"
---
# <a name="mapi-tables"></a>MAPI-Tabellen
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine MAPI-Tabelle ist ein MAPI-Objekt, das verwendet wird, um eine Auflistung von Eigenschaften, die von anderen MAPI-Objekten eines bestimmten Typs anzuzeigen. MAPI-Tabellen sind in einem Format Zeile und Spalte strukturiert, wobei jede Zeile für ein Objekt, und jeder Spalte, eine Eigenschaft des Objekts darstellt. Eine der Eigenschaften in der Regel in jeder Zeile enthalten ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft, einen Bezeichner, der verwendet werden kann, das Objekt zu öffnen. 
  
Da Zeilen Eigenschaftswerte enthalten, wird das Abrufen einer Zeile aus einer Tabelle ähnlich wie beim Abrufen einer Gruppe von Eigenschaften direkt aus dem Objekt, das die Zeile darstellt. Beide Vorgänge bewirken das Abrufen von einem Wertearray-Eigenschaft. Der Hauptunterschied ist bei der Verarbeitung des lange Zeichenfolge und binäre Eigenschaften. Für die Einbeziehung in einer Tabelle abschneiden einige Tabelle Implementierer diese Eigenschaften auf 255 Byte. Wenn direkt aus dem Objekt abgerufen wird, ist der vollständige Wert immer verfügbar.
  
Tabellen werden Zeichenfolgeneigenschaften Address Book und die Nachricht und MAPI, je nach Art der Tabelle und die darin enthaltenen Objekte implementiert. Ein Nachricht Store-Anbieter implementiert Ordnern und einer Inhaltstabelle für jeden Ordner, die Informationen über die Nachrichten im Ordner enthält. Adressbuch-Dienstanbieter implementiert Address Book Container und eine Hierarchietabelle, die ihre Organisation anzeigt. MAPI implementierte mehrere verschiedene Tabellen, einige für die Verwendung durch Clientanwendungen, einige für die Verwendung von Dienstanbietern und einige für die Verwendung durch die beiden. Die Statustabelle ist insofern MAPI letztlich die Tabelle bereitstellt, aber die Zeilen der Beiträge aus allen Arten von zusätzlich zu MAPI-Dienstanbieter bestehen. 
  
Die folgende Abbildung zeigt eine häufige Verwendungsmöglichkeiten von einer Tabelle in MAPI: zum Anzeigen des Inhalts eines Ordners. Auf der rechten Seite ist eine Darstellung von zwei Nachrichten wie in einer normalen messaging Clientanwendung angezeigt werden können. Die Anzeige enthält vier Arten von Informationen zu jeder Nachricht: der Absender, Empfänger, Betreff und den Nachrichtentext. Jede Informationseinheit entspricht einer Eigenschaft der Nachricht.
  
Auf der linken Seite ist eine Ansicht der Inhaltstabelle, die die beiden Nachrichten enthält. Während der Inhaltstabelle zehn Zeilen behandeln, da der Ordner zehn Nachrichten, wobei jede Zeile enthält viele mehr als drei Spalten hat ist in dieser bestimmte Ansicht auf nur zwei Zeilen und drei Spalten beschränkt.
  
In der folgenden Tabelle werden die Eigenschaften gezeigt, die die Spalte für die Tabellenansicht festlegen bilden.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Name des Absenders  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Datum und Uhrzeit, wann die Nachricht gesendet wurde  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Betreffzeile der Nachricht  <br/> |
   
Beachten Sie, dass die Gruppe von Eigenschaften, die in der Nachricht angezeigt sind nicht identisch mit der Satz von Spalten in der Tabelle angezeigt. Die Implementierung der Tabelle, in diesem Fall eine Nachricht Speicheranbieter, Netzteile eine Standardeinstellung von Spalten in einer Standardreihenfolge festlegen. Der Client kann dieser Gruppe Spalte ändern, die zusätzliche Spalten anfordern oder ablehnen Standardattribute, und bitten Sie, dass sie auf eine bestimmte Weise sortiert werden. Der Client kann auch die Zeilen bestellen sie entsprechend dem Wert der eine oder mehrere Spalten zu sortieren.
  
**Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten**
  
![Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten] (media/amapi_54.gif "Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten")
  
Es gibt zwei Schnittstellen für das Arbeiten mit Tabellen:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) ermöglicht Clients und -Dienstanbieter eine schreibgeschützte Ansicht der zugrunde liegenden Daten der Tabelle, Zugang zum Anzeigen und ändern nur die Präsentation. Mehrere Benutzer können die gleichen Daten während der **IMAPITable**zugreifen. **IMAPITable** wird durch MAPI und Dienstanbieter implementiert. 
    
- [ITableData: IUnknown](itabledataiunknown.md) bietet Clients und Dienstanbieter Lese-/Schreibzugriff auf die zugrunde liegenden Daten der Tabelle, Zugang zur dauerhafte Änderungen vornehmen. **IMAPITable** von MAPI implementierte und in erster Linie vom Dienstanbieter, die darauf zugreifen, indem Sie das Aufrufen der [CreateTable](createtable.md) -Funktion verwendet. Die Implementierung **ITableData** enthält alle Daten für die Tabelle und alle zugeordneten Einschränkungen im Speicher, wodurch nicht geeignet für mit sehr große Tabellen verwenden. Zusammengesetzter Einschränkungen und komplexe Vorgänge wie Kategorisierung werden nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte](mapi-concepts.md)


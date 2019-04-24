---
title: MAPI-Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 840c34a64cd0478be8f208799653b9916f50079d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355836"
---
# <a name="mapi-tables"></a>MAPI-Tabellen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine MAPI-Tabelle ist ein MAPI-Objekt, das zum Anzeigen einer Auflistung von Eigenschaften verwendet wird, die zu anderen MAPI-Objekten eines bestimmten Typs gehören. MAPI-Tabellen werden in einem Zeilen-und Spaltenformat mit jeder Zeile strukturiert, die ein Objekt darstellt, und jede Spalte, die eine Eigenschaft des Objekts darstellt. Eine der Eigenschaften, die in der Regel in jeder Zeile enthalten ist, ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft, eine ID, die zum Öffnen und Ändern des Objekts verwendet werden kann. 
  
Da Zeilen Eigenschaftswerte enthalten, ähnelt das Abrufen einer Zeile aus einer Tabelle dem Abrufen einer Gruppe von Eigenschaften direkt aus dem Objekt, das die Zeile darstellt. Beide Vorgänge führen zum Abrufen eines Eigenschafts Wertarrays. Der Hauptunterschied liegt bei der Behandlung von Long-Zeichenfolgen und binären Eigenschaften. Für die Aufnahme in eine Tabelle schneiden einige Tabellen Implementierer Diese Eigenschaften auf 255 Bytes ab. Wenn Sie direkt aus dem Objekt abgerufen werden, ist der vollständige Wert immer verfügbar.
  
Tabellen werden von Adressbuch-und Nachrichtenspeicher Anbietern und von MAPI abhängig vom Tabellentyp und den darin enthaltenen Objekten implementiert. Ein Nachrichtenspeicher Anbieter implementiert Ordner und eine Inhaltstabelle für jeden Ordner, der Informationen zu den Nachrichten im Ordner enthält. Ein Adressbuchanbieter implementiert Adressbuchcontainer und eine Hierarchietabelle, die Ihre Organisation anzeigt. MAPI implementiert mehrere verschiedene Tabellen, einige für die Verwendung durch Clientanwendungen, einige für die Verwendung durch Dienstanbieter und einige für beide. Die Statustabelle ist insofern eindeutig, als MAPI die Tabelle schließlich bereitstellt, aber die Zeilen umfassen zusätzlich zu MAPI Beiträge von allen Arten von Dienstanbietern. 
  
Die folgende Abbildung zeigt eine häufige Verwendung einer Tabelle in MAPI: So zeigen Sie den Inhalt eines Ordners an. Auf der rechten Seite befindet sich eine Anzeige von zwei Nachrichten, die in einer typischen Messaging-Clientanwendung angezeigt werden können. Die Anzeige enthält vier Informationen zu jeder Nachricht: Absender, Empfänger, Betreff und Nachrichtentext. Jede Information entspricht einer Eigenschaft der Nachricht.
  
Auf der linken Seite befindet sich eine Ansicht der Inhaltstabelle, die diese beiden Nachrichten enthält. In der Erwägung, dass die Tabelle Contents zehn Zeilen enthalten kann, da der Ordner zehn Nachrichten enthält, wobei jede Zeile mit mehr als drei Spalten angezeigt wird, ist diese Ansicht auf nur zwei Zeilen und drei Spalten beschränkt.
  
In der folgenden Tabelle sind die Eigenschaften aufgeführt, aus denen die Spaltengruppe für die Tabellenansicht besteht.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Absender Name  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([Pidtagoriginaldeliverytime (](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Datum und Uhrzeit der Nachrichtenübermittlung  <br/> |
|**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Nachrichtenbetreff  <br/> |
   
Beachten Sie, dass die in der Nachricht angezeigten Eigenschaften nicht mit den in der Tabelle angezeigten Spalten übereinstimmen. Die Implementierung der Tabelle, in diesem Fall ein Nachrichtenspeicher Anbieter, stellt einen Standardsatz von Spalten in einer Standardreihenfolge bereit. Der Client kann diesen Spaltensatz ändern, um zusätzliche Spalten anzufordern oder standardmäßig abzulehnen, und die Bestellung auf eine bestimmte Weise zu stellen. Der Client kann die Zeilen auch sortieren, indem er Sie nach dem Wert einer oder mehrerer Spalten sortiert.
  
**Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten**
  
![Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten] (media/amapi_54.gif "Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten")
  
Es gibt zwei Schnittstellen für das Arbeiten mit Tabellen:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) gibt Clients und Dienstanbietern eine schreibgeschützte Ansicht der zugrunde liegenden Daten der Tabelle, sodass Sie nur die Präsentation anzeigen und ändern können. Mehrere Benutzer können gleichzeitig mit **IMAPITable**auf dieselben Daten zugreifen. **IMAPITable** wird von MAPI und von Dienstanbietern implementiert. 
    
- [ITableData: IUnknown](itabledataiunknown.md) gibt Clients und Dienstanbietern Lese-/Schreibzugriff auf die zugrunde liegenden Daten der Tabelle, sodass Sie dauerhafte Änderungen vornehmen können. **IMAPITable** wird von MAPI implementiert und hauptsächlich von Dienstanbietern verwendet, die darauf zugreifen, [](createtable.md) indem Sie die createable-Funktion aufrufen. Die **ITableData** -Implementierung enthält alle Daten für die Tabelle und alle zugeordneten Einschränkungen im Arbeitsspeicher, sodass Sie nicht für sehr große Tabellen verwendet werden kann. Verbund Einschränkungen und komplexe Vorgänge wie Kategorisierung werden nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte (engl.)](mapi-concepts.md)


---
title: MAPI-Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 23f847e525cbfd5d6bc54b54010f09677ec1028c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595770"
---
# <a name="mapi-tables"></a>MAPI-Tabellen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine MAPI-Tabelle ist ein MAPI-Objekt, das zum Anzeigen einer Auflistung von Eigenschaften verwendet wird, die zu anderen MAPI-Objekten eines bestimmten Typs gehören. MAPI-Tabellen sind im Zeilen- und Spaltenformat strukturiert, wobei jede Zeile ein Objekt und jede Spalte eine Eigenschaft des Objekts darstellt. Eine der eigenschaften in der Regel in jeder Zeile enthalten ist die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft, ein Bezeichner, der zum Öffnen und Ändern des Objekts verwendet werden kann. 
  
Da Zeilen Eigenschaftswerte enthalten, ähnelt das Abrufen einer Zeile aus einer Tabelle dem Abrufen eines Eigenschaftensatzes direkt aus dem Objekt, das die Zeile darstellt. Beide Vorgänge führen zum Abrufen eines Eigenschaftswertarrays. Der Hauptunterschied besteht in der Behandlung von langen Zeichenfolgen- und binären Eigenschaften. Zur Aufnahme in eine Tabelle werden diese Eigenschaften von einigen Tabellen implementierern auf 255 Byte gekürzt. Wenn sie direkt aus dem Objekt abgerufen wird, ist der vollständige Wert immer verfügbar.
  
Tabellen werden von Adressbuch- und Nachrichtenspeicheranbietern und von MAPI implementiert, je nach Typ der Tabelle und den darin enthaltenen Objekten. Ein Nachrichtenspeicheranbieter implementiert Ordner und ein Inhaltsverzeichnis für jeden Ordner, der Informationen zu den Nachrichten im Ordner enthält. Ein Adressbuchanbieter implementiert Adressbuchcontainer und eine Hierarchietabelle, in der ihre Organisation angezeigt wird. MAPI implementiert mehrere unterschiedliche Tabellen, einige für die Verwendung durch Clientanwendungen, einige für die Verwendung durch Dienstanbieter und einige für die Verwendung durch beide. Die Statustabelle ist eindeutig, da die MAPI letztendlich die Tabelle bereitstellt, aber die Zeilen bestehen aus Beiträgen aller Arten von Dienstanbietern zusätzlich zur MAPI. 
  
Die folgende Abbildung zeigt eine der häufigen Verwendungsmöglichkeiten einer Tabelle in mapi: zum Anzeigen des Inhalts eines Ordners. Auf der rechten Seite werden zwei Nachrichten angezeigt, die in einer typischen Messaging-Clientanwendung angezeigt werden können. Die Anzeige enthält vier Informationen zu jeder Nachricht: den Absender, den Empfänger, den Betreff und den Nachrichtentext. Jede Information entspricht einer Eigenschaft der Nachricht.
  
Auf der linken Seite befindet sich eine Ansicht des Inhaltsverzeichnisses, das diese beiden Nachrichten enthält. Während das Inhaltsverzeichnis möglicherweise zehn Zeilen enthält, da der Ordner zehn Nachrichten enthält, wobei jede Zeile viele mehr als drei Spalten enthält, ist diese bestimmte Ansicht auf nur zwei Zeilen und drei Spalten beschränkt.
  
In der folgenden Tabelle sind die Eigenschaften aufgeführt, aus denen sich die für die Tabellenansicht festgelegte Spalte zusammensetzen.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Absendername  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Datum und Uhrzeit, zu der die Nachricht gesendet wurde  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Betreffzeile der Nachricht  <br/> |
   
Beachten Sie, dass die in der Nachricht angezeigten Eigenschaften nicht mit dem In der Tabelle angezeigten Spaltensatz übereinstimmen. Der Implementierer der Tabelle, in diesem Fall ein Nachrichtenspeicheranbieter, stellt einen Standardsatz von Spalten in einer Standardreihenfolge bereit. Der Client kann diesen Spaltensatz ändern, zusätzliche Spalten anfordern oder Standardspalten ablehnen und eine bestimmte Reihenfolge anfordern. Der Client kann die Zeilen auch sortieren und nach dem Wert einer oder mehrerer Spalten sortieren.
  
**Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten**
  
![Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten](media/amapi_54.gif "Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten")
  
Es gibt zwei Schnittstellen zum Arbeiten mit Tabellen:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) bietet Clients und Dienstanbietern eine schreibgeschützte Ansicht der zugrunde liegenden Daten der Tabelle, sodass sie nur die Präsentation anzeigen und ändern können. Mehrere Benutzer können gleichzeitig mit **IMAPITable** auf dieselben Daten zugreifen. **IMAPITable** wird von mapi und von Dienstanbietern implementiert. 
    
- [ITableData : IUnknown](itabledataiunknown.md) bietet Clients und Dienstanbietern Lese-/Schreibzugriff auf die zugrunde liegenden Daten der Tabelle, sodass sie dauerhafte Änderungen vornehmen können. **IMAPITable** wird von der MAPI implementiert und hauptsächlich von Dienstanbietern verwendet, die durch Aufrufen der [CreateTable-Funktion](createtable.md) darauf zugreifen. Die **ITableData-Implementierung** enthält alle Daten für die Tabelle und alle zugehörigen Einschränkungen im Arbeitsspeicher, sodass sie nicht für die Verwendung mit sehr großen Tabellen geeignet sind. Zusammengesetzte Einschränkungen und komplexe Vorgänge wie kategorisierung werden nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte](mapi-concepts.md)


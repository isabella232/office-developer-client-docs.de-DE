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
ms.openlocfilehash: 840c34a64cd0478be8f208799653b9916f50079d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437084"
---
# <a name="mapi-tables"></a>MAPI-Tabellen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine MAPI-Tabelle ist ein MAPI-Objekt, das zum Anzeigen einer Auflistung von Eigenschaften verwendet wird, die zu anderen MAPI-Objekten eines bestimmten Typs gehören. MAPI-Tabellen sind in einem Zeilen- und Spaltenformat strukturiert, in dem jede Zeile ein Objekt darstellt, und jede Spalte, die eine Eigenschaft des Objekts darstellt. Eine der In der Regel in jeder Zeile **enthaltenen Eigenschaften** ist die PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft, ein Bezeichner, der zum Öffnen und Ändern des Objekts verwendet werden kann. 
  
Da Zeilen Eigenschaftswerte enthalten, ähnelt das Abrufen einer Zeile aus einer Tabelle dem Abrufen einer Reihe von Eigenschaften direkt aus dem Objekt, das die Zeile darstellt. Beide Vorgänge führen zum Abrufen eines Eigenschaftswertarrays. Der Hauptunterschied besteht in der Verarbeitung von langen Zeichenfolgen- und binären Eigenschaften. Für die Aufnahme in eine Tabelle werden diese Eigenschaften von einigen Tabellen implementierern auf 255 Byte gekürzt. Wenn sie direkt aus dem Objekt abgerufen werden, ist der vollständige Wert immer verfügbar.
  
Tabellen werden von Adressbuch- und Nachrichtenspeicheranbietern und von MAPI implementiert, je nach Art der Tabelle und den objekten in ihr. Ein Nachrichtenspeicheranbieter implementiert Ordner und eine Inhaltstabelle für jeden Ordner, die Informationen zu den Nachrichten im Ordner enthält. Ein Adressbuchanbieter implementiert Adressbuchcontainer und eine Hierarchietabelle, die ihre Organisation zeigt. MAPI implementiert mehrere verschiedene Tabellen, einige für die Verwendung durch Clientanwendungen, einige für die Verwendung durch Dienstanbieter und einige für die Verwendung durch beide. Die Statustabelle ist eindeutig, da MAPI die Tabelle letztendlich liefert, aber die Zeilen bestehen aus Beiträgen aller Arten von Dienstanbietern zusätzlich zu MAPI. 
  
Die folgende Abbildung zeigt eine der häufigen Verwendungen einer Tabelle in MAPI: zum Anzeigen des Inhalts eines Ordners. Auf der rechten Seite werden zwei Nachrichten angezeigt, wie sie in einer typischen Messagingclientanwendung angezeigt werden können. Die Anzeige enthält vier Informationen zu jeder Nachricht: den Absender, den Empfänger, den Betreff und den Nachrichtentext. Jede Information entspricht einer Eigenschaft der Nachricht.
  
Auf der linken Seite befindet sich eine Ansicht der Inhaltstabelle, die diese beiden Nachrichten enthält. Während die Inhaltstabelle zehn Zeilen enthalten kann, da der Ordner zehn Nachrichten enthält, wobei jede Zeile mehr als drei Spalten enthält, ist diese ansicht auf nur zwei Zeilen und drei Spalten beschränkt.
  
In der folgenden Tabelle sind die Eigenschaften aufgeführt, die den Spaltensatz für die Tabellenansicht enthalten.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Absendername  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Datum und Uhrzeit, zu dem die Nachricht gesendet wurde  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Betreffzeile für Nachrichten  <br/> |
   
Beachten Sie, dass die in der Nachricht angezeigten Eigenschaften nicht mit dem In der Tabelle angezeigten Spaltensatz identisch sind. Der Implementier der Tabelle, in diesem Fall ein Nachrichtenspeicheranbieter, stellt einen Standardsatz von Spalten in einer Standardreihenfolge zur. Der Client kann diesen Spaltensatz ändern, zusätzliche Spalten anfordern oder Standardspalten ablehnen und eine bestimmte Reihenfolge anfordern. Der Client kann die Zeilen auch nach dem Wert einer oder mehreren Spalten sortieren.
  
**Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten**
  
![Verwenden einer Tabelle zum Anzeigen von Ordnerinhalten]Verwenden einer Tabelle zum Anzeigen(media/amapi_54.gif "von Ordnerinhalten")
  
Es gibt zwei Schnittstellen zum Arbeiten mit Tabellen:
  
- [IMAPITable : IUnknown](imapitableiunknown.md) bietet Clients und Dienstanbietern eine schreibgeschützte Ansicht der zugrunde liegenden Daten der Tabelle, sodass sie nur die Präsentation anzeigen und ändern können. Mehrere Benutzer können gleichzeitig mit **IMAPITable** auf dieselben Daten zugreifen. **IMAPITable** wird von MAPI und von Dienstanbietern implementiert. 
    
- [ITableData : IUnknown](itabledataiunknown.md) ermöglicht Clients und Dienstanbietern Lese-/Schreibzugriff auf die zugrunde liegenden Daten der Tabelle, sodass sie dauerhafte Änderungen vornehmen können. **IMAPITable** wird von MAPI implementiert und hauptsächlich von Dienstanbietern verwendet, die darauf zugreifen, indem sie die [CreateTable-Funktion](createtable.md) aufrufen. Die **ITableData-Implementierung** enthält alle Daten für die Tabelle und alle zugehörigen Einschränkungen im Arbeitsspeicher, wodurch sie für die Verwendung mit sehr großen Tabellen ungeeignet ist. Zusammengesetzte Einschränkungen und komplexe Vorgänge wie kategorisierung werden nicht unterstützt. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Konzepte (engl.)](mapi-concepts.md)


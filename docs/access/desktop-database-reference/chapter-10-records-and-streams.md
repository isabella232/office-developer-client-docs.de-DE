---
title: 'Kapitel 10: Datensätze und Datenströme'
TOCTitle: 'Chapter 10: Records and streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a47ac1f850905546651ffbdd708887bf7d74940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296493"
---
# <a name="chapter-10-records-and-streams"></a>Kapitel 10: Datensätze und Datenströme

**Gilt für**: Access 2013, Office 2013

Zurzeit wird durch ADO das [Recordset](recordset-object-ado.md)-Objekt als primäre Methode für das Zugreifen auf Informationen in Datenquellen, z. B. in relationalen Datenbanken, bereitgestellt. Von manchen Anbietern werden jedoch die Objekte [Record](record-object-ado.md) und [Stream](stream-object-ado.md) als alternative oder ergänzende Objekte, mit denen Daten von Anbietern geändert werden können, bereitgestellt. Einzelheiten zum Verhalten von **Record** finden Sie in der Dokumentation des Anbieters.

## <a name="records"></a>Datensätze

**Record**-Objekte fungieren im Wesentlichen als einzeilige **Datensätze**. **Datensätze** verfügen jedoch im Vergleich zu **Recordsets** über eine eingeschränkte Funktionalität und unterschiedliche Eigenschaften und Methoden. Die Quelle für die Daten in einem **Record**-Objekt kann ein Befehl sein, durch den eine Zeile mit Daten vom Anbieter zurückgegeben wird. Das Verwenden von **Record**-Objekten anstelle von **Recordset**-Objekten zum Empfangen der Ergebnisse aus einer Abfrage, durch die eine Zeile mit Daten zurückgegeben wird, eliminiert den Aufwand für das Instanziieren des komplexeren **Recordset**-Objekts.

**Record**-Objekte können zu einem anderen Zweck dienen, insbesondere bei anderen Anbietern als herkömmlichen relationalen Datenbanken für Datenquellen, z. B. dem [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Ein großer Teil der zu verarbeitenden Informationen ist nicht als Tabellen in Datenbanken, sondern als Nachrichten in elektronischen Mailsystemen und Dateien in modernen Dateisystemen vorhanden. Die Objekte **Record** und **Stream** ermöglichen den Zugriff auf Informationen, die in anderen Quellen als in relationalen Datenbanken gespeichert sind.

Das **Record** -Objekt kann Daten wie Verzeichnisse und Dateien in einem Dateisystem oder in Ordnern und Nachrichten in einem e-Mail-System darstellen und verwalten. Zu diesen Zwecken kann die Quelle für das **Record**-Objekt die aktuelle Zeile eines geöffneten **Recordset**-Objekts, eine absolute URL oder eine relative URL in Verbindung mit einem geöffneten [Connection](connection-object-ado.md)-Objekt sein.

Normalerweise kann ein **Recordset** -Objekt verwendet werden, um einen Container oder einen übergeordneten Container in einer Hierarchie, z. B. einen Ordner oder ein Verzeichnis, darzustellen. Ein **Record** -Objekt kann verwendet werden, um bestimmte Informationen zu einem Knoten im übergeordneten Container, z. B. eine Datei oder ein Dokument, zurückzugeben. Der Hauptgrund für die Verwendung von **Record** -Objekten zum Darstellen dieses Informationstyps besteht darin, dass diese Datenquellen heterogen sind. Das heißt, dass jedes **Record** -Objekt verschiedene und unterschiedlich viele Felder enthalten kann. Herkömmliche **Recordset** -Objekte, die Zeilen aus einer Datenbank enthalten, sind homogen, d. h., jede Zeile enthält gleich viele Felder vom gleichen Typ.

Weitere Informationen zum Verwenden des **Record** -Objekts zum Verarbeiten dieser heterogenen Daten von Anbietern wie dem Internet Publishing-Anbieter finden Sie unter [Verwenden von ADO für Internet Publishing](using-ado-for-internet-publishing.md).

## <a name="streams"></a>Datenströme

Durch das **Stream** -Objekt wird die Möglichkeit zum Lesen, Schreiben und Verwalten eines Bytedatenstroms bereitgestellt. Dieser Bytedatenstrom kann aus Text oder Binärdaten bestehen und ist in der Größe nur durch die Systemressourcen beschränkt. Normalerweise werden **Stream** -ADO-Objekte für die folgenden Zwecke verwendet:

- Abrufen des Texts oder der Bytes, aus denen eine Datei oder Nachricht besteht, wird normalerweise mit Anbietern wie dem Microsoft OLE DB-Anbieter für Internet Publishing verwendet. Weitere Informationen zu dieser Verwendung von **Stream** -Objekten finden Sie unter [Verwenden von ADO für Internet Publishing](using-ado-for-internet-publishing.md).

Ein **Stream** -Objekt kann für Folgendes geöffnet werden:

- Eine einfache Datei, die mit einer URL angegeben wird.

- Ein Feld eines **Record** oder **Recordset** -Objekts, das ein **Stream** -Objekt enthält.

- Den Standarddatenstrom eines **Record** - oder **Recordset** -Objekts, das ein Verzeichnis oder eine Verbunddatei darstellt.

- Ein Ressourcenfeld, das die URL einer einfachen Datei enthält.

- Keine bestimmte Quelle. In diesem Fall wird ein **Stream** -Objekt im Arbeitsspeicher geöffnet. Es ist möglich, Daten in das Objekt zu schreiben und es in einem anderen **Stream** -Objekt oder einer Datei zu speichern.

- Ein BLOB-Feld in einem **Recordset** -Objekt.

In diesem Kapitel werden die folgenden Themen behandelt:

- [Datenströme und Speicherung](streams-and-persistence.md)
- [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md)
- [Absolute und relative URLs](absolute-and-relative-urls.md)
- [Verwenden von ADO für Internet Publishing (ADO)](using-ado-for-internet-publishing.md)

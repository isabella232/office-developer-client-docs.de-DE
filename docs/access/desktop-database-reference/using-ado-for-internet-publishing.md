---
title: Verwenden von ADO für Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f8266d2b632b27ee4fafbb4ed0634def544c17a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860259"
---
# <a name="using-ado-for-internet-publishing"></a>Verwenden von ADO für Internet Publishing


**Betrifft**: Access 2013 | Office 2013



In [Der OLE DB-Anbieter für Internet Publishing](the-ole-db-provider-for-internet-publishing.md) wird ein konkretes Beispiel für das Zugreifen auf heterogene Daten mit ADO gezeigt. Während sich die Beispiele in diesem Abschnitt speziell auf das Verwenden des Internet Publishing-Anbieters beziehen, sollten die veranschaulichten Prinzipien mit denen für die Verwendung von ADO mit anderen Anbietern für heterogene Daten, z. B. einem Anbieter für einen E-Mail-Speicher, vergleichbar sein.

## <a name="urls"></a>URLs

URLs (Uniform Resource Locators) können als Alternative zu Verbindungszeichenfolgen und Befehlstext verwendet werden, um Datenquellen und Speicherorte von Dateien und Verzeichnissen anzugeben. Sie können URLs mit den vorhandenen Objekten [Connection](connection-object-ado.md) und **Recordset** sowie mit den Objekten **Record** und **Stream** verwenden.

Weitere Informationen zum Verwenden von URLs finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).

## <a name="record-fields"></a>Record-Felder

Der entscheidende Unterschied zwischen heterogenen Daten und homogenen Daten besteht darin, dass für erstere jede Zeile mit Daten bzw. jeder **Datensatz** einen unterschiedlichen Satz Spalten bzw. **Felder** enthalten kann. Bei homogenen Daten enthält jede Zeile den gleichen Satz Spalten. Weitere Informationen zu den spezifischen Feldern für den Internet Publishing-Anbieter finden Sie unter [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md).

## <a name="appending-new-fields"></a>Anfügen neuer Felder

Mehrere ADO-Objekte wurden verbessert, um mit den Objekten **Record** und **Stream** zusammenzuarbeiten.

  - Mit der [Append](fields-collection-ado.md)-Methode der [Fields](append-method-ado.md)-Auflistung, durch die ein [Field](field-object-ado.md)-Objekt erstellt und der Auflistung hinzugefügt wird, kann auch der Wert von **Field** angegeben werden.

  - Durch die [Update](update-method-ado.md)-Methode wird die Hinzufügung oder Löschung von Feldern in der Auflistung fertig gestellt.

  - Als Abkürzung und Alternative zur **Append** -Methode können Sie Felder erstellen, indem Sie einfach einem nicht definierten oder vorher gelöschten Feld einen Wert zuweisen.

## <a name="see-also"></a>Siehe auch

- [Internet Publishing-Szenario Themen](internet-publishing-scenario.md)
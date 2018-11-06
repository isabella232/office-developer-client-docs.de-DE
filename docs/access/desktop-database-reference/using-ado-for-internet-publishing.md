---
title: Verwenden von ADO für Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e63e765461eec1c89f3e3dc04d35f1bf88a3c578
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997623"
---
# <a name="using-ado-for-internet-publishing"></a>Verwenden von ADO für Internet publishing


**Betrifft**: Access 2013, Office 2013



[OLE DB-Anbieter für Internet Publishing](the-ole-db-provider-for-internet-publishing.md) zeigt ein bestimmtes Beispiel für den Zugriff auf heterogenen Daten mit ADO. Während der Beispiele in diesem Abschnitt speziell für mit dem Internet Publishing-Anbieter werden, sollten die veranschaulichten Prinzipien ähnlich sein, wenn ADO mit anderen Anbietern für heterogenen Daten enthält, wie ein Anbieter für einen e-Mail-Speicher.

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
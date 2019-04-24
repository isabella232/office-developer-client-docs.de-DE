---
title: 'Anhang A: Anbieter'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4549c8817361cfb5b9fa730ee37ca6a07edc98b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297060"
---
# <a name="appendix-a-providers"></a>Anhang A: Anbieter


**Gilt für**: Access 2013, Office 2013


In diesem Abschnitt werden drei Arten von Anbietern beschrieben: Datenprovider, Dienstanbieter und Dienstkomponenten. Anbieter können in zwei Kategorien geteilt werden: diejenigen, die Daten anbieten, und diejenigen, die Dienste anbieten. Ein *Datenprovider* besitzt eigene Daten und stellt diese für Ihre Anwendung in tabellarischer Form bereit. Ein *Dienstanbieter* kapselt einen Dienst durch Erstellen und Verwenden von Daten und Vergrößern von Features in den ADO-Anwendungen. Ein Dienstanbieter kann darüber hinaus auch als *Dienstkomponente* definiert werden, die mit anderen Dienstanbietern oder -komponenten verwendet werden muss.

## <a name="data-providers"></a>Datenanbieter

ADO ist leistungsfähig und flexibel, da es eine Verbindung mit einem beliebigen Datenprovider herstellen und unabhängig von den spezifischen Features eines bestimmten Anbieters dennoch dasselbe Programmiermodell verfügbar machen kann.

Da jedoch jeder Datenprovider einzigartig ist, ergeben sich bei der Interaktion der Anwendung mit ADO je nach Datenprovider geringfügige Abweichungen. Die Abweichungen können einer von drei Kategorien zugeordnet werden:

- Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.

- Verwendung des [Command](command-object-ado.md)-Objekts.

- Anbieterspezifisches [Recordset](recordset-object-ado.md)-Verhalten.

Ausführliche Informationen zu den derzeit von Microsoft erhältlichen Datenprovidern finden Sie in den folgenden Abschnitten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bereich</p></th>
<th><p>Thema</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ODBC-Datenbanken</p></td>
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB-Anbieter für ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Indexdienst</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB-Anbieter für Microsoft Indexdienst</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Active Directory-Dienst</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB-Anbieter für Microsoft Active Directory-Dienst</a></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Jet-Datenbanken</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Microsoft OLE DB-Anbieter für Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB-Anbieter für SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Oracle-Datenbanken</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB-Anbieter für Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Internet Publishing</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB-Anbieter für Internet Publishing</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Anbieterspezifische dynamische Eigenschaften

Die [Properties](properties-collection-ado.md)-Auflistungen von [Connection](connection-object-ado.md)-, [Command](command-object-ado.md)- und [Recordset](recordset-object-ado.md)-Objekten enthalten anbieterspezifische dynamische Eigenschaften. Diese Eigenschaften stellen über die von ADO unterstützten integrierten Eigenschaften hinaus Informationen zur anbieterspezifischen Funktionalität bereit.

After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties. Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.

## <a name="service-providers"></a>Dienstanbieter

Um einen Dienstanbieter zu verwenden, müssen Sie ein Schlüsselwort angeben. Darüber hinaus müssen Sie die anbieterspezifischen dynamischen Eigenschaften kennen, die den einzelnen Dienstanbietern zugeordnet sind. Informationen zu anwenderspezifischen Eigenschaften für die derzeit von Microsoft erhältlichen Dienstanbieter finden Sie in den folgenden Abschnitten:

- [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [Microsoft OLE DB-Anbieter für Persistenz](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [Microsoft OLE DB-Anbieter für Remoting](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Dienstkomponenten

Die Dienstkomponente [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ergänzt die Cursor-Hilfsfunktionen von Datenanbietern. Sie erfordert ebenfalls ein Schlüsselwort und hat dynamische Eigenschaften.

For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

## <a name="provider-commands"></a>Anbieter Befehle

Wenn Ihre Anwendungen Benutzern die Eingabe von SQL-Anweisungen als Anbieter Befehle gestatten, müssen Sie für jeden hier aufgeführten Anbieter die Benutzereingabe immer überprüfen und auf mögliche Hackerangriffe mit potenziell gefährlichen SQL-Anweisungen wie, als Teil des Benutzereingabe.


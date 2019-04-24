---
title: Erstellen der Verbindungszeichenfolge
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295327"
---
# <a name="creating-the-connection-string"></a>Erstellen der Verbindungszeichenfolge

**Gilt für**: Access 2013, Office 2013

ADO unterstützt direkt fünf Argumente in einer Verbindungszeichenfolge. Andere Argumente werden ohne Verarbeitung durch ADO an den Anbieter übergeben, der im Argument *Provider* angegeben ist.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider</em></p></td>
<td><p>Gibt den Namen eines Anbieters an, der für die Verbindung verwendet werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>File Name</em></p></td>
<td><p>Gibt den Namen einer anbieterspezifischen Datei an (z. B. ein gespeichertes Datenquellenobjekt), die voreingestellte Verbindungsinformationen enthält.</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em></p></td>
<td><p>Gibt die Verbindungszeichenfolge als absolute URL an, die eine Ressource wie z. B. eine Datei oder ein Verzeichnis identifiziert.</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Provider</em></p></td>
<td><p>Gibt den Namen eines Anbieters an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Server</em></p></td>
<td><p>Gibt den Pfadnamen des Servers an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll. (Nur Remote Datendienst.)</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> In den folgenden Beispielen und im ADO-Programmierhandbuch wird die Benutzer-ID "MyId" mit dem Kennwort "123aBc" zur Authentifizierung beim Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Ersetzen Sie außerdem "MySqlServer" durch den Namen Ihres Servers.

Für die HelloData-Anwendung in Kapitel 1 wurde die folgende Verbindungszeichenfolge verwendet:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

In dieser Verbindungszeichenfolge wurde nur der ADO-Parameter "Provider=SQLOLEDB" bereitgestellt, der für den Microsoft OLE DB-Anbieter für SQL Server steht. Weitere gültige Parameter, die in der Verbindungszeichenfolge übergeben werden können, können mithilfe der Dokumentation des jeweiligen Anbieters bestimmt werden. Gemäß der Dokumentation zum OLE DB-Anbieter für SQL Server können Sie den *Data Source*-Parameter durch "Server" und den *Initial Catalog*-Parameter durch "Database" ersetzen. Die folgende Verbindungszeichenfolge würde demnach die gleichen Ergebnisse wie die erste Verbindungszeichenfolge liefern:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

Um die Verbindung zu öffnen, übergeben Sie einfach die Verbindungszeichenfolge als erstes Argument in der **Open** -Methode des **Connection** -Objekts:

```vb 
 
objConn.Open m_sConnStr 
```

Viele dieser Informationen können auch bereitgestellt werden, indem Sie Eigenschaften des **Connection** -Objekts vor dem Öffnen der Verbindung festlegen. Beispielsweise könnten Sie mit dem folgenden Code denselben Effekt wie mit der obigen Verbindungszeichenfolge erzielen:

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```


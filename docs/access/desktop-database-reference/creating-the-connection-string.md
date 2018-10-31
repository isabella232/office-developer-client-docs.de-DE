---
title: Erstellen der Verbindungszeichenfolge
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d4c869d6021c807e27fb7970ef6ea91f91bd4de
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860455"
---
# <a name="creating-the-connection-string"></a>Erstellen der Verbindungszeichenfolge


**Betrifft**: Access 2013 | Office 2013

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
<td><p><em>Dateiname</em></p></td>
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
<td><p>Gibt den Pfadnamen des Servers an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> In den folgenden Beispielen und im ADO-Programmierhandbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Ersetzen Sie außerdem "MySqlServer" durch den Namen Ihres Servers.

Für die HelloData-Anwendung in Kapitel 1 wurde die folgende Verbindungszeichenfolge verwendet:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

In dieser Verbindungszeichenfolge wurde nur der ADO-Parameter "Provider=SQLOLEDB" bereitgestellt, der für den Microsoft OLE DB-Anbieter für SQL Server steht. Weitere gültige Parameter, die in der Verbindungszeichenfolge übergeben werden können, können mithilfe der Dokumentation des jeweiligen Anbieters bestimmt werden. Gemäß den OLE DB-Anbieter für SQL Server-Dokumentation können Sie für den Parameter *Initial Catalog* "Server" für den Parameter *Datenquelle* und "Database" ersetzen. Die folgende Verbindungszeichenfolge würde demnach die gleichen Ergebnisse wie die erste Verbindungszeichenfolge liefern:

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


---
title: Datenbindungsobjekt des Adressbuchs
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc8fe1fa2addab5338d7c330d90e8616f0af9b5c
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025714"
---
# <a name="address-book-data-binding-object"></a>Datenbindungsobjekt des Adressbuchs


**Betrifft**: Access 2013, Office 2013

In der Adressbuchanwendung wird das [RDS.DataControl](datacontrol-object-rds.md)-Objekt zum Binden von Daten von der SQL Server-Datenbank an visuelle Objekte (in diesem Fall eine DHTML-Tabelle) in der Client-HTML-Seite der Anwendung verwendet. Die ereignisgesteuerte VBScript-Programmlogik verwendet [RDS.DataControl](datacontrol-object-rds.md) für Folgendes:

  - Die Datenbank abfragen, Aktualisierungen an die Datenbank senden, und das Datenraster aktualisieren.

  - Es Benutzern ermöglichen, zum ersten, zum nächsten, zum vorherigen oder zum letzten Datensatz im Datenraster zu springen.

Mit dem folgenden Code wird die Komponente **RDS.DataControl** definiert:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

Mit dem OBJECT-Tag wird die Komponente **RDS.DataControl** im Programm definiert. Das Tag umfasst zwei Arten von Parametern:

  - Parameter, die dem generischen OBJECT-Tag zugeordnet sind.

  - Parameter, die nur für das **RDS.DataControl** -Objekt gelten.

## <a name="generic-object-tag-parameters"></a>Generische Parameter des OBJECT-Tags

In der folgenden Tabellen werden die Parameter beschrieben, die dem OBJECT-Tag zugeordnet sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parameter</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><em>CLASSID</em></strong></p></td>
<td><p>Eine eindeutige 128-Bit-Nummer, mit der der Typ des eingebetteten Objekts für das System definiert wird. Dieser Bezeichner wird in der Systemregistrierung des lokalen Computers verwaltet. (Informationen zu den Klassen-IDs des <strong>RDS.DataControl</strong>-Objekts finden Sie unter <a href="datacontrol-object-rds.md">RDS.DataControl-Objekt</a>.)</p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>Definiert einen dokumentweiten Bezeichner für das eingebettete Objekt, der verwendet wird, um das Objekt im Code zu identifizieren.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>RDS.DataControl-Tagparameter

In der folgenden Tabelle werden die Parameter beschrieben, die für das **RDS.DataControl** -Objekt gelten. (Eine vollständige Liste der **RDS.DataControl** -Objektparameter und Informationen zu deren Implementierung finden Sie unter [RDS.DataControl-Objekt](datacontrol-object-rds.md).)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parameter</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="server-property-rds.md">SERVER</a></p></td>
<td><p>Wenn Sie HTTP verwenden, ist der Wert der Name des Servercomputers mit https://.</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">EINE VERBINDUNG HERSTELLEN</a></p></td>
<td><p>Bietet die erforderlichen Verbindungsinformationen für <strong>RDS.DataControl</strong>, um eine Verbindung mit SQL Server herzustellen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p>Legt die Abfragezeichenfolge fest oder gibt sie zurück, mit der das <a href="recordset-object-ado.md">Recordset</a>-Objekt abgerufen wird.</p></td>
</tr>
</tbody>
</table>


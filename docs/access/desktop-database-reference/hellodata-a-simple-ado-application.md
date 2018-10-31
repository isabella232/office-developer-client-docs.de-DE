---
title: 'HelloData: Eine einfache ADO-Anwendung'
TOCTitle: 'HelloData: A Simple ADO Application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9e70d611f351cf3ff073a1ad91e359a08e026295
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863297"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: Eine einfache ADO-Anwendung


**Betrifft**: Access 2013 | Office 2013

Als Grundlage für eine Erläuterung der ADO-Bibliothek wird im Folgenden eine einfache ADO-Anwendung mit dem Namen HelloData vorgestellt. HelloData durchläuft die vier wichtigsten ADO-Vorgänge (Abrufen, Überprüfen, Bearbeiten und Aktualisieren von Daten). In dem Beispiel wird eine minimale Fehlerbehandlung ausgeführt, um die ADO-Grundlagen darzustellen und Code-Durcheinander zu vermeiden.

Die Anwendung fragt die Northwind-Beispieldatenbank ab, die mit Microsoft SQL Server 2000 ausgeliefert wird.

**Ausführen von HelloData**

1.  Erstellen Sie ein neues ausführbares Visual Basic-Standardprojekt, das auf die ADO 2.5-Bibliothek verweist.

2.  Erstellen Sie oben auf dem Formular vier Befehlsschaltflächen, indem Sie die Eigenschaften **Name** und **Caption** auf die Werte der folgenden Tabelle festlegen.

3.  Fügen Sie unterhalb der Schaltflächen ein **DataGrid-Steuerelement von Microsoft** (Msdatgrd.ocx). Die Datei Msdatgrd.ocx im Lieferumfang von Visual Basic und befindet sich Ihrer \\Windows\\system32 oder \\Winnt\\Ordner System32. Um Ihre Visual Basic-Bereich Toolbox DataGrid-Steuerelement hinzuzufügen, wählen Sie im Menü **Projekt** **Komponenten...** aus. Aktivieren Sie das Kontrollkästchen neben "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)", und klicken Sie auf **OK**. Um das Steuerelement dem Projekt hinzuzufügen, ziehen Sie das DataGrid-Steuerelement aus der Toolbox auf das Visual Basic-Formular.

4.  Erstellen Sie ein **TextBox** -Objekt auf dem Formular unterhalb des Rasters, und legen Sie seine Eigenschaften auf die in der folgenden Tabelle angegebenen Werte fest. Das Formular sollte bei seiner Fertigstellung ähnlich der folgenden Abbildung aussehen.

5.  Schließlich, kopieren Sie den Code in [HelloData-Code](hellodata-code.md) , und fügen Sie ihn in das Code-Editor-Fenster des Formulars. Drücken Sie **F5**, um den Code auszuführen.


> [!NOTE]
> <P>[!HINWEIS] Im folgenden Beispiel und im gesamten Handbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Außerdem sollten Sie den Wert "MyServer" durch den Namen Ihres Servers ersetzen.</P>



Eine ausführliche Beschreibung des Codes finden Sie unter [Informationen zu HelloData](hellodata-details.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Control Type</p></th>
<th><p>Eigenschaft</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Formular</p></td>
<td><p>Name</p></td>
<td><p>Form1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Height</p></td>
<td><p>6500</p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p>Width</p></td>
<td><p>6500</p></td>
</tr>
<tr class="even">
<td><p>MS DataGrid</p></td>
<td><p>Name</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox-Steuerelement</p></td>
<td><p>Name</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Multiline</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Befehlsschaltfläche</p></td>
<td><p>Name</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Befehlsschaltfläche</p></td>
<td><p>Name</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Examine Data</p></td>
</tr>
<tr class="odd">
<td><p>Befehlsschaltfläche</p></td>
<td><p>Name</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Edit Data</p></td>
</tr>
<tr class="odd">
<td><p>Befehlsschaltfläche</p></td>
<td><p>Name</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Update Data</p></td>
</tr>
</tbody>
</table>




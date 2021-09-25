---
title: 'HelloData: Eine einfache ADO-Anwendung'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63c26ea16f3c93094a877ffb4b9a394b0be89be6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602479"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: Eine einfache ADO-Anwendung

**Gilt für**: Access 2013, Office 2013

To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.

Die Anwendung fragt die Northwind-Beispieldatenbank ab, die mit Microsoft SQL Server 2000 ausgeliefert wird.

**Ausführen von HelloData**

1.  Erstellen Sie ein neues ausführbares Visual Basic-Standardprojekt, das auf die ADO 2.5-Bibliothek verweist.

2.  Erstellen Sie oben auf dem Formular vier Befehlsschaltflächen, indem Sie die Eigenschaften **Name** und **Caption** auf die Werte der folgenden Tabelle festlegen.

3.  Fügen Sie unterhalb der Schaltflächen ein **Microsoft DataGrid-Steuerelement** (Msdatgrd.ocx) hinzu. Die Datei "Msdatgrd.ocx" enthält Visual Basic und befindet sich im \\ Windows \\ System32- oder \\ Winnt-System32-Verzeichnis. \\ Wenn Sie das DataGrid-Steuerelement ihrem Visual Basic Toolboxbereich hinzufügen möchten, wählen Sie im Menü **Project** **komponenten...** aus. Aktivieren Sie dann das Kontrollkästchen neben "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)", und klicken Sie auf **"OK".** Um das Steuerelement dem Projekt hinzuzufügen, ziehen Sie das DataGrid-Steuerelement aus der Toolbox auf das Visual Basic Formular.

4.  Erstellen Sie ein **TextBox** -Objekt auf dem Formular unterhalb des Rasters, und legen Sie seine Eigenschaften auf die in der folgenden Tabelle angegebenen Werte fest. Das Formular sollte bei seiner Fertigstellung ähnlich der folgenden Abbildung aussehen.

5.  Kopieren Sie abschließend den in [HelloData Code](hellodata-code.md) aufgeführten Code, und fügen Sie ihn in das Code-Editor-Fenster des Formulars ein. Drücken Sie **F5**, um den Code auszuführen.

> [!NOTE]
> [!HINWEIS] Im folgenden Beispiel und im gesamten Handbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Außerdem sollten Sie den Wert "MyServer" durch den Namen Ihres Servers ersetzen.

Eine ausführliche Beschreibung des Codes finden Sie unter ["HelloData Details".](hellodata-details.md)

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
<td><p>TextBox</p></td>
<td><p>Name</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Mehrzeiligen</p></td>
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
<td><p>Beschriftung</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Befehlsschaltfläche</p></td>
<td><p>Name</p></td>
<td><p>cmdExthanData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Beschriftung</p></td>
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
<td><p>Beschriftung</p></td>
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
<td><p>Beschriftung</p></td>
<td><p>Update Data</p></td>
</tr>
</tbody>
</table>




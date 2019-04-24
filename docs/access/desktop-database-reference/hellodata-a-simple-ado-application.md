---
title: 'HelloData: Eine einfache ADO-Anwendung'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292020"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: Eine einfache ADO-Anwendung

**Gilt für**: Access 2013, Office 2013

To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.

Die Anwendung fragt die Northwind-Beispieldatenbank ab, die mit Microsoft SQL Server 2000 ausgeliefert wird.

**Ausführen von HelloData**

1.  Erstellen Sie ein neues ausführbares Visual Basic-Standardprojekt, das auf die ADO 2.5-Bibliothek verweist.

2.  Erstellen Sie oben auf dem Formular vier Befehlsschaltflächen, indem Sie die Eigenschaften **Name** und **Caption** auf die Werte der folgenden Tabelle festlegen.

3.  Fügen Sie unterhalb der Schaltflächen ein **Microsoft DataGrid-Steuerelement** (msdatgrd. ocx) hinzu. Die Datei msdatgrd. ocx wird mit Visual Basic geliefert und befindet sich in \\Ihrem\\Windows System32 \\-\\oder winnt system32-Verzeichnis. Zum Hinzufügen des DataGrid-Steuerelements zum Visual Basic-Toolboxbereich wählen Sie im Menü **Projekt** die Option Components.. **.** aus. Aktivieren Sie dann das Kontrollkästchen neben "Microsoft DataGrid-Steuerelement 6,0 (SP3) (OLEDB)", und klicken Sie auf **OK**. Um dem Projekt das Steuerelement hinzuzufügen, ziehen Sie das DataGrid-Steuerelement aus der Toolbox in das Visual Basic-Formular.

4.  Erstellen Sie ein **TextBox** -Objekt auf dem Formular unterhalb des Rasters, und legen Sie seine Eigenschaften auf die in der folgenden Tabelle angegebenen Werte fest. Das Formular sollte bei seiner Fertigstellung ähnlich der folgenden Abbildung aussehen.

5.  Kopieren Sie schließlich den im HelloData- [Code](hellodata-code.md) aufgeführten Code, und fügen Sie ihn in das Code-Editor-Fenster des Formulars ein. Drücken Sie **F5**, um den Code auszuführen.

> [!NOTE]
> [!HINWEIS] Im folgenden Beispiel und im gesamten Handbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Außerdem sollten Sie den Wert "MyServer" durch den Namen Ihres Servers ersetzen.

Eine ausführliche Beschreibung des Codes finden Sie unter [HelloData Details](hellodata-details.md).

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
<td><p>Beschriftung</p></td>
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




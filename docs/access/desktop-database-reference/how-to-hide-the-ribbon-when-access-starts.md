---
title: Ausblenden des Menübands beim Starten von Access
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473315"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Ausblenden des Menübands beim Starten von Access

**Gilt für:** Access 2013 | Office 2013

Standardmäßig stellt Microsoft Access keine Methode zum Ausblenden des Menübands bereit. In diesem Thema wird erläutert, wie Sie ein benutzerdefiniertes Menüband laden, in dem alle integrierten Registerkarten ausgeblendet sind.

Damit beim Start von Access ein benutzerdefiniertes Menüband geladen wird, sollten Sie die Einstellungen für dieses Menüband in einer Tabelle mit der Bezeichnung **USysRibbons** speichern.

Die Tabelle **USysRibbons** muss unter Verwendung bestimmter Spaltennamen erstellt werden, damit die Anpassungen des Menübands implementiert werden. In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Spaltenname</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Text</p></td>
<td><p>Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memo</p></td>
<td><p>Enthält die Menübanderewiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</p></td>
</tr>
</tbody>
</table>


In der folgenden Tabelle werden die Einstellungen zum Anpassen des Menübands aufgelistet, die in der **USysRibbons** -Tabelle gespeichert werden müssen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Spaltenname</p></th>
<th><p>Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>HideTheRibbon</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>&lt;CustomUI Xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;des Menübands StartFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a>Anwenden eines benutzerdefinierten Menübands beim Starten von Access

Wenn Sie ein benutzerdefiniertes Menüband so anwenden möchten, dass es beim Starten der Anwendung zur Verfügung steht, führen Sie folgende Schritte aus:

1.  Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.

2.  Schließen Sie die Anwendung, und starten Sie sie dann neu.

3.  Klicken Sie auf der **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , und klicken Sie dann auf **Access-Optionen**.

4.  Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Name des Menübands**. Wählen Sie **HideTheRibbon** aus.

5.  Schließen Sie die Anwendung, und starten Sie sie neu.

> [!NOTE]
> [!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



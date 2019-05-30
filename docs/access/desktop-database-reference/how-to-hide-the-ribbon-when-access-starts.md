---
title: Ausblenden des Menübands beim Starten von Access
TOCTitle: Hide the ribbon when Access starts
description: Informationen zum Laden eines benutzerdefinierten Menübands, in dem alle integrierten Registerkarten in Access 2013 ausgeblendet sind.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537829"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Ausblenden des Menübands beim Starten von Access

**Gilt für:** Access 2013 | Office 2013

Standardmäßig stellt Microsoft Access keine Methode zum Ausblenden des Menübands bereit. In diesem Thema wird erläutert, wie Sie ein benutzerdefiniertes Menüband laden, in dem alle integrierten Registerkarten ausgeblendet sind.

Damit beim Start von Access ein benutzerdefiniertes Menüband geladen wird, sollten Sie die Einstellungen für dieses Menüband in einer Tabelle mit der Bezeichnung **USysRibbons** speichern.

Die Tabelle **USysRibbons** muss unter Verwendung bestimmter Spaltennamen erstellt werden, damit die Anpassungen des Menübands implementiert werden. 

Die folgende Tabelle enthält die zu verwendenden Einstellungen zum Erstellen der **USysRibbons**-Tabelle.

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
<td><p>Enthält die Menübanderweiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</p></td>
</tr>
</tbody>
</table>

<br/>

In der folgenden Tabelle sind die Einstellungen für die Menübandanpassung aufgeführt, die in der **USysRibbons**-Tabelle gespeichert werden sollen.

|Spaltenname|Wert|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Anwenden eines benutzerdefinierten Menübands beim Starten von Access

Wenn Sie ein benutzerdefiniertes Menüband so anwenden möchten, dass es beim Starten der Anwendung zur Verfügung steht, führen Sie folgende Schritte aus:

1.  Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.

2.  Schließen Sie die Anwendung, und starten Sie sie dann neu.

3.  Klicken Sie auf die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), und wählen Sie dann **Access-Optionen** aus.

4.  Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Menübandname**. Wählen Sie dann **HideTheRibbon** aus.

5.  Schließen Sie die Anwendung, und starten Sie sie neu.

> [!NOTE]
> Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



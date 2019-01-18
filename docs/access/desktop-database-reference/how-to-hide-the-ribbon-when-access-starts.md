---
title: Ausblenden des Menübands beim Starten von Access
TOCTitle: Hide the ribbon when Access starts
description: Wie ein benutzerdefiniertes Menüband geladen, die alle integrierten Registerkarten in Access 2013 ausgeblendet.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4ce9327790f620ba9163f5cdbe7b5c8900de4341
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704105"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Ausblenden des Menübands beim Starten von Access

**Gilt für:** Access 2013 | Office 2013

Standardmäßig stellt Microsoft Access keine Methode zum Ausblenden des Menübands bereit. In diesem Thema wird erläutert, wie Sie ein benutzerdefiniertes Menüband laden, in dem alle integrierten Registerkarten ausgeblendet sind.

Damit beim Start von Access ein benutzerdefiniertes Menüband geladen wird, sollten Sie die Einstellungen für dieses Menüband in einer Tabelle mit der Bezeichnung **USysRibbons** speichern.

Mit bestimmten Spaltennamen für die menübandanpassungen implementiert werden muss die **USysRibbons** -Tabelle erstellt werden. 

In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.

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
<td><p>Enthält die Menüband-Erweiterbarkeits-XML (RibbonX), die die menübandanpassung definiert wird.</p></td>
</tr>
</tbody>
</table>

<br/>

In der folgenden Tabelle werden die Einstellungen zum Anpassen des Menübands aufgelistet, die in der **USysRibbons** -Tabelle gespeichert werden müssen.

|Spaltenname|Wert|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Anwenden einer benutzerdefinierten Multifunktionsleiste beim Starten von Access

Wenn Sie ein benutzerdefiniertes Menüband so anwenden möchten, dass es beim Starten der Anwendung zur Verfügung steht, führen Sie folgende Schritte aus:

1.  Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.

2.  Schließen Sie die Anwendung, und starten Sie sie dann neu.

3.  Wählen Sie die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), und klicken Sie dann auf **Access-Optionen**.

4.  Wählen Sie die Option **Aktuelle Datenbank** und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** wählen Sie in der Liste **Name** des Menübands, und **Klicken**.

5.  Schließen Sie die Anwendung, und starten Sie sie neu.

> [!NOTE]
> [!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



---
title: ImportSharePointList-Makroaktion
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291859"
---
# <a name="importsharepointlist-macro-action"></a>ImportSharePointList-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **ImportierenSharePointListe** -Aktion können Sie Daten von einer Microsoft SharePoint Foundation-Website importieren oder verknüpfen.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ImportierenSharePointListe**-Aktion hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Transfertyp</strong></p></td>
<td><p>Wählen Sie den Übertragungstyp aus.</p>
<ul>
<li><p>Wählen Sie <strong>importieren</strong> aus, um die SharePoint Foundation-Daten in eine Tabelle in Microsoft Access zu kopieren. Aktualisierungen der Daten in Access wirken sich nicht auf die Daten in SharePoint Foundation aus. Entsprechend wirken sich Aktualisierungen an den Daten in SharePoint Foundation nicht auf die Daten in Access aus.</p></li>
<li><p>Wählen Sie <strong>Link</strong> aus, um eine verknüpfte Tabelle in Access zu erstellen, die mit den Daten in SharePoint Foundation verknüpft ist. Aktualisierungen der Daten in Access werden in SharePoint Foundation widergespiegelt. Entsprechend werden Aktualisierungen der Daten in SharePoint Foundation in Access wiedergegeben.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Websiteadresse</strong></p></td>
<td><p>Geben Sie den vollständigen Pfad der SharePoint-Website ein.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Listen-ID</strong></p></td>
<td><p>Geben Sie den Namen oder die GUID der zu übertragenden Liste ein. Erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Sicht-ID</strong></p></td>
<td><p>Geben Sie die GUID der Ansicht für die Liste ein, die Sie verwenden möchten. Lassen Sie das Argument leer, um alle Zeilen und Spalten in der Liste zu übertragen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tabellenname</strong></p></td>
<td><p>Geben Sie den Namen ein, der in Access für die Tabelle oder die verknüpfte Tabelle angezeigt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nachschlageanzeigewerte abrufen</strong></p></td>
<td><p>Wählen Sie <strong>Ja</strong>, um Anzeigewerte für Nachschlagefelder statt der ID zu übertragen, um die Suche durchzuführen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

- Diese Aktion hat den gleichen Effekt wie das Klicken auf **SharePoint-Liste** in der Gruppe **Importieren** auf der Registerkarte **Externe Daten**. Die Argumente für die Aktion entsprechen den Optionen, die Sie im Assistenten für externe Daten auswählen.

- Verwenden Sie die **TransferSharePointList** -Methode des **DoCmd** -Objekts, um die **ImportierenSharePointListe** -Aktion in einem VBA-Modul auszuführen.

- Wenn Sie eine nicht vorhandene Liste oder Ansicht angeben, tritt kein Fehler auf, und es werden keine Daten übertragen.

- Eine GUID ist ein eindeutiger hexadezimaler Bezeichner für eine Liste oder eine Ansicht. Eine GUID muss im folgenden Format eingegeben werden, in dem jedes "F" eine hexadezimale Nummer ist (0 bis 9 oder A bis F).
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  Sie erhalten die GUID für eine Liste oder Ansicht von der SharePoint-Website mithilfe der folgenden Prozedur:
    
  1. Öffnen Sie die Liste in SharePoint Foundation.
    
  2. Wenn die gewünschte Ansicht nicht angezeigt wird, klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann die gewünschte Ansicht.
    
  3. Klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann **Diese Ansicht ändern**.Die Adresse in der Adressleiste des Browsers enthält die GUIDs sowohl für die Liste als auch für die Ansicht. Die GUID für die Liste befolgt **Liste=**, und die GUID für die Ansicht befolgt **Ansicht=**. In der Adresse wird jedoch jedes **{** -Zeichen (linke Klammer) durch die Zeichenfolge **%7B** dargestellt, jeder **-** (Bindestrich) durch die Zeichenfolge **%2D**, und jedes **}** -Zeichen (rechte Klammer) wird durch die Zeichenfolge **%7D** dargestellt. Beispiel:
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  Bevor Sie die GUIDs aus der Adresse als Argumente in dieser Makroaktion verwenden können, müssen Sie jede **% 7B** -Zeichenfolge durch das Zeichen **{** ersetzen, jede **%-2D** - **-** Zeichenfolge durch das Zeichen ersetzen und jede **% 7D** -Zeichenfolge durch die **}** -Zeichen. Fügen Sie nicht das **&** -Zeichen (kaufmännisches Und-Zeichen) ein, das auf die **%7D** -Zeichenfolge in der Listen-GUID folgt.


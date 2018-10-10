---
title: Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475235"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht


**Betrifft**: Access 2013 | Office 2013

Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Laden eines Formulars oder eines Berichts angewendet werden.

## <a name="making-the-ribbon-customization-xml-available"></a>XML für die Menübandanpassung verfügbar machen

**Speichern der Menübanderweiterungs-XML in einer Tabelle**

Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.

**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle. Die Tabelle muss mit bestimmten Spaltennamen erstellt werden, damit die Menübandanpassungen implementiert werden können. In der folgenden Tabelle sind die Einstellungen aufgeführt, die beim Erstellen der **USysRibbons** -Tabelle verwendet werden müssen.

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


**Menübanderweiterungs-XML programmatisch laden**

Mit der **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.

Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.

Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI** -Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>Zuweisen benutzerdefinierter Menübänder zu Formularen oder Berichten

1.  Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.

2.  Öffnen Sie das Formular oder den Bericht in der Entwurfsansicht.

3.  Klicken Sie auf der Registerkarte „Entwurf" auf **Eigenschaftenblatt**.

4.  Klicken Sie auf der Registerkarte **Alle** des Eigenschaftenfensters auf die Liste **Name des Menübands**, und wählen Sie anschließend ein Menüband aus.

5.  Speichern und schließen Sie das Formular oder den Bericht, und öffnen Sie das Formular oder den Bericht dann erneut. Die ausgewählte Menüband-Benutzeroberfläche wird angezeigt.


> [!NOTE]
> [!HINWEIS] Die in der Menüband-Benutzeroberfläche angezeigten Registerkarten sind additiv. D. h., es sei denn, Sie insbesondere die Registerkarten ausblenden oder *von vorne beginnen* -Attribut auf **True**festgelegt, die Registerkarten angezeigt, in einem Formular oder des Berichts Menüband-Benutzeroberfläche sind zusätzlich zu den vorhandenen Registerkarten.

> [!NOTE]
> [!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



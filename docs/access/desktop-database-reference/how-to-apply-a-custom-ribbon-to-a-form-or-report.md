---
title: Anwenden eines benutzerdefinierten Menübands auf ein Formular oder einen Bericht
TOCTitle: Apply a custom ribbon to a form or report
description: Anwenden eines benutzerdefinierten Menübands beim Laden eines Formulars oder Berichts in Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 329f184a1bcd3c856ccfd0b15c3fa92bc6230c98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291915"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Anwenden eines benutzerdefinierten Menübands auf ein Formular oder einen Bericht

**Gilt für**: Access 2013, Office 2013

Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. 

So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Laden eines Formulars oder eines Berichts angewendet werden.

## <a name="make-the-ribbon-customization-xml-available"></a>XML für die Menübandanpassung verfügbar machen

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Speichern der Menübanderweiterungs-XML in einer Tabelle

Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.

**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle. Die Tabelle muss mit bestimmten Spaltennamen erstellt werden, damit die Menübandanpassungen implementiert werden können. 

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


### <a name="load-ribbon-extensibility-xml-programmatically"></a>Menübanderweiterungs-XML programmatisch laden

Mit der **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.

Das XML-Markup kann von einem **Recordset**-Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI**-Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id**-Attribut der Registerkarten des Menübands eindeutig sind.

Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI**-Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.

## <a name="assign-custom-ribbons-to-forms-or-reports"></a>Zuweisen benutzerdefinierter Menübänder zu Formularen oder Berichten

1.  Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.

2.  Öffnen Sie das Formular oder den Bericht in der Entwurfsansicht.

3.  Klicken Sie auf der Registerkarte „Entwurf“ auf **Eigenschaftenblatt**.

4.  Klicken Sie auf der Registerkarte **Alle** des Eigenschaftenfensters auf die Liste **Name des Menübands**, und wählen Sie anschließend ein Menüband aus.

5.  Speichern und schließen Sie das Formular oder den Bericht, und öffnen Sie das Formular oder den Bericht dann erneut. Die ausgewählte Menüband-Benutzeroberfläche wird angezeigt.


> [!NOTE]
> Die in der Menüband-Benutzeroberfläche angezeigten Registerkarten sind additiv. Das heißt, wenn Sie die Registerkarten nicht ausdrücklich ausblenden oder das *Start from Scratch*-Attribut auf **True** festlegen, werden die Registerkarten in der Menüband-Benutzeroberfläche eines Formulars oder Berichts zusätzlich zu den bereits vorhandenen Registerkarten angezeigt.

> [!NOTE]
> Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



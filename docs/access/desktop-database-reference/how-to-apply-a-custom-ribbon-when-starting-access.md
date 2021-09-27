---
title: Anwenden eines benutzerdefinierten Menübands beim Starten von Access
TOCTitle: Apply a custom ribbon when starting Access
description: Anwenden eines benutzerdefinierten Menübands beim Öffnen einer Datenbank in Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: b52d3b261a3655eedd6a6f911d0d1eade31712aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602388"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>Anwenden eines benutzerdefinierten Menübands beim Starten von Access

**Gilt für:** Access 2013 | Office 2013

Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet eine enorme Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Öffnen einer Datenbank angewendet werden.

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

Nach Abschluss der Prozedur, erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI**-Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.

## <a name="apply-customized-ribbons-when-access-starts"></a>Anwenden von angepassten Menübändern beim Starten von Access

Gehen Sie wie folgt vor, um eine benutzerdefiniert Oberfläche anzuwenden, die beim Starten der Anwendung zur Verfügung steht:

1.  Führen Sie den weiter oben beschriebenen Vorgang aus, um der Anwendung die benutzerdefinierten Menübänder verfügbar zu machen.

2.  Schließen Sie die Anwendung, und starten Sie sie neu.

3.  Wählen Sie die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") und dann **Access-Optionen** aus.

4.  Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Menübandname**. Wählen Sie dann ein Menüband aus.

5.  Schließen Sie jetzt die Anwendung, und starten Sie sie neu. Die ausgewählte Benutzeroberfläche wird jetzt angezeigt.

> [!NOTE]
> Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



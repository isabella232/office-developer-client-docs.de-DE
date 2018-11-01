---
title: Anwenden eines benutzerdefinierten Menübands beim Starten von Access
TOCTitle: Apply a custom ribbon when starting Access
description: Informationen zum Anwenden von benutzerdefinierten Menüleisten beim Öffnen einer Datenbank in Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 755ff8c5b8c51927de0b212b91f2a332228f0550
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881300"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>Anwenden eines benutzerdefinierten Menübands beim Starten von Access

**Gilt für:** Access 2013 | Office 2013

Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet eine enorme Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Öffnen einer Datenbank angewendet werden.

## <a name="make-the-ribbon-customization-xml-available"></a>Anpassung der Multifunktionsleiste XML verfügbar machen

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Menüband-Erweiterbarkeits-XML in einer Tabelle speichern

Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.

**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle. Die Tabelle muss mit bestimmten Spaltennamen für die menübandanpassungen implementiert werden erstellt werden. 

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


### <a name="load-ribbon-extensibility-xml-programmatically"></a>Menüband-Erweiterbarkeits-XML programmgesteuert laden

Mit der **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.

Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.

Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise, wenn die Anwendung gestartet wird, wird automatisch die **LoadCustomUI** -Methode ausgeführt, und alle benutzerdefinierten Multifunktionsleisten der Anwendung zur Verfügung gestellt werden.

## <a name="apply-customized-ribbons-when-access-starts"></a>Anwenden Sie benutzerdefinierte Multifunktionsleisten beim Starten von Access

Gehen Sie wie folgt vor, um eine benutzerdefiniert Oberfläche anzuwenden, die beim Starten der Anwendung zur Verfügung steht:

1.  Führen Sie den weiter oben beschriebenen Vorgang aus, um der Anwendung die benutzerdefinierten Menübänder verfügbar zu machen.

2.  Schließen Sie die Anwendung, und starten Sie sie neu.

3.  Wählen Sie die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") und wählen Sie dann auf **Access-Optionen**.

4.  Wählen Sie die Option **Aktuelle Datenbank** und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** wählen Sie in der Liste **Name** des Menübands, und wählen Sie ein Menüband aus.

5.  Schließen Sie jetzt die Anwendung, und starten Sie sie neu. Die ausgewählte Benutzeroberfläche wird jetzt angezeigt.

> [!NOTE]
> [!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).



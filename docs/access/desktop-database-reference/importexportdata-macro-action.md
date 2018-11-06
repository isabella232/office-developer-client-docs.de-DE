---
title: ImportExportData-Makroaktion
TOCTitle: ImportExportData macro action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 363945386233fd992390f1fbc4b6115e272dc923
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997616"
---
# <a name="importexportdata-macro-action"></a>ImportExportData-Makroaktion

**Betrifft**: Access 2013, Office 2013

Verwenden Sie die **ImportierenExportierenDaten** -Aktion zum Importieren oder Exportieren von Daten zwischen der aktuellen Access-Datenbank (MDB oder ACCDB) oder dem aktuellen Access-Projekt (ADP) und anderen Datenbanken. Microsoft Access-Datenbanken lassen auch das Verknüpfen einer Tabelle mit der aktuellen Access-Datenbank aus anderen Datenbanken zu. Bei einer verknüpften Tabelle können Sie auf die Daten der Tabelle zugreifen, während die Tabelle selbst in der anderen Datenbank verbleibt.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="settings"></a>Einstellungen

Die **ImportierenExportierenDaten** -Aktion hat die folgenden Argumente.

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
<td><p>Der Transfertyp, den Sie vornehmen möchten. Wählen Sie <strong>Importieren</strong>, <strong>Exportieren</strong> oder <strong>Verknüpfen</strong> im Feld <strong>Transfertyp</strong> des Abschnitts <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" aus. Die Standardeinstellung ist <strong>Importieren</strong>.  </p><p><strong>Hinweis</strong>: Der Transfertyp <strong>Verknüpfen</strong> wird für Access-Projekte (ADP) nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Datenbanktyp</strong></p></td>
<td><p>Der Typ der Datenbank für den Import, Export oder die Verknüpfung. Sie können im Feld <strong>Datenbankformat</strong> die Option <strong>Microsoft Access</strong> oder eines der verschiedenen anderen Datenbankformate auswählen. Die Standardeinstellung ist <strong>Microsoft Access</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenbankname</strong></p></td>
<td><p>Der Name der Datenbank an, aus der Sie importieren exportieren oder Verknüpfen an. Enthalten Sie den vollständigen Pfad. Dies ist ein erforderliches Argument. Arten von Datenbanken, die verwenden separate Dateien für jede Tabelle, wie FoxPro, Paradox und dBASE, geben Sie in das Verzeichnis mit der Datei. Geben Sie den Dateinamen ein, in das Argument <strong>Source</strong> (zum Importieren oder verknüpfen) oder kein <strong>Destination</strong> -Argument (zum Exportieren). Geben Sie für ODBC-Datenbanken die vollständige Verbindungszeichenfolge Open Database Connectivity (ODBC).</p>
<p>Verknüpfen Sie eine externe Tabelle mit Access, um ein Beispiel für eine Verbindungszeichenfolge anzuzeigen:</p>
<ol>
<li><p>Geben Sie im Dialogfeld <strong>Externe Daten</strong> den Pfad der Quelldatenbank in das Feld <strong>Dateiname</strong> ein.</p></li>
<li><p>Klicken Sie auf <strong>Erstellen Sie eine Verknüpfung zur Datenquelle, indem Sie eine verknüpfte Tabelle erstellen</strong>, und klicken Sie dann auf <strong>OK</strong>.</p></li>
<li><p>Wählen Sie im Dialogfeld <strong>Tabellen verknüpfen</strong> eine Tabelle aus, und klicken Sie auf <strong>OK</strong>.</p></li>
</ol>
<p>Öffnen Sie die neu verknüpfte Tabelle in der Entwurfsansicht. Zeigen Sie die Tabelleneigenschaften an, indem Sie auf der Registerkarte <strong>Entwurf</strong> unter <strong>Tools</strong> auf <strong>Eigenschaftenblatt</strong> klicken. Der Text in der Eigenschafteneinstellung <strong>Beschreibung</strong> ist die Verbindungszeichenfolge für diese Tabelle.</p>
<p>Weitere Informationen zu ODBC-Verbindungszeichenfolgen finden Sie unter der Hilfedatei oder der Dokumentation zum ODBC-Treiber für diese Art von ODBC-Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objekttyp</strong></p></td>
<td><p>Der zu importierende oder exportierende Objekttyp. Wenn Sie <strong>Microsoft Access</strong> für das Argument <strong>Datenbankformat</strong> auswählen, können Sie auswählen <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong> Diagramm</strong>, <strong>Gespeicherte Prozedur</strong>oder <strong>Funktion</strong> im Feld <strong>Objekttyp</strong> . Der Standardwert ist <strong>Tabelle</strong>. Wenn Sie eine andere Art von Datenbank auswählen, oder wenn Sie im Feld <strong>Transfertyp</strong> <strong>Verknüpfen</strong> auswählen, wird dieses Argument ignoriert. Wenn Sie eine select-Abfrage in einer Access-Datenbank exportieren, wählen Sie <strong>Tabelle</strong> in diesem Argument die Ergebnisgruppe der Abfrage zu exportieren, und wählen <strong>Abfrage</strong> die Abfrage selbst zu exportieren. Wenn Sie eine select-Abfrage in einen anderen Typ der Datenbank exportieren, wird dieses Argument wird ignoriert, und die Ergebnisgruppe der Abfrage exportiert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Der Name der zu importierenden, exportierenden oder verknüpfenden Tabelle, der Auswahlabfrage oder des Access-Objekts. Bei einigen Datenbankformaten (z. B. FoxPro, Paradox oder dBASE) handelt es sich hierbei um einen Dateinamen. Schließen Sie die Dateinamenerweiterung (wie DBF) in den Dateinamen ein. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Destination</strong></p></td>
<td><p>Der Name des importierten, exportierten oder verknüpften Tabelle, Auswahlabfrage oder des Access-Objekts in der Zieldatenbank. Bei einigen Datenbanktypen wie FoxPro, Paradox oder dBASE ist dies einen Dateinamen ein. Der Dateiname die Dateinamenerweiterung (beispielsweise .dbf) einschließen. Dies ist ein erforderliches Argument. Wenn Sie <strong>Importieren</strong> für das Argument <strong>Transfertyp</strong> und <strong>Tabelle</strong> für das Argument <strong>Objekttyp</strong> auswählen, wird von Access eine neue Tabelle erstellt, die die Daten der importierten Tabelle enthält. Wenn Sie eine Tabelle oder ein anderes Objekt importieren, fügt Access eine Zahl auf den Namen, wenn es mit einem vorhandenen Namen in Konflikt steht. Wenn beim Importieren und Mitarbeiter bereits vorhanden ist, benennt Access beispielsweise der importierten Tabelle oder ein anderes Objekt Personal1. Beim Exportieren in eine Access-Datenbank oder eine andere Datenbank ersetzt Access automatisch vorhandene Tabellen oder andere Objekte mit demselben Namen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nur Struktur</strong></p></td>
<td><p>Gibt an, ob nur die Struktur einer Datenbanktabelle ohne deren Daten importiert oder exportiert werden soll. Wählen Sie <strong>Ja</strong> oder <strong>Nein</strong> aus. Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können Tabellen zwischen Access und anderen Datenbanktypen importieren und exportieren. Sie können auch Access-Auswahlabfragen in andere Datenbanktypen exportieren. In Access wird das Resultset der Abfrage in Form einer Tabelle exportiert. Sie können jedes beliebige Datenbankobjekt von Access importieren und exportieren, wenn es sich bei beiden Datenbanken um Access-Datenbanken handelt.

Wenn Sie aus einer anderen Access-Datenbank (MDB oder ACCDB) eine in dieser Datenbank verknüpfte Tabelle importieren, bleibt sie nach dem Import verknüpft. Dies bedeutet, dass nur die Verknüpfung importiert wird, nicht die Tabelle.

Erfordert die Datenbank, auf die Sie zugreifen, ein Kennwort, wird beim Ausführen des Makros ein Dialogfeld angezeigt. Geben Sie in dieses Dialogfeld das Kennwort ein.

Die **ImportierenExportierenDaten** -Aktion ist mit den Befehlen auf der Registerkarte **Externe Daten** unter **Importieren** oder **Exportieren** vergleichbar. Verwenden Sie diese Befehle zum Auswählen einer Datenquelle, z. B. einer Access-Datenbank oder eines anderen Datenbankformats, einer Kalkulationstabelle oder einer Textdatei. Beim Auswählen einer Datenbank werden ein oder mehrere Dialogfelder angezeigt. In diesen Dialogfeldern wählen Sie je nach der für den Import, den Export oder die Verknüpfung verwendeten Datenbank den Typ des zu importierenden oder exportierenden Objekts (für Access-Datenbanken), den Namen des Objekts und sonstige Optionen aus. Die Argumente für die **ImportierenExportierenDaten** -Aktion stellen die Optionen in diesen Dialogfeldern dar.

Wenn Sie Indexinformationen für eine verknüpfte dBASE-Tabelle bereitstellen möchte, verknüpfen Sie zuerst die Tabelle:

1.  Klicken Sie auf **dBASE-Datei**.

2.  Geben Sie im Dialogfeld **Externe Daten** im Feld **Dateiname** den Pfad für die dBASE-Datei ein.

3.  Klicken Sie auf **Erstellen Sie eine Verknüpfung zur Datenquelle, indem Sie eine verknüpfte Tabelle erstellen**, und klicken Sie dann auf **OK**.

4.  Geben Sie die Indizes in die Dialogfelder für diesen Befehl ein. Die Indexinformationen werden von Access in einer speziellen Informationsdatei (INF) gespeichert, die sich im Microsoft Office-Ordner befindet.

5.  Die Verknüpfung zur verknüpften Tabelle kann gelöscht werden.

Wenn Sie diese dBASE-Tabelle das nächste Mal mithilfe der **ImportierenExportierenDaten** -Aktion verknüpfen, werden die von Ihnen angegebenen Indexinformationen von Access verwendet.

> [!NOTE]
> [!HINWEIS] Beim Abfragen oder Filtern einer verknüpften Tabelle wird die Groß-/Kleinschreibung beachtet.

Verwenden Sie die **ImportierenExportierenDaten** -Methode des **DoCmd** -Objekts, um die **TransferDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.


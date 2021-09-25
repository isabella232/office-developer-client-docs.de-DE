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
ms.localizationpriority: medium
ms.openlocfilehash: 199da1d702bea1db81443faffaa89d00192c22d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565282"
---
# <a name="importexportdata-macro-action"></a>ImportExportData-Makroaktion

**Gilt für**: Access 2013, Office 2013

Verwenden Sie die **ImportierenExportierenDaten** -Aktion zum Importieren oder Exportieren von Daten zwischen der aktuellen Access-Datenbank (MDB oder ACCDB) oder dem aktuellen Access-Projekt (ADP) und anderen Datenbanken. Microsoft Access-Datenbanken lassen auch das Verknüpfen einer Tabelle mit der aktuellen Access-Datenbank aus anderen Datenbanken zu. Bei einer verknüpften Tabelle können Sie auf die Daten der Tabelle zugreifen, während die Tabelle selbst in der anderen Datenbank verbleibt.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="settings"></a>Einstellungen

Die **ImportierenExportierenDaten**-Aktion hat die folgenden Argumente.

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
<td><p>Der Transfertyp, den Sie vornehmen möchten. Wählen Sie <strong>Importieren</strong>, <strong>Exportieren</strong> oder <strong>Verknüpfen</strong> im Feld <strong>Transfertyp</strong> des Abschnitts <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" aus. Die Standardeinstellung ist <strong>Importieren</strong>.  </p><p><strong>HINWEIS</strong>: Der <strong>Link</strong>-Transfertyp wird für Access-Projekte (ADP) nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Datenbankformat</strong></p></td>
<td><p>Der Typ der Datenbank für den Import, Export oder die Verknüpfung. Sie können im Feld <strong>Datenbankformat</strong> die Option <strong>Microsoft Access</strong> oder eines der verschiedenen anderen Datenbankformate auswählen. Die Standardeinstellung ist <strong>Microsoft Access</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Datenbankname</strong></p></td>
<td><p>Der Name der Datenbank für den Import, Export oder die Verknüpfung. Schließen Sie den vollständigen Pfad ein. Dies ist ein erforderliches Argument. Geben Sie bei Datenbankformaten, bei denen für jede Tabelle gesonderte Dateien verwendet werden (wie FoxPro, Paradox oder dBASE), das Verzeichnis ein, das die Datei enthält. Geben Sie den Dateinamen für das Argument <strong>Quelle</strong> (zum Importieren oder Verknüpfen) oder für das Argument <strong>Ziel</strong> (zum Exportieren) ein. Geben Sie für ODBC-Datenbanken die vollständige ODBC-Verbindungszeichenfolge (Open Database Connectivity) ein.</p>
<p>Verknüpfen Sie eine externe Tabelle mit Access, um ein Beispiel für eine Verbindungszeichenfolge anzuzeigen:</p>
<ol>
<li><p>Geben <strong>Sie</strong> im Dialogfeld Externe Daten abrufen den Pfad der Quelldatenbank in das <strong>Feld "Dateiname"</strong> ein.</p></li>
<li><p>Klicken Sie auf <strong>Erstellen Sie eine Verknüpfung zur Datenquelle, indem Sie eine verknüpfte Tabelle erstellen</strong>, und klicken Sie dann auf <strong>OK</strong>.</p></li>
<li><p>Wählen Sie im Dialogfeld <strong>Tabellen verknüpfen</strong> eine Tabelle aus, und klicken Sie auf <strong>OK</strong>.</p></li>
</ol>
<p>Öffnen Sie die neu verknüpfte Tabelle in der Entwurfsansicht. Zeigen Sie die Tabelleneigenschaften an, indem Sie auf der Registerkarte <strong>Entwurf</strong> unter <strong>Tools</strong> auf <strong>Eigenschaftenblatt</strong> klicken. Der Text in der Eigenschafteneinstellung <strong>Beschreibung</strong> ist die Verbindungszeichenfolge für diese Tabelle.</p>
<p>Weitere Informationen zu ODBC-Verbindungszeichenfolgen finden Sie in der Hilfedatei oder in einer anderen Dokumentation für den ODBC-Treiber dieses ODBC-Datenbanktyps.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objekttyp</strong></p></td>
<td><p>Der Typ des Objekts, das Sie importieren oder exportieren möchten. Wenn Sie <strong>Microsoft Access</strong> für das Argument <strong>Datenbankformat</strong> auswählen, können Sie im Feld <strong>Objekttyp</strong> die Option <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Datenbankdiagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong> auswählen. Die Standardeinstellung ist <strong>Tabelle</strong>. Wenn Sie ein anderes Datenbankformat auswählen oder wenn Sie im Feld <strong>Transfertyp</strong> die Option <strong>Verknüpfen</strong> auswählen, wird dieses Argument ignoriert. Wenn Sie eine Auswahlabfrage in eine Access-Datenbank exportieren, <strong>wählen</strong> Sie Tabelle in diesem Argument aus, um das Resultset der Abfrage zu exportieren, und wählen Sie <strong>Abfrage</strong> aus, um die Abfrage selbst zu exportieren. Wenn Sie eine Auswahlabfrage in einen anderen Datenbanktyp exportieren, wird dieses Argument ignoriert, und das Resultset der Abfrage wird exportiert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Der Name der zu importierenden, exportierenden oder verknüpfenden Tabelle, der Auswahlabfrage oder des Access-Objekts. Bei einigen Datenbankformaten (z. B. FoxPro, Paradox oder dBASE) handelt es sich hierbei um einen Dateinamen. Schließen Sie die Dateinamenerweiterung (wie DBF) in den Dateinamen ein. Dies ist ein erforderliches Argument.</p></td>
</tr>
<tr class="even">
<td><p><strong>Ziel</strong></p></td>
<td><p>Der Name der importierten, exportierten oder verknüpften Tabelle, der Auswahlabfrage oder des Access-Objekts in der Zieldatenbank. Bei einigen Datenbankformaten (z. B. FoxPro, Paradox oder dBASE) handelt es sich hierbei um einen Dateinamen. Schließen Sie die Dateinamenerweiterung (wie DBF) in den Dateinamen ein. Dies ist ein erforderliches Argument. Wenn Sie <strong>Importieren</strong> für das Argument <strong>Transfertyp</strong> und <strong>Tabelle</strong> für das Argument <strong>Objekttyp</strong> auswählen, wird von Access eine neue Tabelle erstellt, die die Daten der importierten Tabelle enthält. Wenn Sie eine Tabelle oder ein anderes Objekt importieren, fügt Access dem Namen eine Zahl hinzu, falls Konflikte mit vorhandenen Namen auftreten. Wenn beispielsweise beim Importieren von Personal der Name "Personal" bereits vorhanden ist, wird die importierte Tabelle oder das andere Objekt von Access in Personal1 umbenannt. Beim Exportieren in eine Access-Datenbank oder eine andere Datenbank ersetzt Access automatisch vorhandene Tabellen oder andere Objekte mit demselben Namen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nur Struktur</strong></p></td>
<td><p>Gibt an, ob nur die Struktur einer Datenbanktabelle ohne deren Daten importiert oder exportiert werden soll. Wählen Sie <strong>Ja</strong> oder <strong>Nein</strong> aus. Die Standardeinstellung ist <strong>Nein</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

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


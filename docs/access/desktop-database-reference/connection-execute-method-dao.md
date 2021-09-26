---
title: Connection.Execute-Methode (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9f4d2159e50c54b6dc448cf2b2963ec05df6ffeb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597588"
---
# <a name="connectionexecute-method-dao"></a>Connection.Execute-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Führt eine Aktionsabfrage oder eine SQL-Anweisung für das angegebene Objekt aus.

## <a name="syntax"></a>Syntax

*Ausdruck* . Execute(***Query** _, _*_Options_**)

*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Query</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ein <strong>String</strong>-Wert, der eine SQL-Anweisung oder den <strong>Name</strong>-Eigenschaftswert eines <strong>QueryDef</strong>-Objekts darstellt.</p></td>
</tr>
<tr class="even">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante oder eine Kombination aus Konstanten, durch die die Datenintegritätsmerkmale der Abfrage festgelegt sind, wie unter Einstellungen festgelegt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die folgenden **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)**-Konstanten für Options verwenden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Verweigert anderen Benutzern die Schreibberechtigung (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Standardeinstellung) Führt inkonsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Führt konsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Führt eine SQL-Pass-Through-Abfrage aus. Wenn Sie diese Option festlegen, wird die SQL-Anweisung zur Verarbeitung an eine ODBC-Datenbank übergeben (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Führt ein Rollback für Updates aus, wenn ein Fehler auftritt (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Führt die Abfrage asynchron aus (nur ODBCDirect-Connection- und -QueryDef-Objekte).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.

> [!NOTE]
> Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können die eine oder die andere, nicht jedoch beide in einer bestimmten Instanz von **OpenRecordset** verwenden. Die gemeinsame Verwendung von **dbConsistent** und **dbInconsistent** verursacht einen Fehler.

Die **Execute** -Methode ist nur für Aktionsabfragen gültig. Wenn Sie die **Execute** -Methode mit einem anderen Abfragetyp verwenden, tritt ein Fehler auf. Da eine Aktionsabfrage keine Datensätze zurückgibt, gibt die **Execute** -Methode keinen **Datensatz** zurück. (Durch Ausführen einer SQL-Pass-Through-Abfrage in einem ODBCDirect-Arbeitsbereich wird kein Fehler zurückgegeben, wenn kein **Datensatz** zurückgegeben wird).

Verwenden Sie die **RecordsAffected** -Eigenschaft des **Connection** -, **Database** - oder **QueryDef** -Objekts, um die Anzahl der von der aktuellsten **Execute** -Methode betroffenen Datensätze zu ermitteln. **RecordsAffected** enthält beispielsweise die Anzahl gelöschter, aktualisierter oder eingefügter Datensätze bei der Ausführung einer Aktionsabfrage. Wenn Sie zum Ausführen einer Abfrage die **Execute** -Methode verwenden, wird bei der **RecordsAffected** -Eigenschaft des **QueryDef** -Objekts die Anzahl der betroffenen Datensätze festgelegt.

Wenn Sie in einem Microsoft Access-Arbeitsbereich eine syntaktisch korrekte SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen, tritt bei der **Execute**-Methode kein Fehler auf, selbst wenn keine einzige Zeile geändert oder gelöscht werden kann. Verwenden Sie daher stets die **dbFailOnError**-Option, wenn Sie eine Update- oder Löschabfrage mit der **Execute** Methode ausführen. Diese Option generiert einen Laufzeitfehler und führt ein Rollback aller erfolgreichen Änderungen durch, wenn einer der betroffenen Datensätze gesperrt ist und nicht aktualisiert oder gelöscht werden kann.

In früheren Versionen des Microsoft Jet-Datenbankmoduls wurden SQL-Anweisungen automatisch in implizite Transaktionen eingebettet. Wenn bei der Ausführung eines Teils einer Anweisung ein **dbFailOnError**-Fehler auftrat, wurde ein Rollback für die gesamte Anweisung durchgeführt. Um die Leistung zu verbessern, wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie älteren DAO-Code aktualisieren, denken Sie daran, explizite Transaktionen um **Execute**-Anweisungen zu verwenden.

Um die beste Leistung in einem Microsoft Access-Arbeitsbereich zu erzielen, insbesondere in einer Mehrbenutzerumgebung, schachteln Sie die **Execute** -Methode innerhalb einer Transaktion. Verwenden Sie die **BeginTrans** -Methode bei dem aktuellen **Workspace** -Objekt, und anschließend die **Execute** -Methode, und vervollständigen Sie die Transaktion mithilfe der **CommitTrans** -Methode im **Arbeitsbereich**. Dadurch werden die Änderungen auf einem Datenträger gespeichert und während der Ausführung der Abfrage eingesetzte Sperren aufgehoben.


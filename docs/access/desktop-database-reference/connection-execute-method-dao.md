---
title: Connection.Execute-Methode (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d95b33531f32ebc3524737c3322c92838518b97f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949537"
---
# <a name="connectionexecute-method-dao"></a>Connection.Execute-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

Führt eine Aktionsabfrage oder eine SQL-Anweisung für das angegebene Objekt aus.

## <a name="syntax"></a>Syntax

*Ausdruck* . Führen Sie (***Abfrage***, ***Optionen***)

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
<th><p>Erforderlich/Optional</p></th>
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
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante oder eine Kombination aus Konstanten, durch die die Datenintegritätsmerkmale der Abfrage festgelegt sind, wie unter Einstellungen festgelegt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die folgenden **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** -Konstanten für Optionen verwenden.

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
<td><p><strong>Bei der Ausführung</strong></p></td>
<td><p>Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.

> [!NOTE]
> [!HINWEIS] Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können eins von beiden, jedoch nicht beide in einer angegebenen Instanz von **OpenRecordset** verwenden. Durch die Verwendung der **dbConsistent** - und **dbInconsistent** -Konstanten wird ein Fehler erzeugt.

Die **Execute**-Methode gilt nur für Aktionsabfragen. Wenn Sie **Execute** mit einem anderen Abfragetyp verwenden, tritt ein Fehler auf. Da bei einer Aktionsabfrage keine Datensätze zurückgegeben werden, gibt **Execute** kein **Recordset**-Objekt zurück. (Das Durchführen einer SQL Pass-Through-Abfrage in einem ODBCDirect-Arbeitsbereich gibt keinen Fehler zurück, wenn kein **Recordset** zurückgegeben wird.)

Mit der **RecordsAffected**-Eigenschaft des **Connection**-, **Database**- oder **QueryDef**-Objekts können Sie die Anzahl von Datensätzen bestimmen, die von der aktuellsten **Execute**-Methode betroffen sind. So umfasst **RecordsAffected** beispielsweise die Anzahl von Datensätzen, die beim Ausführen einer Aktionsabfrage gelöscht, aktualisiert oder eingefügt wurden. Wenn Sie zum Ausführen einer Abfrage die **Execute**-Methode verwenden, ist die **RecordsAffected**-Eigenschaft des **QueryDef**-Objekts auf die Anzahl von betroffenen Datensätzen festgelegt.

Wenn Sie in einem Microsoft Access-Arbeitsbereich eine syntaktisch richtige SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen, schlägt die **Execute**-Methode nicht fehl, auch wenn keine einzelne Zeile geändert oder gelöscht werden kann. Daher sollten Sie immer mit der **dbFailOnError**-Option arbeiten, wenn Sie mit der **Execute**-Methode eine Aktualisierung ausführen oder eine Abfrage löschen. Mit dieser Option wird ein Laufzeitfehler generiert, und für alle erfolgreichen Änderungen wird ein Rollback durchgeführt, wenn einer der betroffenen Datensätze gesperrt ist und nicht aktualisiert oder gelöscht werden kann.

In früheren Versionen des Microsoft Jet-Datenbankmoduls wurden SQL-Anweisungen automatisch in implizite Transaktionen eingebettet. Würde ein Teil einer mit **dbFailOnError** ausgeführten Anweisung fehlschlagen, würde für die Anweisung ein Rollback durchgeführt. Zur Leistungssteigerung wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie älteren DAO-Code aktualisieren, sollten Sie auf jeden Fall explizite Transaktionen bei **Execute**-Anweisungen verwenden.

Die beste Leistung erzielen Sie in einem Microsoft Access-Arbeitsbereich, insbesondere in einer Mehrbenutzerumgebung, indem Sie die **Execute**-Methode in einer Transaktion schachteln. Verwenden Sie die **BeginTrans**-Methode für das aktuelle **Workspace**-Objekt und dann die **Execute**-Methode. Schließen Sie die Transaktion mithilfe der **CommitTrans**-Methode für **Workspace** ab. Damit werden die Änderungen auf einem Datenträger gespeichert, und mögliche Sperren, die beim Ausführen der Abfrage angewendet wurden, werden aufgehoben.


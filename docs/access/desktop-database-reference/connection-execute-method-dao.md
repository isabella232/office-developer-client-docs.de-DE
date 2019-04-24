---
title: Connection. Execute-Methode (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295912"
---
# <a name="connectionexecute-method-dao"></a>Connection. Execute-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Führt eine Aktionsabfrage oder eine SQL-Anweisung zu dem angegebenen Objekt aus.

## <a name="syntax"></a>Syntax

*Ausdruck* . Execute (***Abfrage***, ***Optionen***)

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
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.

> [!NOTE]
> [!HINWEIS] Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können eins von beiden, jedoch nicht beide in einer angegebenen Instanz von **OpenRecordset** verwenden. Durch die Verwendung der **dbConsistent** - und **dbInconsistent** -Konstanten wird ein Fehler erzeugt.

Die **Execute** -Methode ist nur für Aktionsabfragen gültig. Wenn Sie die **Execute** -Methode mit einem anderen Abfragetyp verwenden, tritt ein Fehler auf. Da eine Aktionsabfrage keine Datensätze zurückgibt, gibt die **Execute** -Methode keinen **Datensatz** zurück. (Durch Ausführen einer SQL-Pass-Through-Abfrage in einem ODBCDirect-Arbeitsbereich wird kein Fehler zurückgegeben, wenn kein **Datensatz** zurückgegeben wird).

Verwenden Sie die **RecordsAffected** -Eigenschaft des **Connection** -, **Database** - oder **QueryDef** -Objekts, um die Anzahl der von der aktuellsten **Execute** -Methode betroffenen Datensätze zu ermitteln. **RecordsAffected** enthält beispielsweise die Anzahl gelöschter, aktualisierter oder eingefügter Datensätze bei der Ausführung einer Aktionsabfrage. Wenn Sie zum Ausführen einer Abfrage die **Execute** -Methode verwenden, wird bei der **RecordsAffected** -Eigenschaft des **QueryDef** -Objekts die Anzahl der betroffenen Datensätze festgelegt.

In einem Microsoft Access-Arbeitsbereich erzeugt die **Execute** -Methode keinen Fehler, wenn Sie eine syntaktisch korrekte SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen - sogar dann, wenn keine einzige Zeile bearbeitet oder gelöscht werden kann. Verwenden Sie deshalb immer die **dbFailOnError** -Option, wenn Sie zum Ausführen eines Updates oder zum Löschen einer Abfrage die **Execute** -Methode. Diese Option generiert einen Laufzeitfehler und setzt alle erfolgreichen Änderungen zurück, wenn einer der betroffenen Datensätze gesperrt ist und deshalb nicht aktualisiert oder gelöscht werden kann.

In früheren Versionen des Microsoft Jet-Datenbankmoduls werden SQL-Anweisungen automatisch in implizite Transaktionen integriert. Wenn ein Teil einer Anweisung, die mit **dbFailOnError** ausgeführt wurde, einen Fehler verursacht, würde die gesamte Anweisung zurückgesetzt. Um die Leistung zu verbessern, wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie einen älteren DAO-Code aktualisieren, sollten Sie erwägen, explizite Transaktionen um **Execute** -Anweisungen zu verwenden.

Die beste Leistung erzielen Sie in einem Microsoft Access-Arbeitsbereich, insbesondere in einer Mehrbenutzerumgebung, indem Sie die **Execute**-Methode in einer Transaktion schachteln. Verwenden Sie die **BeginTrans**-Methode für das aktuelle **Workspace**-Objekt und dann die **Execute**-Methode. Schließen Sie die Transaktion mithilfe der **CommitTrans**-Methode für **Workspace** ab. Damit werden die Änderungen auf einem Datenträger gespeichert, und mögliche Sperren, die beim Ausführen der Abfrage angewendet wurden, werden aufgehoben.


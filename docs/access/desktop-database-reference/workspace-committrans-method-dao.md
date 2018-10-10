---
title: Workspace.CommitTrans Method (DAO)
TOCTitle: CommitTrans Method
ms:assetid: e6d129fb-a578-5c79-9c16-6444519f0daf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835985(v=office.15)
ms:contentKeyID: 48548391
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 149727c7f7424a7508edb21bf486e6148cd12295
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472853"
---
# <a name="workspacecommittrans-method-dao"></a>Workspace.CommitTrans Method (DAO)

**Betrifft**: Access 2013 | Office 2013

Beendet die aktuelle Transaktion und speichert die Änderungen.

## <a name="syntax"></a>Syntax

*Ausdruck* . CommitTrans (***Optionen***)

*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<td><p>Option</p></td>
<td><p>Optional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>In einem Microsoft Access-Arbeitsbereich können Sie die <strong>dbForceOSFlush</strong>-Konstante in <strong>CommitTrans</strong> einfügen. Dadurch wird das Datenbankmodul gezwungen, alle Aktualisierungen sofort auf den Datenträger zu leeren, statt sie temporär zu speichern. Ohne diese Option besteht die Gefahr, dass ein Benutzer direkt nach dem Aufrufen von <strong>CommitTrans</strong> durch das Anwendungsprogramm die Kontrolle übernimmt und den Computer ausschaltet, ohne dass die Daten auf einen Datenträger geschrieben wurden. Diese Option kann zwar die Anwendungsleistung beeinträchtigen, ist aber dennoch nützlich in Situationen, in denen der Computer heruntergefahren werden könnte, bevor zwischengespeicherte Aktualisierungen auf einem Datenträger gespeichert wurden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mithilfe der Transaktionsmethoden **BeginTrans**, **CommitTrans** und **Rollback** wird die Transaktionsverarbeitung während einer Sitzung verwaltet, die durch ein **Workspace**-Objekt definiert wurde. Sie verwenden diese Methoden mit einem **Workspace**-Objekt, wenn Sie eine Reihe von an den Datenbanken vorgenommenen Änderungen in einer Sitzung als eine Einheit verarbeiten möchten.

In der Regel verwenden Sie Transaktionen zur Wahrung der Integrität Ihrer Daten, wenn Sie Datensätze in mindestens zwei Tabellen aktualisieren und gleichzeitig sicherstellen müssen, dass die Änderungen in allen Tabellen (Commit) oder in keiner der Tabellen (Rollback) ausgeführt wurden. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren ihn dann zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Verwenden Sie vor dem Aktualisieren des ersten Datensatzes die **BeginTrans**-Methode. Falls nachfolgende Aktualisierungen fehlschlagen, können Sie anschließend mithilfe der **Rollback**-Methode sämtliche Aktualisierungen rückgängig machen. Verwenden Sie die **CommitTrans**-Methode, nachdem Sie den letzten Datensatz erfolgreich aktualisiert haben.

> [!NOTE]
> [!HINWEIS] Innerhalb eines **Workspace**-Objekts sind Transaktionen für **Workspace** immer global und nicht auf ein **Connection**- oder **Database**-Objekt beschränkt. Wenn Sie Operationen für mehrere Verbindungen oder Datenbanken innerhalb einer **Workspace**-Transaktion durchführen, wirkt sich das Auflösen der Transaktion (d. h. die Verwendung der **CommitTrans**- oder **Rollback**-Methode) auf alle Operationen für sämtliche Verbindungen und Datenbanken innerhalb dieses Arbeitsbereichs aus.

Nach Verwendung von **CommitTrans** können Sie an dieser Transaktion vorgenommene Änderungen nur dann rückgängig machen, wenn die Transaktion in einer anderen Transaktion geschachtelt ist, für die ein Rollback ausgeführt wurde. Wenn Sie Transaktionen schachteln, müssen Sie die aktuelle Transaktion auflösen, bevor Sie eine Transaktion auf einer höheren Schachtelungsebene auflösen können.

Wenn Sie gleichzeitige Transaktionen mit überlappenden, nicht geschachtelten Bereichen wünschen, können Sie zusätzliche **Workspace**-Objekte für die gleichzeitigen Transaktionen erstellen.

Wenn Sie ein **Workspace**-Objekt schließen, ohne ausstehende Transaktionen aufzulösen, wird automatisch ein Rollback für die Transaktionen ausgeführt.

Wenn Sie die **CommitTrans**- oder **Rollback**-Methode verwenden, ohne vorher die **BeginTrans**-Methode verwendet zu haben, tritt ein Fehler auf.

Einige ISAM-Datenbanken, die in einem Microsoft Access-Arbeitsbereich verwendet unterstützen möglicherweise keine Transaktionen, in diesem Fall wird die **Transactions** -Eigenschaft des **Database** -Objekt oder **Recordset** -Objekts **False**. Überprüfen Sie den Wert der **Transaktionen** -Eigenschaft des **Database** -Objekts, um sicherzustellen, dass die Datenbank Transaktionen unterstützt, bevor Sie die **BeginTrans** -Methode verwenden. Wenn Sie ein **Recordset** -Objekt basierend auf mehrere Datenbanken verwenden, überprüfen Sie die **Transactions** -Eigenschaft des **Recordset** -Objekts. 

Wenn ein **Recordset** vollständig auf Tabellen des Microsoft Access-Datenbankmoduls basiert, können Sie immer Transaktionen verwenden. **Recordset** -Objekte auf Tabellen, die von anderen Datenbankprodukten erstellt wurde, jedoch basieren, möglicherweise Transaktionen nicht unterstützt. Sie können nicht beispielsweise Transaktionen in einem **Recordset-Objekt** basierend auf einer Paradox-Tabelle verwenden. In diesem Fall wird die **Transactions** -Eigenschaft **False**. Wenn die **Datenbank** oder **Recordset-Objekt** nicht Transaktionen unterstützt, die Methoden werden ignoriert, und tritt kein Fehler auf.

Wenn Sie über das Microsoft Access-Datenbankmodul auf ODBC-Datenquellen zugreifen, können Sie Transaktionen nicht schachteln.

Wenn Sie in ODBC-Arbeitsbereichen **CommitTrans** verwenden, ist der Cursor möglicherweise nicht mehr gültig. Zeigen Sie die Änderungen im **Recordset**-Objekt mithilfe der **Requery**-Methode an, oder schließen Sie das **Recordset**-Objekt, und öffnen Sie es erneut.

> [!NOTE]
> - Die Leistung der Anwendung lässt sich oftmals dadurch verbessern, dass Operationen unterbrochen werden, die Datenträgerzugriff auf Transaktionsblöcke erfordern. So werden die Operationen zwischengespeichert, und die Zugriffe auf den Datenträger können deutlich verringert werden.
> - In einem Microsoft Access-Arbeitsbereich werden Transaktionen in einer Datei protokolliert, die in dem Verzeichnis gespeichert ist, das durch die Umgebungsvariable TEMP auf der Arbeitsstation festgelegt ist. Wenn der Speicherplatz des TEMP-Laufwerks für die Protokolldatei nicht ausreicht, löst das Datenbankmodul einen Laufzeitfehler aus. Wenn Sie nun **CommitTrans** verwenden, wird ein Commit für eine unbestimmte Anzahl von Operationen ausgeführt. Die übrigen Operationen gehen verloren, und die Operation muss neu gestartet werden. Bei Verwendung einer **Rollback**-Methode wird das Transaktionsprotokoll freigegeben, und für sämtliche Operationen in der Transaktion wird ein Rollback ausgeführt.
> - Wenn Sie den Klon eines **Recordset**-Objekts in einer ausstehenden Transaktion schließen, wird eine implizite **Rollback**-Operation verursacht.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird aufgezeigt, wie eine Transaktion in einem Data Access Objects (DAO)-Arbeitsbereich verwendet werden kann.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```

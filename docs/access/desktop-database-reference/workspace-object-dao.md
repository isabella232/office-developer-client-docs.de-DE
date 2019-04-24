---
title: Arbeitsbereichsobjekt (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308358"
---
# <a name="workspace-object-dao"></a>Arbeitsbereichsobjekt (DAO)

**Gilt für**: Access 2013, Office 2013

Ein **Arbeitsbereichs**objekt definiert eine benannte Sitzung für einen Benutzer. Es enthält geöffnete Datenbanken und stellt Mechanismen für gleichzeitige Transaktionen und in Microsoft Access Arbeitsbereiche für den sicheren Arbeitsgruppen-Support bereit.

## <a name="remarks"></a>Bemerkungen

Ein **Arbeitsbereich** ist ein nicht persistentes Objekt, das definiert, wie die Anwendung mit Daten interagiert, indem es das Microsoft Access-Datenbank verwendet. Verwenden Sie ein **Arbeitsbereichs**objekt, um die aktuelle Sitzung zu verwalten oder eine zusätzliche Sitzung zu starten. In einer SItzung können Sie mehrere Datenbanken oder Verbindungen öffnen und Transaktionen verwalten. Sie können beispielsweise folgende Aktionen durchführen:

- Verwenden Sie die **Name**-, **UserName**- und **Type**-Eigenschaften, um eine benannte Sitzung einzurichten. Die Sitzung erstellt einen Bereich, in dem Sie mehrere Datenbanken öffnen und eine Instanz verschachtelter Transaktionen durchführen.

- Verwenden Sie die **Close**-Methode, um eine Sitzung zu beenden.

- Verwenden Sie die **OpenDatabase**-Methode, um eine oder mehrere vorhandene Datenbanken eines **Arbeitsbereichs** zu öffnen.

- Verwenden Sie die **BeginTrans**-, **CommitTrans**- und **Rollback**-methoden, um das Verarbeiten von verschachtelten Transaktionen innerhalb eines **Arbeitsbereichs** und mehrere **Arbeitsbereichs**objekte zum Durchführen mehrerer gleichzeitiger sich überschneidender Transaktionen zu verwenden.

Wenn Sie zunächst auf ein **Arbeitsbereichsobjekt** verweisen oder es verwenden, erstellen Sie automatisch den Standardarbeitsbereich, DBEngine.Workspaces(0). Die Einstellungen für die Eigenschaften **Name** und **UserName** des standardmäßigen Arbeitsbereichs sind „\#Standardarbeitsbereich\#" bzw. „Admin“. Wenn die Sicherheit aktiviert ist, lautet ist die **UserName** -Eigenschaftseinstellung der Name des angemeldeten Benutzers.

Bei der Verwendung von Transaktionen sind alle im **Arbeitsbereich** angegebenen Datenbanken betroffen - sogar wenn mehrere **Datenbank** objekte im **Arbeitsbereich** geöffnet sind. Wenn Sie beispielsweise eine **BeginTrans** -Methode verwenden, aktualisieren Sie mehrere Datensätze in einer Datenbank und löschen Sie anschließend die Datensätze in einer anderen Datenbank. Wenn Sie anschließend die **Rollback** -Methode verwenden, werden die Aktualisierungs- und Löschvorgänge abgebrochen und zurückgesetzt. Sie können zusätzliche **Arbeitsbereichs** objekte erstellen, um Transaktionen unabhängig zwischen **Datenbank** objekten zu verwalten.

Sie können **Arbeitsbereichs**objekte mit der **CreateWorkspace**-Methode erstellen. Nachdem Sie ein neues **Arbeitsbereichs**objekt erstellt haben, müssen Sie es an die **Arbeitsbereichs**auflistung anhängen, wenn Sie aus der **Arbeitsbereichs**auflistung darauf verweisen müssen.

Sie können ein neu erstelltes **Arbeitsbereichs**objekt verwenden, ohne es an die **Arbeitsbereichs**auflistung anhängen zu müssen. Sie müssen jedoch durch die Objektvariable darauf verweisen, der sie es zugewiesen haben.

Um auf ein **Arbeitsbereichs**objekt in einer Auflistung durch die Ordinalzahl oder die **Name**-Eigenschaftseinstellung zu verweisen, verwenden Sie eine der folgenden Syntaxformen:

**DBEngine**.**Arbeitsbereiche**(0)

**DBEngine**.**Arbeitsbereiche**(„name“)

**DBEngine**.**Workspaces**\!\[name\]

> [!NOTE]
> ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.


## <a name="example"></a>Beispiel

In diesem Beispiel wird ein neues Microsoft Access-Arbeitsbereichsobjekt erstellt und an die **Arbeitsbereichs**auflistung angehängt. Anschließend werden die **Arbeitsbereichs**auflistungen und die **Eigenschafts**auflistung des **Arbeitsbereichs**objekts aufgezählt.

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

In diesem Beispiel wird die **CreateWorkspace** -Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Anschließend werden die Eigenschaften des Arbeitsbereichs aufgelistet.

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

Im folgenden Beispiel wird aufgezeigt, wie eine Transaktion in einem Data Access Objects (DAO)-Arbeitsbereich verwendet werden kann.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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

---
title: Database-Objekt (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 265edf6b5d426b87d718c66e9886b7a4877120de
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918849"
---
# <a name="database-object-dao"></a>Database-Objekt (DAO)

**Betrifft**: Access 2013, Office 2013

Ein **Database** -Objekt stellt eine geöffnete Datenbank dar.

## <a name="remarks"></a>Hinweise

Verwenden Sie das **Database** -Objekt und seine Methoden und Eigenschaften zum Bearbeiten einer geöffneten Datenbank. In jeder Art von Datenbank können Sie folgende Aktionen ausführen:

  - Verwenden Sie die **Execute** -Methode, um eine Aktionsabfrage auszuführen.

  - Legen Sie die **Connect** -Eigenschaft fest, um eine Verbindung mit einer ODBC-Datenquelle herzustellen.

  - Legen Sie die **QueryTimeout** -Eigenschaft fest, um die Wartezeit für eine Abfrage, die für eine ODBC-Datenquelle ausgeführt wird, zu beschränken.

  - Verwenden Sie die **RecordsAffected** -Eigenschaft, um zu bestimmen, wie viele Datensätze durch eine Aktionsabfrage geändert wurden.

  - Verwenden Sie die **OpenRecordset** -Methode, um eine Auswahlabfrage auszuführen und ein **Recordset** -Objekt zu erstellen.

  - Verwenden Sie die **Version** -Eigenschaft, um zu bestimmen, mit welcher Version eines Datenbankmoduls die Datenbank erstellt wurde.

Mit einem Microsoft Access-Datenbankmodul können Sie auch andere Methoden, Eigenschaften und Auflistungen verwenden, um ein **Database** -Objekt zu bearbeiten sowie Informationen zu den Tabellen, Abfragen und Beziehungen zu erstellen, zu ändern oder abzurufen. Sie können beispielsweise folgende Aktionen ausführen:

  - Verwenden Sie die Methoden **CreateTableDef** und **CreateRelation** zum Erstellen von Tabellen bzw. Beziehungen.

  - Verwenden Sie die **CreateProperty** -Methode, um neue **Database** -Eigenschaften zu definieren.

  - Verwenden Sie die **CreateQueryDef** -Methode, um eine dauerhafte oder temporäre Abfragedefinition zu erstellen.

  - Verwenden Sie die Methoden **MakeReplica**, **Synchronize** und **PopulatePartial** zum Erstellen und Synchronisieren vollständiger oder teilweiser Replikate Ihrer Datenbank.

  - Legen Sie die **CollatingOrder** -Eigenschaft fest, um die alphabetische Sortierreihenfolge für zeichenbasierte Felder in verschiedenen Sprachen einzurichten.

Verwenden Sie die **CreateDatabase** -Methode, um ein dauerhaftes **Database** -Objekt zu erstellen, das automatisch an die **Databases** -Auflistung angefügt und dadurch auf dem Datenträger gespeichert wird.

Sie müssen das **DBEngine** -Objekt nicht angeben, wenn Sie die **OpenDatabase** -Methode verwenden.

Beim Öffnen einer Datenbank mit verknüpften Tabellen werden nicht automatisch Links zu den angegebenen externen Dateien erstellt. Sie müssen entweder auf die **TableDef** - oder **Field** -Objekte der Tabelle verweisen oder ein **Recordset** -Objekt öffnen. Wenn Sie keine Links zu diesen Tabellen herstellen können, tritt ein abfangbarer Fehler auf. Möglicherweise benötigen Sie auch die Berechtigung zum Zugriff auf die Datenbank, oder ein anderer Benutzer hat die Datenbank im Exklusivmodus geöffnet. In diesen Fällen treten abfangbare Fehler auf.

Nach der Ausführung einer Prozedur, die ein **Database** -Objekt deklariert, werden lokale **Database** -Objekte sowie alle geöffneten **Recordset** -Objekte geschlossen. Ausstehende Aktualisierungen gehen verloren, und für alle ausstehenden Transaktionen wird ein Rollback durchgeführt. Es tritt jedoch kein abfangbarer Fehler auf. Sie sollten explizit alle ausstehenden Transaktionen oder Bearbeitungen abschließen und **Recordset** -Objekte und **Database** -Objekte vor dem Beenden von Verfahren schließen, in denen diese Objektvariablen lokal deklariert werden.

Bei Verwendung einer der Transaktionsmethoden (**BeginTrans**, **CommitTrans** oder **Rollback**) für das **Workspace**-Objekt gelten diese Transaktionen für alle Datenbanken, die in dem **Workspace**-Objekt geöffnet wurden, aus dem das **Database**-Objekt geöffnet wurde. Wenn Sie unabhängige Transaktionen verwenden möchten, müssen Sie zuerst ein zusätzliches **Workspace**-Objekt öffnen und dann ein anderes **Database**-Objekt in diesem **Workspace**-Objekt öffnen.


> [!NOTE]
> [!HINWEIS] Sie können dieselbe Datenquelle oder Datenbank mehrmals öffnen, wodurch Duplikatnamen in der **Databases**-Auflistung erstellt werden. Sie sollten Objektvariablen **Database**-Objekte zuweisen und mit Variablennamen auf sie verweisen.



## <a name="example"></a>Beispiel

In diesem Beispiel wird ein neues **Database** -Objekt erstellt und ein vorhandenes **Database** -Objekt im standardmäßigen **Workspace** -Objekt geöffnet. Dann wird die **Database** -Auflistung und die **Properties** -Auflistung der einzelnen **Database** -Objekte aufgezählt.

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

In diesem Beispiel wird **CreateDatabase** zum Erstellen eines neuen verschlüsselten **Database** -Objekts verwendet.

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```

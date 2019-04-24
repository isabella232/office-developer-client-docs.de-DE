---
title: Datenbankobjekt (DAO)
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
localization_priority: Priority
ms.openlocfilehash: c23772c54f2f980b8d10d4afc352687935840752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294838"
---
# <a name="database-object-dao"></a><span data-ttu-id="6b7ff-102">Datenbankobjekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="6b7ff-102">Database Object (DAO)</span></span>

<span data-ttu-id="6b7ff-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b7ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b7ff-104">Ein **Database**-Objekt stellt eine geöffnete Datenbank dar.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7ff-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b7ff-105">Remarks</span></span>

<span data-ttu-id="6b7ff-p101">Verwenden Sie das **Database**-Objekt und seine Methoden und Eigenschaften zum Bearbeiten einer geöffneten Datenbank. In jeder Art von Datenbank können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p101">You use the **Database** object and its methods and properties to manipulate an open database. In any type of database, you can:</span></span>

  - <span data-ttu-id="6b7ff-108">Verwenden Sie die **Execute**-Methode, um eine Aktionsabfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="6b7ff-109">Legen Sie die **Connect**-Eigenschaft fest, um eine Verbindung mit einer ODBC-Datenquelle herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="6b7ff-110">Legen Sie die **QueryTimeout**-Eigenschaft fest, um die Wartezeit für eine Abfrage, die für eine ODBC-Datenquelle ausgeführt wird, zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="6b7ff-111">Verwenden Sie die **RecordsAffected**-Eigenschaft, um zu bestimmen, wie viele Datensätze durch eine Aktionsabfrage geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="6b7ff-112">Verwenden Sie die **OpenRecordset**-Methode, um eine Auswahlabfrage auszuführen und ein **Recordset**-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="6b7ff-113">Verwenden Sie die **Version**-Eigenschaft, um zu bestimmen, mit welcher Version eines Datenbankmoduls die Datenbank erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="6b7ff-p102">Mit einem Microsoft Access-Datenbankmodul können Sie auch andere Methoden, Eigenschaften und Auflistungen verwenden, um ein **Database**-Objekt zu bearbeiten sowie Informationen zu den Tabellen, Abfragen und Beziehungen zu erstellen, zu ändern oder abzurufen. Sie können beispielsweise folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p102">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships. For example, you can:</span></span>

  - <span data-ttu-id="6b7ff-116">Verwenden Sie die Methoden **CreateTableDef** und **CreateRelation** zum Erstellen von Tabellen bzw. Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="6b7ff-117">Verwenden Sie die **CreateProperty**-Methode, um neue **Database**-Eigenschaften zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="6b7ff-118">Verwenden Sie die **CreateQueryDef**-Methode, um eine dauerhafte oder temporäre Abfragedefinition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="6b7ff-119">Verwenden Sie die Methoden **MakeReplica**, **Synchronize** und **PopulatePartial** zum Erstellen und Synchronisieren vollständiger oder teilweiser Replikate Ihrer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="6b7ff-120">Legen Sie die **CollatingOrder**-Eigenschaft fest, um die alphabetische Sortierreihenfolge für zeichenbasierte Felder in verschiedenen Sprachen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="6b7ff-121">Verwenden Sie die **CreateDatabase**-Methode, um ein dauerhaftes **Database**-Objekt zu erstellen, das automatisch an die **Databases**-Auflistung angefügt und dadurch auf dem Datenträger gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="6b7ff-122">Sie müssen das **DBEngine**-Objekt nicht angeben, wenn Sie die **OpenDatabase**-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="6b7ff-p103">Beim Öffnen einer Datenbank mit verknüpften Tabellen werden nicht automatisch Links zu den angegebenen externen Dateien erstellt. Sie müssen entweder auf die **TableDef**- oder **Field**-Objekte der Tabelle verweisen oder ein **Recordset**-Objekt öffnen. Wenn Sie keine Links zu diesen Tabellen herstellen können, tritt ein abfangbarer Fehler auf. Möglicherweise benötigen Sie auch die Berechtigung zum Zugriff auf die Datenbank, oder ein anderer Benutzer hat die Datenbank im Exklusivmodus geöffnet. In diesen Fällen treten abfangbare Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p103">Opening a database with linked tables doesn't automatically establish links to the specified external files. You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object. If you can't establish links to these tables, a trappable error occurs. You may also need permission to access the database, or another user might have the database opened exclusively. In these cases, trappable errors occur.</span></span>

<span data-ttu-id="6b7ff-p104">Nach der Ausführung einer Prozedur, die ein **Database**-Objekt deklariert, werden lokale **Database**-Objekte sowie alle geöffneten **Recordset**-Objekte geschlossen. Ausstehende Aktualisierungen gehen verloren, und für alle ausstehenden Transaktionen wird ein Rollback durchgeführt. Es tritt jedoch kein abfangbarer Fehler auf. Sie sollten explizit alle ausstehenden Transaktionen oder Bearbeitungen abschließen und **Recordset**-Objekte und **Database**-Objekte vor dem Beenden von Verfahren schließen, in denen diese Objektvariablen lokal deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p104">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects. Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs. You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="6b7ff-p105">Bei Verwendung einer der Transaktionsmethoden (**BeginTrans**, **CommitTrans** oder **Rollback**) für das **Workspace**-Objekt gelten diese Transaktionen für alle Datenbanken, die in dem **Workspace**-Objekt geöffnet wurden, aus dem das **Database**-Objekt geöffnet wurde. Wenn Sie unabhängige Transaktionen verwenden möchten, müssen Sie zuerst ein zusätzliches **Workspace**-Objekt öffnen und dann ein anderes **Database**-Objekt in diesem **Workspace**-Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p105">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened. If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="6b7ff-p106">Sie können die gleiche Datenquelle oder Datenbank mehrmals öffnen, indem Sie doppelte Namen in der **Databases**-Auflistung erstellen. Sie sollten **Database**-Objekte zu Objektvariablen zuweisen und mit Variablennamen darauf verweisen.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p106">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="6b7ff-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6b7ff-135">Example</span></span>

<span data-ttu-id="6b7ff-p107">In diesem Beispiel wird ein neues **Database**-Objekt erstellt und ein vorhandenes **Database**-Objekt im standardmäßigen **Workspace**-Objekt geöffnet. Dann wird die **Database**-Auflistung und die **Properties**-Auflistung der einzelnen **Database**-Objekte aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-p107">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

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

<span data-ttu-id="6b7ff-138">In diesem Beispiel wird **CreateDatabase** zum Erstellen eines neuen verschlüsselten **Database**-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b7ff-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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

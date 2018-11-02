---
title: Recordset-Objekt (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4ce9b3480cfa2a8eb074065016131e2c82752c3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921129"
---
# <a name="recordset-object-dao"></a><span data-ttu-id="b26b2-102">Recordset-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="b26b2-102">Recordset object (DAO)</span></span>

<span data-ttu-id="b26b2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b26b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b26b2-104">Ein **Recordset** -Objekt stellt die Datensätze in einer Basistabelle oder die Datensätze dar, die aus einer Abfrageausführung resultieren.</span><span class="sxs-lookup"><span data-stu-id="b26b2-104">A **Recordset** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="b26b2-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b26b2-105">Remarks</span></span>

<span data-ttu-id="b26b2-p101">Sie verwenden **Recordset** -Objekte, um Daten in einer Datenbank auf Datensatzebene zu ändern. Wenn Sie DAO-Objekte verwenden, ändern Sie Daten fast ausschließlich mit **Recordset** -Objekten. Alle **Recordset** -Objekte werden mit Datensätzen (Zeilen) und Feldern (Spalten) erstellt. Es gibt von Typen von **Recordset** -Objekten:</span><span class="sxs-lookup"><span data-stu-id="b26b2-p101">You use **Recordset** objects to manipulate data in a database at the record level. When you use DAO objects, you manipulate data almost entirely using **Recordset** objects. All **Recordset** objects are constructed using records (rows) and fields (columns). There are five types of **Recordset** objects:</span></span>

- <span data-ttu-id="b26b2-110">Tabellentyp-Recordset: Darstellung im Code einer Basistabelle, den Sie verwenden können, um Datensätze in einer einzelnen Datenbanktabelle hinzuzufügen, zu ändern oder zu löschen (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b26b2-110">Table-type Recordset— representation in code of a base table that you can use to add, change, or delete records from a single database table (Microsoft Access workspaces only).</span></span>

- <span data-ttu-id="b26b2-p102">Recordset vom "dynaset"-Typ: das Ergebnis einer Abfrage, die aktualisierbare Datensätze haben kann. Ein **Recordset** -Objekt vom "dynaset"-Typ ist eine dynamische Gruppe mit Datensätzen, die Sie verwenden können, um Datensätze aus einer zugrunde liegenden Tabelle oder zugrunde liegenden Tabellen hinzuzufügen, zu ändern oder zu löschen. Ein **Recordset** -Objekt vom "dynaset"-Typ kann Felder aus mindestens einer Tabelle in einer Datenbank enthalten. Der Typ entspricht einem ODBC-Keysetcursor.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p102">Dynaset-type Recordset— the result of a query that can have updatable records. A dynaset-type **Recordset** object is a dynamic set of records that you can use to add, change, or delete records from an underlying database table or tables. A dynaset-type **Recordset** object can contain fields from one or more tables in a database. This type corresponds to an ODBC keyset cursor.</span></span>

- <span data-ttu-id="b26b2-p103">Recordset vom "snapshot"-Typ: eine statische Kopie einer Datensatzgruppe, die Sie verwenden können, um Daten zu suchen oder Berichte zu generieren. Ein **Recordset** -Objekt vom "snapshot"-Typ kann Felder aus mindestens einer Tabelle in einer Datenbank enthalten, kann aber nicht aktualisiert werden. Dieser Typ entspricht einem statischen ODBC-Cursor.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p103">Snapshot-type Recordset— a static copy of a set of records that you can use to find data or generate reports. A snapshot-type **Recordset** object can contain fields from one or more tables in a database but can't be updated. This type corresponds to an ODBC static cursor.</span></span>

- <span data-ttu-id="b26b2-p104">Recordset vom "forward-only"-Typ: identnisch zum "snapshot"-Typ mit der Ausnahme, dass kein Cursor bereitgestellt wird. Sie können nur vorwärts durch Datensätze blättern. Auf diese Weise wird die Leistung in Situationen verbessert, in denen Sie ein Resultset lediglich einmal durchlaufen müssen. Dieser Typ entspricht einem ODBC-Cursor vom "forward-only"-Typ.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p104">Forward-only-type Recordset— identical to a snapshot except that no cursor is provided. You can only scroll forward through records. This improves performance in situations where you only need to make a single pass through a result set. This type corresponds to an ODBC forward-only cursor.</span></span>

- <span data-ttu-id="b26b2-p105">Recordset vom "dynamic"-Typ: eine Abfragergebnisgruppe aus mindestens einer Basistabelle, in der Sie Datensätze einer Abfrage, die Zeilen zurückgibt, hinzufügen, ändern oder löschen können. Außerdem werden Datensätze, die andere Benutzer in den Basistabellen hinzufügen, löschen oder bearbeiten, ebenfalls im **Recordset** angezeigt. Dieser Typ entspricht einem dynamischen ODBC-Cursor (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b26b2-p105">Dynamic-type Recordset— a query result set from one or more base tables in which you can add, change, or delete records from a row-returning query. Further, records other users add, delete, or edit in the base tables also appear in your **Recordset**. This type corresponds to an ODBC dynamic cursor (ODBCDirect workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="b26b2-p106">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="b26b2-127">Sie können den Typ des **Recordset** -Objekts auswählen, den, die Sie mit dem Argument Type der **OpenRecordset** -Methode erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b26b2-127">You can choose the type of **Recordset** object you want to create using the type argument of the **OpenRecordset** method.</span></span>

<span data-ttu-id="b26b2-128">In Microsoft Access-Arbeitsbereich Wenn Sie nicht, dass ein DAO Versuche zum Erstellen des Typs des **Recordset-Objekts** mit der meisten Funktionen zur Verfügung angeben, beginnend mit Table.</span><span class="sxs-lookup"><span data-stu-id="b26b2-128">In a Microsoft Access workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the most functionality available, starting with table.</span></span> <span data-ttu-id="b26b2-129">Falls dieser Typ nicht verfügbar ist, probiert DAO ein "dynaset"-, dann ein "snapshot"- und schließlich ein "forward-only"- **Recordset** -Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="b26b2-129">If this type isn't available, DAO attempts a dynaset, then a snapshot, and finally a forward-only type **Recordset** object.</span></span>

<span data-ttu-id="b26b2-130">In einem ODBCDirect-Arbeitsbereich Wenn Sie einen Typ nicht angeben versucht DAO den Typ des **Recordset-Objekts** mit die schnellstmögliche Antwortzeit für die Abfrage erstellen beginnend mit Vorwärtscursor.</span><span class="sxs-lookup"><span data-stu-id="b26b2-130">In an ODBCDirect workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the fastest query response, starting with forward-only.</span></span> <span data-ttu-id="b26b2-131">Falls dieser Typ nicht verfügbar ist, probiert DAO ein "snapshot"-, dann ein "dynaset"- und schließlich ein "dynamic"- **Recordset** -Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="b26b2-131">If this type isn't available, DAO attempts a snapshot, then a dynaset, and finally a dynamic- type **Recordset** object.</span></span>

<span data-ttu-id="b26b2-p109">Wenn Sie ein **Recordset** -Objekt mit einem nicht verknüpften **[TableDef](tabledef-object-dao.md)** -Objekt in einem Microsoft Access-Arbeitsbereich erstellen, werden **Recordset** -Objekte vom "table"-Typ erstellt. Nur **Recordset** -Objekte vom "dynaset"- oder "snapshot"-Typ können mit verknüpften Tabellen oder Tabellen in ODBC-Datenbanken mit verbundenem Microsoft Access-Datenbankmodul erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p109">When creating a **Recordset** object using a non-linked **[TableDef](tabledef-object-dao.md)** object in a Microsoft Access workspace, table-type **Recordset** objects are created. Only dynaset-type or snapshot-type **Recordset** objects can be created with linked tables or tables in Microsoft Access database engine-connected ODBC databases.</span></span>

<span data-ttu-id="b26b2-134">Ein neues **Recordset** -Objekt wird automatisch der **Recordsets** -Auflistung hinzugefügt, wenn Sie das Objekt öffnen, und wird automatisch entfernt, wenn Sie das Objekt schließen.</span><span class="sxs-lookup"><span data-stu-id="b26b2-134">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the object, and is automatically removed when you close it.</span></span>

> [!NOTE]
> <span data-ttu-id="b26b2-p110">[!HINWEIS] Wenn Sie Variablen verwenden, um ein **Recordset** -Objekt darzustellen, und das **Database** -Objekt das **Recordset** enthält, stellen Sie sicher, dass die Variablen den gleichen Umfang bzw. die gleiche Lebenszeit aufweisen. Wenn Sie beispielsweise eine öffentliche Variable deklarieren, die ein **Recordset** -Objekt darstellt, stellen Sie sicher, dass die Variable, die das **Database** -Objekt mit dem **Recordset** enthält, ebenfalls öffentlich ist oder in einer **Sub** - oder **Function** -Prozedur mit dem **Static** -Schlüsselwort deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p110">If you use variables to represent a **Recordset** object and the **Database** object that contains the **Recordset**, make sure the variables have the same scope, or lifetime. For example, if you declare a public variable that represents a **Recordset** object, make sure the variable that represents the **Database** containing the **Recordset** is also public, or is declared in a **Sub** or **Function** procedure using the **Static** keyword.</span></span>

<span data-ttu-id="b26b2-p111">Sie können beliebig viele **Recordset** -Objektvariablen erstellen. Unterschiedliche **Recordset** -Objekte können auf die gleichen Tabellen, Abfragen und Felder ohne Konflikte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p111">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="b26b2-139">Dynaset, Snapshot und Weiterleiten Typ **Recordset** -Objekte werden im lokalen Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b26b2-139">Dynaset–, snapshot–, and forward–only–type **Recordset** objects are stored in local memory.</span></span> <span data-ttu-id="b26b2-140">Wenn zum Speichern dieser Daten im lokalen Arbeitsspeicher nicht genug Platz verfügbar ist, speichert das Microsoft Access-Datenbankmodul die zusätzlichen Daten in das Festplattenverzeichnis TEMP.</span><span class="sxs-lookup"><span data-stu-id="b26b2-140">If there isn't enough space in local memory to store the data, the Microsoft Access database engine saves the additional data to TEMP disk space.</span></span> <span data-ttu-id="b26b2-141">Wenn dieser Platz aufgebraucht ist, tritt ein verfolgbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b26b2-141">If this space is exhausted, a trappable error occurs.</span></span>

<span data-ttu-id="b26b2-p113">Die Standardauflistung eines **Recordset** -Objekts ist die **Fields** -Auflistung und die Standardeigenschaft eines **[Field](field-object-dao.md)** -Objekts ist die **[Value](field-value-property-dao.md)** -Eigenschaft. Verwenden Sie diese Standardeinstellungen, um Ihren Code zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p113">The default collection of a **Recordset** object is the **Fields** collection, and the default property of a **[Field](field-object-dao.md)** object is the **[Value](field-value-property-dao.md)** property. Use these defaults to simplify your code.</span></span>

<span data-ttu-id="b26b2-p114">Wenn Sie ein **Recordset** -Objekt erstellen, wird der aktuelle Datensatz als erster Datensatz positioniert, falls Datensätze vorhanden sind. Falls keine Datensätze vorhanden sind, lautet die Einstellung der **RecordCount** -Eigenschaft "0", und die Einstellungen der **BOF** - und **EOF** -Eigenschaften sind **True**.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p114">When you create a **Recordset** object, the current record is positioned to the first record if there are any records. If there are no records, the **RecordCount** property setting is 0, and the **BOF** and **EOF** property settings are **True**.</span></span>

<span data-ttu-id="b26b2-p115">Sie können die Methoden **MoveNext**, **MovePrevious**, **MoveFirst** und **MoveLast** verwenden, um den aktuellen Datensatz neu zu positionieren. "Forward-only"-**Recordset**-Objekte unterstützen nur die **MoveNext**-Methode. Wenn Sie die Move-Methoden verwenden, um die einzelnen Datensätze aufzurufen (oder das **Recordset** "durchlaufen"), können Sie die **BOF**- und **EOF**-Eigenschaften verwenden, um nach dem Anfang oder Ende des **Recordset**-Objekts zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p115">You can use the **MoveNext**, **MovePrevious**, **MoveFirst**, and **MoveLast** methods to reposition the current record. Forward–only–type **Recordset** objects support only the **MoveNext** method. When using the Move methods to visit each record (or "walk" through the **Recordset**), you can use the **BOF** and **EOF** properties to check for the beginning or end of the **Recordset** object.</span></span>

<span data-ttu-id="b26b2-p116">Mit "dynaset"- und "snapshot"- **Recordset** -Objekten in einem Microsoft Access-Arbeitsbereich können Sie auch die Find-Methoden verwenden, zum Beispiel **FindFirst**, um einen bestimmten Datensatz basierend auf Kriterien zu suchen. Falls der Datensatz nicht gefunden wird, wird die **NoMatch** -Eigenschaft auf **True** festgelegt. Für **Recordset** -Objekte vom "table"-Typ können Sie Datensätze mithilfe der **Seek** -Methode suchen.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p116">With dynaset- and snapshot-type **Recordset** objects in a Microsoft Access workspace, you can also use the Find methods, such as **FindFirst**, to locate a specific record based on criteria. If the record isn't found, the **NoMatch** property is set to **True**. For table-type **Recordset** objects, you can scan records using the **Seek** method.</span></span>

<span data-ttu-id="b26b2-152">Die **Type** -Eigenschaft gibt den Typ des erstellten **Recordset** -Objekts an und die **Updatable** -Eigenschaft gibt an, ob Sie die Datensätze des Objekts ändern können.</span><span class="sxs-lookup"><span data-stu-id="b26b2-152">The **Type** property indicates the type of **Recordset** object created, and the **Updatable** property indicates whether you can change the object's records.</span></span>

<span data-ttu-id="b26b2-153">Informationen zur Struktur einer Basistabelle, zum Beispiel zu den Namen und Datentypen der einzelnen **Field** -Objekte und **Index** -Objekte, werden in einem **TableDef** -Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b26b2-153">Information about the structure of a base table, such as the names and data types of each **Field** object and any **Index** objects, is stored in a **TableDef** object.</span></span>

<span data-ttu-id="b26b2-154">Wenn Sie auf ein **Recordset**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="b26b2-154">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="b26b2-155">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="b26b2-155">**Recordsets**(0)</span></span>

- <span data-ttu-id="b26b2-156">**Recordset-Objekte** ("Name")</span><span class="sxs-lookup"><span data-stu-id="b26b2-156">**Recordsets**("name")</span></span>

- <span data-ttu-id="b26b2-157">**Recordsets**\!\[Namen\]</span><span class="sxs-lookup"><span data-stu-id="b26b2-157">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="b26b2-p117">[!HINWEIS] Sie können ein **Recordset**-Objekt derselben Datenquelle oder Datenbank mehrmals öffnen und dabei doppelte Namen in der **Recordsets**-Auflistung erstellen. Sie sollten Objektvariablen **Recordset**-Objekte zuweisen und mit Variablennamen auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p117">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="b26b2-160">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b26b2-160">Example</span></span>

<span data-ttu-id="b26b2-161">Dieses Beispiel demonstriert **Recordset** -Objekte und die **Recordsets** -Auflistung durch Öffnen von vier verschiedenen **Recordsets**, Aufzählen der Recordsets-Auflistung des aktuellen **Database** -Objekts und Aufzählen der **Properties** -Auflistung jedes **Recordset** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b26b2-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="b26b2-p118">Dieses Beispiel verwendet die **OpenRecordset** -Methode, um fünf verschiedene **Recordset** -Objekte zu öffnen und ihre Inhalte anzuzeigen. Die OpenRecordsetOutput-Prozedur ist für die Ausführung dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b26b2-p118">This example uses the **OpenRecordset** method to open five different **Recordset** objects and display their contents. The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="b26b2-164">Dieses Beispiel öffnet ein **Recordset** -Objekt vom "dynamic"-Typ und zählt seine Datensätze auf.</span><span class="sxs-lookup"><span data-stu-id="b26b2-164">This example opens a dynamic-type **Recordset** object and enumerates its records.</span></span>

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="b26b2-165">Dieses Beispiel öffnet ein **Recordset** vom "dynaset"-Typ und zeigt den Umfang, in dem die Felder aktualisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="b26b2-165">This example opens a dynaset-type **Recordset** and shows the extent to which its fields are updatable.</span></span>

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="b26b2-166">Dieses Beispiel öffnet ein **Recordset** vom "forward-only"-Typ, demonstriert die schreibgeschützten Merkmale und durchläuft das **Recordset** mit der **MoveNext** -Methode.</span><span class="sxs-lookup"><span data-stu-id="b26b2-166">This example opens a forward-only-type **Recordset**, demonstrates its read-only characteristics, and steps through the **Recordset** with the **MoveNext** method.</span></span>

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="b26b2-167">Dieses Beispiel öffnet ein **Recordset** vom "snapshot"-Typ und demonstriert die schreibgeschützten Merkmale.</span><span class="sxs-lookup"><span data-stu-id="b26b2-167">This example opens a snapshot-type **Recordset** and demonstrates its read-only characteristics.</span></span>

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="b26b2-168">Dieses Beispiel öffnet ein **Recordset** vom "table"-Typ, legt die **Index** -Eigenschaft fest und zählt die Datensätze auf.</span><span class="sxs-lookup"><span data-stu-id="b26b2-168">This example opens a table-type **Recordset**, sets its **Index** property, and enumerates its records.</span></span>

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="b26b2-169">Das folgende Beispiel zeigt das Verwenden der Seek-Methode zum Suchen eines Datensatzes in einer verknüpften Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b26b2-169">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="b26b2-170">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b26b2-170">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

<br/>

<span data-ttu-id="b26b2-171">The following example shows how to open a Recordset that is based on a parameter query.</span><span class="sxs-lookup"><span data-stu-id="b26b2-171">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="b26b2-172">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Tabelle oder Abfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="b26b2-172">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="b26b2-173">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer SQL-Anweisung (Structured Query Language) basiert.</span><span class="sxs-lookup"><span data-stu-id="b26b2-173">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="b26b2-174">Das folgende Beispiel zeigt das Verwenden der FindFirst- und FindNext-Methoden zum Suchen eines Datensatzes in einem Recordset.</span><span class="sxs-lookup"><span data-stu-id="b26b2-174">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="b26b2-175">Das folgende Beispiel zeigt das Kopieren der Ergebnisse einer Abfrage in ein Arbeitsblatt in einer neuen Microsoft Excel-Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="b26b2-175">The following example shows how to copy the results of a query to a worksheet in a new Microsoft Excel workbook.</span></span>

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```


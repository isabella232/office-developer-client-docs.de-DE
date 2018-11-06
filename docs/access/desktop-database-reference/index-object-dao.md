---
title: Index-Objekt - Data Access Objects (DAO)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6646a3121bc353c8e8d74e3698ae688272656769
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997399"
---
# <a name="index-object-dao"></a><span data-ttu-id="e9386-102">Index-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9386-102">Index object (DAO)</span></span>

<span data-ttu-id="e9386-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9386-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9386-p101">**Index**-Objekte geben die Reihenfolge an, in der auf Datensätze aus Datenbanktabellen zugegriffen wird, und sie geben an, ob doppelte Datensätze akzeptiert werden. Dadurch stellen sie einen effizienten Zugriff auf Daten sicher. Bei externen Datenbanken beschreiben **Index**-Objekte die für externe Tabellen eingerichteten Indizes (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="e9386-p101">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9386-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9386-106">Remarks</span></span>

<span data-ttu-id="e9386-p102">Im Microsoft Access-Datenbankmodul werden beim Verknüpfen von Tabellen und Erstellen von Recordset-Objekten Indizes verwendet. Indizes bestimmen die Reihenfolge, in der Recordset-Objekte vom Typ Tabelle Objekte zurückgeben, sie bestimmen jedoch nicht die Reihenfolge, in der Datensätze in der Basistabelle im Microsoft Access-Datenbankmodul gespeichert werden, oder die Reihenfolge, in der ein anderer Typ von Recordset-Objekten Datensätze zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e9386-p102">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects. Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="e9386-109">Bei einem **Index**-Objekt können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="e9386-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="e9386-110">Bestimmen Sie mit der **Required**-Eigenschaft, ob die **[Field](field-object-dao.md)** -Objekte im Index Werte erfordern, die nicht Null sind, und bestimmen Sie dann mit der **IgnoreNulls**-Eigenschaft, ob die Nullwerte Indexeinträge besitzen.</span><span class="sxs-lookup"><span data-stu-id="e9386-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="e9386-111">Bestimmen Sie mit den Eigenschaften **Primary** und **Unique** die Sortierung und Eindeutigkeit des **Index**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e9386-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="e9386-p103">Das Microsoft Access-Datenbankmodul verwaltet alle Indizes von Basistabellen automatisch. Bei jedem Hinzufügen, Ändern oder Löschen von Datensätzen in der Basistabelle werden die Indizes aktualisiert. Nachdem Sie die Datenbank erstellt haben, bringen Sie die Indexstatistiken mit der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode regelmäßig auf den neuesten Stand.</span><span class="sxs-lookup"><span data-stu-id="e9386-p103">The Microsoft Access database engine maintains all base table indexes automatically. It updates indexes whenever you add, change, or delete records from the base table. Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="e9386-p104">Wenn Sie auf ein Recordset-Objekt vom Typ Tabelle zugreifen, geben Sie mit der Index-Eigenschaft des Objekts die Reihenfolge der Datensätze an. Legen Sie diese Eigenschaft auf die Einstellung der Name-Eigenschaft eines vorhandenen Index-Objekts in der Indexes-Auflistung fest. Diese Auflistung ist im TableDef-Objekt enthalten, das dem zu füllenden Recordset-Objekt zugrunde liegt.</span><span class="sxs-lookup"><span data-stu-id="e9386-p104">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection. This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <span data-ttu-id="e9386-p105">[!HINWEIS] Sie müssen für Tabellen keine Indizes erstellen, jedoch kann der Zugriff auf einen bestimmten Datensatz oder die Verarbeitung von Verknüpfungen bei großen Tabellen ohne Index lange dauern. Zu viele Indizes hingegen können Aktualisierungen der Datenbank verlangsamen, da jeder der Tabellenindizes ergänzt wird.</span><span class="sxs-lookup"><span data-stu-id="e9386-p105">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time. Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span>

<span data-ttu-id="e9386-120">Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft jedes **Field**-Objekts im Index bestimmt die Reihenfolge zurückgegebener Datensätze und somit das zu verwendende Zugriffsverfahren für diesen Index.</span><span class="sxs-lookup"><span data-stu-id="e9386-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="e9386-p106">Jedes **Field**-Objekt in der **Fields**-Auflistung eines **Index**-Objekts ist Bestandteil des Indexes. Legen Sie beim Definieren eines neuen **Index**-Objekts dessen Eigenschaften fest, bevor Sie es einer Auflistung anfügen, damit das **Index**-Objekt anschließend verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e9386-p106">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index. To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <span data-ttu-id="e9386-123">[!HINWEIS] Sie können die Einstellung einer **Name**-Eigenschaft eines vorhandenen **Index**-Objekts nur dann ändern, wenn die Einstellung der **[Updatable](connection-updatable-property-dao.md)** -Eigenschaft des **TableDef**-Objekts, in dem es sich befindet, auf **True** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9386-123">You can modify the **Name** property setting of an existing **Index** object only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="e9386-p107">Wenn Sie einen Primärschlüssel für eine Tabelle festlegen, wird er vom Microsoft Access-Datenbankmodul automatisch als Primärindex definiert. Ein Primärindex besteht aus einem oder mehreren Feldern, die alle Datensätze einer Tabelle in einer vordefinierten Reihenfolge eindeutig anordnen. Da das Primärindexfeld eindeutig sein muss, wird die **Unique**-Eigenschaft des primären **Index**-Objekts vom Microsoft Access-Datenbankmodul automatisch auf **True** festgelegt. Wenn der Primärindex aus mehreren Feldern besteht, kann jedes Feld doppelte Werte enthalten, die Kombination der Werte aus allen indizierten Feldern muss jedoch eindeutig sein. Ein Primärindex besteht aus einem Schüssel für die Tabelle und enthält stets dieselben Felder wie der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e9386-p107">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index. A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**. If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique. A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9386-p108">Stellen Sie sicher, dass die Daten mit den Attributen des neuen Indexes übereinstimmen. Wenn der Index eindeutige Werte erfordert, stellen Sie sicher, dass vorhandene Datensätze keine Duplikate enthalten. Bei Duplikaten kann das Microsoft Access-Datenbankmodul den Index nicht erstellen, und bei dem Versuch, die Append-Methode des neuen Indexes zu verwenden, tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e9386-p108">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="e9386-p109">Wenn Sie eine Beziehung erstellen, die die referentielle Integrität erzwingt, erstellt das Microsoft Access-Datenbankmodul automatisch einen Index, wobei die **Foreign**-Eigenschaft in der referenzierenden Tabelle als Fremdschlüssel festgelegt wird. Nachdem Sie eine Tabellenbeziehung erstellt haben, verhindert das Microsoft Access-Datenbankmodul Ergänzungen oder Änderungen der Datenbank, die nicht zu der Beziehung passen. Wenn Sie die **Attributes**-Eigenschaft des **[Relation](relation-object-dao.md)** -Objekts so festlegen, dass Aktualisierungsweitergaben und Löschweitergaben zulässig sind, werden Datensätze in verknüpften Tabellen automatisch vom Microsoft Access-Datenbankmodul aktualisiert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9386-p109">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table. After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship. If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="e9386-135">Verwenden Sie die **CreateIndex**-Methode für ein **TableDef**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e9386-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="e9386-136">Verwenden Sie die **CreateField**-Methode für ein **Index**-Objekt, um ein **Field**-Objekt für jedes Feld (Spalte) zu erstellen, das Sie in das **Index**-Objekt einschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="e9386-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="e9386-137">Legen Sie nach Bedarf **Index**-Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="e9386-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="e9386-138">Fügen Sie das **Field**-Objekt der **Fields**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="e9386-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="e9386-139">Fügen Sie das **Index**-Objekt der **Indexes**-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="e9386-139">Append the **Index** object to the **Indexes** collection.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9386-140">[!HINWEIS] Die **Clustered**-Eigenschaft wird für Datenbanken ignoriert, die das Microsoft Access-Datenbankmodul verwenden, das gruppierte Indizes nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9386-140">The **Clustered** property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span>

## <a name="example"></a><span data-ttu-id="e9386-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e9386-141">Example</span></span>

<span data-ttu-id="e9386-p110">Dieses Beispiel erstellt ein neues Index-Objekt, fügt es der Indexes-Auflistung des TableDef-Objekts der Employees-Tabelle (Personal) an und führt die Indexes-Auflistung des TableDef-Objekts auf. Zuletzt listet es ein Recordset-Objekt auf, zuerst unter Verwendung des primären Index-Objekts und dann unter Verwendung des neuen Index-Objekts. Die IndexOutput-Prozedur ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9386-p110">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="e9386-145">Dieses Beispiel verwendet die **CreateIndex** -Methode, um zwei neue **Index** -Objekte zu erstellen, und fügt sie dann der **Indexes** -Auflistung des **TableDef** -Objekts der Employees-Tabelle (Personal) an.</span><span class="sxs-lookup"><span data-stu-id="e9386-145">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="e9386-146">Klicken Sie dann der **Indexes** -Auflistung des **TableDef** -Objekts, der **Fields** -Auflistung der neuen **Index** -Objekte und der Properties-Auflistung der neuen **Index** -Objekte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e9386-146">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="e9386-147">Zum Ausführen dieser Prozedur ist die CreateIndexOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9386-147">The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```

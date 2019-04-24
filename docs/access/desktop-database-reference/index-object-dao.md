---
title: Index-Objekt-Datenzugriffsobjekte (DAO)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291768"
---
# <a name="index-object-dao"></a>Index-Objekt (DAO)

**Gilt für**: Access 2013, Office 2013

**Index**-Objekte geben die Reihenfolge an, in der auf Datensätze aus Datenbanktabellen zugegriffen wird, und sie geben an, ob doppelte Datensätze akzeptiert werden. Dadurch stellen sie einen effizienten Zugriff auf Daten sicher. Bei externen Datenbanken beschreiben **Index**-Objekte die für externe Tabellen eingerichteten Indizes (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="remarks"></a>Bemerkungen

The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects. Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.

Bei einem **Index**-Objekt können Sie die folgenden Aktionen ausführen:

- Bestimmen Sie mit der **Required**-Eigenschaft, ob die **[Field](field-object-dao.md)** -Objekte im Index Werte erfordern, die nicht Null sind, und bestimmen Sie dann mit der **IgnoreNulls**-Eigenschaft, ob die Nullwerte Indexeinträge besitzen.

- Bestimmen Sie mit den Eigenschaften **Primary** und **Unique** die Sortierung und Eindeutigkeit des **Index**-Objekts.

Das Microsoft Access-Datenbankmodul verwaltet alle Indizes von Basistabellen automatisch. Bei jedem Hinzufügen, Ändern oder Löschen von Datensätzen in der Basistabelle werden die Indizes aktualisiert. Nachdem Sie die Datenbank erstellt haben, bringen Sie die Indexstatistiken mit der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode regelmäßig auf den neuesten Stand.

When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property. Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection. This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.

> [!NOTE]
> [!HINWEIS] Sie müssen für Tabellen keine Indizes erstellen, jedoch kann der Zugriff auf einen bestimmten Datensatz oder die Verarbeitung von Verknüpfungen bei großen Tabellen ohne Index lange dauern. Zu viele Indizes hingegen können Aktualisierungen der Datenbank verlangsamen, da jeder der Tabellenindizes ergänzt wird.

Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft jedes **Field**-Objekts im Index bestimmt die Reihenfolge zurückgegebener Datensätze und somit das zu verwendende Zugriffsverfahren für diesen Index.

Jedes **Field**-Objekt in der **Fields**-Auflistung eines **Index**-Objekts ist Bestandteil des Indexes. Legen Sie beim Definieren eines neuen **Index**-Objekts dessen Eigenschaften fest, bevor Sie es einer Auflistung anfügen, damit das **Index**-Objekt anschließend verwendet werden kann.

> [!NOTE]
> [!HINWEIS] Sie können die Einstellung einer **Name**-Eigenschaft eines vorhandenen **Index**-Objekts nur dann ändern, wenn die Einstellung der **[Updatable](connection-updatable-property-dao.md)** -Eigenschaft des **TableDef**-Objekts, in dem es sich befindet, auf **True** festgelegt ist.

Wenn Sie einen Primärschlüssel für eine Tabelle festlegen, wird er vom Microsoft Access-Datenbankmodul automatisch als Primärindex definiert. Ein Primärindex besteht aus einem oder mehreren Feldern, die alle Datensätze einer Tabelle in einer vordefinierten Reihenfolge eindeutig anordnen. Da das Primärindexfeld eindeutig sein muss, wird die **Unique**-Eigenschaft des primären **Index**-Objekts vom Microsoft Access-Datenbankmodul automatisch auf **True** festgelegt. Wenn der Primärindex aus mehreren Feldern besteht, kann jedes Feld doppelte Werte enthalten, die Kombination der Werte aus allen indizierten Feldern muss jedoch eindeutig sein. Ein Primärindex besteht aus einem Schüssel für die Tabelle und enthält stets dieselben Felder wie der Primärschlüssel.

> [!IMPORTANT]
> Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.

Wenn Sie eine Beziehung erstellen, die die referentielle Integrität erzwingt, erstellt das Microsoft Access-Datenbankmodul automatisch einen Index, wobei die **Foreign**-Eigenschaft in der referenzierenden Tabelle als Fremdschlüssel festgelegt wird. Nachdem Sie eine Tabellenbeziehung erstellt haben, verhindert das Microsoft Access-Datenbankmodul Ergänzungen oder Änderungen der Datenbank, die nicht zu der Beziehung passen. Wenn Sie die **Attributes**-Eigenschaft des **[Relation](relation-object-dao.md)** -Objekts so festlegen, dass Aktualisierungsweitergaben und Löschweitergaben zulässig sind, werden Datensätze in verknüpften Tabellen automatisch vom Microsoft Access-Datenbankmodul aktualisiert oder gelöscht.

1.  Verwenden Sie die **CreateIndex**-Methode für ein **TableDef**-Objekt.

2.  Verwenden Sie die **CreateField**-Methode für ein **Index**-Objekt, um ein **Field**-Objekt für jedes Feld (Spalte) zu erstellen, das Sie in das **Index**-Objekt einschließen möchten.

3.  Legen Sie nach Bedarf **Index**-Eigenschaften fest.

4.  Fügen Sie das **Field**-Objekt der **Fields**-Auflistung an.

5.  Fügen Sie das **Index**-Objekt der **Indexes**-Auflistung an.

    > [!NOTE]
    > [!HINWEIS] Die **Clustered**-Eigenschaft wird für Datenbanken ignoriert, die das Microsoft Access-Datenbankmodul verwenden, das gruppierte Indizes nicht unterstützt.

## <a name="example"></a>Beispiel

This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.

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

This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.

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

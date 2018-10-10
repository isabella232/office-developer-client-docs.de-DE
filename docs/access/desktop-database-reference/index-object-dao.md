---
title: Index-Objekt - Datenzugriff Objekte (DAO)
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e45356a09a6a625381ef9a39d40e7349234460ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474571"
---
# <a name="index-object-dao"></a>Index Object (DAO)

**Betrifft**: Access 2013 | Office 2013

**Index**-Objekte geben die Reihenfolge an, in der auf Datensätze aus Datenbanktabellen zugegriffen wird, und sie geben an, ob doppelte Datensätze akzeptiert werden. Dadurch stellen sie einen effizienten Zugriff auf Daten sicher. Bei externen Datenbanken beschreiben **Index**-Objekte die für externe Tabellen eingerichteten Indizes (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="remarks"></a>Bemerkungen

Im Microsoft Access-Datenbankmodul werden beim Verknüpfen von Tabellen und Erstellen von Recordset-Objekten Indizes verwendet. Indizes bestimmen die Reihenfolge, in der Recordset-Objekte vom Typ Tabelle Objekte zurückgeben, sie bestimmen jedoch nicht die Reihenfolge, in der Datensätze in der Basistabelle im Microsoft Access-Datenbankmodul gespeichert werden, oder die Reihenfolge, in der ein anderer Typ von Recordset-Objekten Datensätze zurückgibt.

Bei einem **Index**-Objekt können Sie die folgenden Aktionen ausführen:

- Bestimmen Sie mit der **Required**-Eigenschaft, ob die **[Field](field-object-dao.md)** -Objekte im Index Werte erfordern, die nicht Null sind, und bestimmen Sie dann mit der **IgnoreNulls**-Eigenschaft, ob die Nullwerte Indexeinträge besitzen.

- Bestimmen Sie mit den Eigenschaften **Primary** und **Unique** die Sortierung und Eindeutigkeit des **Index**-Objekts.

Das Microsoft Access-Datenbankmodul verwaltet alle Indizes von Basistabellen automatisch. Bei jedem Hinzufügen, Ändern oder Löschen von Datensätzen in der Basistabelle werden die Indizes aktualisiert. Nachdem Sie die Datenbank erstellt haben, bringen Sie die Indexstatistiken mit der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode regelmäßig auf den neuesten Stand.

Wenn Sie auf ein Recordset-Objekt vom Typ Tabelle zugreifen, geben Sie mit der Index-Eigenschaft des Objekts die Reihenfolge der Datensätze an. Legen Sie diese Eigenschaft auf die Einstellung der Name-Eigenschaft eines vorhandenen Index-Objekts in der Indexes-Auflistung fest. Diese Auflistung ist im TableDef-Objekt enthalten, das dem zu füllenden Recordset-Objekt zugrunde liegt.

> [!NOTE]
> <P>[!HINWEIS] Sie müssen für Tabellen keine Indizes erstellen, jedoch kann der Zugriff auf einen bestimmten Datensatz oder die Verarbeitung von Verknüpfungen bei großen Tabellen ohne Index lange dauern. Zu viele Indizes hingegen können Aktualisierungen der Datenbank verlangsamen, da jeder der Tabellenindizes ergänzt wird.</P>

Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft jedes **Field**-Objekts im Index bestimmt die Reihenfolge zurückgegebener Datensätze und somit das zu verwendende Zugriffsverfahren für diesen Index.

Jedes **Field**-Objekt in der **Fields**-Auflistung eines **Index**-Objekts ist Bestandteil des Indexes. Legen Sie beim Definieren eines neuen **Index**-Objekts dessen Eigenschaften fest, bevor Sie es einer Auflistung anfügen, damit das **Index**-Objekt anschließend verwendet werden kann.

> [!NOTE]
> <P>[!HINWEIS] Sie können die Einstellung einer <STRONG>Name</STRONG>-Eigenschaft eines vorhandenen <STRONG>Index</STRONG>-Objekts nur dann ändern, wenn die Einstellung der <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> -Eigenschaft des <STRONG>TableDef</STRONG>-Objekts, in dem es sich befindet, auf <STRONG>True</STRONG> festgelegt ist.</P>

Wenn Sie einen Primärschlüssel für eine Tabelle festlegen, wird er vom Microsoft Access-Datenbankmodul automatisch als Primärindex definiert. Ein Primärindex besteht aus einem oder mehreren Feldern, die alle Datensätze einer Tabelle in einer vordefinierten Reihenfolge eindeutig anordnen. Da das Primärindexfeld eindeutig sein muss, wird die **Unique**-Eigenschaft des primären **Index**-Objekts vom Microsoft Access-Datenbankmodul automatisch auf **True** festgelegt. Wenn der Primärindex aus mehreren Feldern besteht, kann jedes Feld doppelte Werte enthalten, die Kombination der Werte aus allen indizierten Feldern muss jedoch eindeutig sein. Ein Primärindex besteht aus einem Schüssel für die Tabelle und enthält stets dieselben Felder wie der Primärschlüssel.

> [!IMPORTANT]
> Stellen Sie sicher, dass die Daten mit den Attributen des neuen Indexes übereinstimmen. Wenn der Index eindeutige Werte erfordert, stellen Sie sicher, dass vorhandene Datensätze keine Duplikate enthalten. Bei Duplikaten kann das Microsoft Access-Datenbankmodul den Index nicht erstellen, und bei dem Versuch, die Append-Methode des neuen Indexes zu verwenden, tritt ein abfangbarer Fehler auf.

Wenn Sie eine Beziehung erstellen, die die referentielle Integrität erzwingt, erstellt das Microsoft Access-Datenbankmodul automatisch einen Index, wobei die **Foreign**-Eigenschaft in der referenzierenden Tabelle als Fremdschlüssel festgelegt wird. Nachdem Sie eine Tabellenbeziehung erstellt haben, verhindert das Microsoft Access-Datenbankmodul Ergänzungen oder Änderungen der Datenbank, die nicht zu der Beziehung passen. Wenn Sie die **Attributes**-Eigenschaft des **[Relation](relation-object-dao.md)** -Objekts so festlegen, dass Aktualisierungsweitergaben und Löschweitergaben zulässig sind, werden Datensätze in verknüpften Tabellen automatisch vom Microsoft Access-Datenbankmodul aktualisiert oder gelöscht.

1.  Verwenden Sie die **CreateIndex**-Methode für ein **TableDef**-Objekt.

2.  Verwenden Sie die **CreateField**-Methode für ein **Index**-Objekt, um ein **Field**-Objekt für jedes Feld (Spalte) zu erstellen, das Sie in das **Index**-Objekt einschließen möchten.

3.  Legen Sie nach Bedarf **Index**-Eigenschaften fest.

4.  Fügen Sie das **Field**-Objekt der **Fields**-Auflistung an.

5.  Fügen Sie das **Index**-Objekt der **Indexes**-Auflistung an.
    

    > [!NOTE]
    > <P>[!HINWEIS] Die <STRONG>Clustered</STRONG>-Eigenschaft wird für Datenbanken ignoriert, die das Microsoft Access-Datenbankmodul verwenden, das gruppierte Indizes nicht unterstützt.</P>



## <a name="example"></a>Beispiel

Dieses Beispiel erstellt ein neues Index-Objekt, fügt es der Indexes-Auflistung des TableDef-Objekts der Employees-Tabelle (Personal) an und führt die Indexes-Auflistung des TableDef-Objekts auf. Zuletzt listet es ein Recordset-Objekt auf, zuerst unter Verwendung des primären Index-Objekts und dann unter Verwendung des neuen Index-Objekts. Die IndexOutput-Prozedur ist zum Ausführen dieser Prozedur erforderlich.

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

Dieses Beispiel verwendet die **CreateIndex** -Methode, um zwei neue **Index** -Objekte zu erstellen, und fügt sie dann der **Indexes** -Auflistung des **TableDef** -Objekts der Employees-Tabelle (Personal) an. Klicken Sie dann der **Indexes** -Auflistung des **TableDef** -Objekts, der **Fields** -Auflistung der neuen **Index** -Objekte und der Properties-Auflistung der neuen **Index** -Objekte aufgelistet. Zum Ausführen dieser Prozedur ist die CreateIndexOutput-Funktion erforderlich.

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

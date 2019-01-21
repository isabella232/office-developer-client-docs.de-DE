---
title: TableDef-Objekt (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6e1182427c688e7c8b5ca53c1f5f4bb208b3609a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726344"
---
# <a name="tabledef-object-dao"></a><span data-ttu-id="3863e-102">TableDef-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="3863e-102">TableDef Object (DAO)</span></span>

<span data-ttu-id="3863e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3863e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3863e-104">Ein **TableDef**-Objekt stellt die gespeicherte Definition einer Basistabelle oder einer verknüpften Tabelle dar (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="3863e-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="3863e-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3863e-105">Remarks</span></span>

<span data-ttu-id="3863e-p101">Sie ändern eine Tabellendefinition mithilfe eines **TableDef**-Objekts sowie seiner Methoden und Eigenschaften. Folgendes ist zum Beispiel möglich:</span><span class="sxs-lookup"><span data-stu-id="3863e-p101">You manipulate a table definition using a **TableDef** object and its methods and properties. For example, you can:</span></span>

- <span data-ttu-id="3863e-108">Untersuchen Sie das Feld und die Indexstruktur einer lokalen, verknüpften oder externen Tabelle in einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3863e-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="3863e-109">Verwenden Sie die **Connect**- und **SourceTableName**-Eigenschaften, um Informationen zu verknüpften Tabellen festzulegen oder zurückzugeben, und verwenden Sie die **RefreshLink**-Methode, um Verbindungen zu verknüpften Tabellen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3863e-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="3863e-110">Verwenden Sie die **ValidationRule**- und **ValidationText**-Eigenschaften, um Überprüfungsbedingungen festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3863e-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="3863e-111">Verwenden Sie die **OpenRecordset**-Methode, um ein **Recordset**-Objekt vom Typ "table", "dynaset", "dynamic", "snapshot" oder "forward–only" basierend auf der Tabellendefinition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3863e-111">Use the **OpenRecordset** method to create a table-, dynaset-, dynamic-, snapshot-, or forward-only-type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="3863e-112">Für Basistabellen enthält die **RecordCount**-Eigenschaft die Anzahl der Datensätze in der angegebenen Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="3863e-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="3863e-113">For linked tables, the **RecordCount** property setting is always –1.</span><span class="sxs-lookup"><span data-stu-id="3863e-113">For linked tables, the **RecordCount** property setting is always -1.</span></span>

<span data-ttu-id="3863e-114">Um ein neues **TableDef**-Objekt zu erstellen, verwenden Sie die **[CreateTableDef](database-createtabledef-method-dao.md)**-Methode.</span><span class="sxs-lookup"><span data-stu-id="3863e-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="3863e-115">So fügen Sie einer Tabelle ein Feld hinzu</span><span class="sxs-lookup"><span data-stu-id="3863e-115">To add a field to a table</span></span>

1.  <span data-ttu-id="3863e-116">Stellen Sie sicher, dass alle **[Recordset](recordset-object-dao.md)**-Objekte, die auf der Tabelle basieren, geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="3863e-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="3863e-117">Verwenden Sie die **CreateField**-Methode, um eine **Field**-Objektvariable zu erstellen, und legen Sie ihre Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="3863e-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="3863e-118">Verwenden Sie die **Append**-Methode, um das **Field**-Objekt zur **Fields**-Auflistung des **TableDef**-Objekts hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3863e-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="3863e-119">Sie können ein **Field**-Objekt aus einer **TableDefs**-Auflistung löschen, wenn ihm keine Indizes zugewiesen sind. Die Daten des Felds gehen aber verloren.</span><span class="sxs-lookup"><span data-stu-id="3863e-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="3863e-120">So erstellen Sie eine Tabelle, die für neue Datensätze in einer Datenbank bereit ist</span><span class="sxs-lookup"><span data-stu-id="3863e-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="3863e-121">Verwenden Sie die **CreateTableDef**-Methode, um ein **TableDef**-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3863e-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="3863e-122">Legen Sie seine Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="3863e-122">Set its properties.</span></span>

3.  <span data-ttu-id="3863e-123">Verwenden Sie für jedes Feld in der Tabelle die **CreateField**-Methode, um eine **Field**-Objektvariable zu erstellen, und legen Sie ihre Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="3863e-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="3863e-124">Verwenden Sie die **Append**-Methode, um die Felder zur **Fields**-Auflistung des **TableDef**-Objekts hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3863e-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="3863e-125">Verwenden Sie die **Append**-Methode, um das neue **TableDef**-Objekt zur **TableDefs**-Auflistung des **Database**-Objekts hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3863e-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="3863e-126">Eine verknüpfte Tabelle ist durch die **SourceTableName**- und **Connect**-Eigenschaften des **TableDef**-Objekts mit der Datenbank verbunden.</span><span class="sxs-lookup"><span data-stu-id="3863e-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="3863e-127">So verknüpfen Sie eine Tabelle mit einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="3863e-127">To link a table to a database</span></span>

1.  <span data-ttu-id="3863e-128">Verwenden Sie die **CreateTableDef**-Methode, um ein **TableDef**-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3863e-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="3863e-129">Legen Sie die **Connect**- und **SourceTableName**-Eigenschaften (und optional die **Attributes**-Eigenschaft) fest.</span><span class="sxs-lookup"><span data-stu-id="3863e-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="3863e-130">Verwenden Sie die **Append**-Methode, um es der **TableDefs**-Auflistung eines **Database**-Objekts hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3863e-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="3863e-131">Um auf ein **TableDef**-Objekt in einer Auflistung durch die Ordnungszahl oder die Einstellung der **Name**-Eigenschaft zu verweisen, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="3863e-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="3863e-132">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="3863e-132">**TableDefs**(0)</span></span>

<span data-ttu-id="3863e-133">**TableDefs**("name")</span><span class="sxs-lookup"><span data-stu-id="3863e-133">TableDefs![name]</span></span>

<span data-ttu-id="3863e-134">**TableDefs**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="3863e-134">**TableDefs**![\!name\]]</span></span>

## <a name="example"></a><span data-ttu-id="3863e-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3863e-135">Example</span></span>

<span data-ttu-id="3863e-p103">Dieses Beispiel erstellt ein neues **TableDef**-Objekt und hängt es an die **TableDefs**-Auflistung des Northwind-Datenbankobjekts an. Dann zählt es die **TableDefs**-Auflistung und die **Properties**-Auflistung des neuen **TableDef**-Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="3863e-p103">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="3863e-138">Dieses Beispiel erstellt ein neues **TableDef**-Objekt in der Northwind-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3863e-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

<span data-ttu-id="3863e-p104">Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.</span><span class="sxs-lookup"><span data-stu-id="3863e-p104">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="3863e-142">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="3863e-142">**Sample code provided by:** The [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

---
title: Index.Primary-Eigenschaft (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ff99f60fce41c7fa7de604a5109e68f6f744e68a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997644"
---
# <a name="indexprimary-property-dao"></a><span data-ttu-id="c5f6a-102">Index.Primary-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5f6a-102">Index.Primary property (DAO)</span></span>

<span data-ttu-id="c5f6a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5f6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5f6a-104">Legt einen Wert fest, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen Primärschlüsselindex für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c5f6a-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a primary key index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f6a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f6a-105">Syntax</span></span>

<span data-ttu-id="c5f6a-106">*Ausdruck* . Primäre</span><span class="sxs-lookup"><span data-stu-id="c5f6a-106">*expression* .Primary</span></span>

<span data-ttu-id="c5f6a-107">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5f6a-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f6a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5f6a-108">Remarks</span></span>

<span data-ttu-id="c5f6a-p101">Ein neues **Index**-Objekt, das noch nicht an eine Auflistung angehängt wurde, hat den Lese-/Schreibzugriff für die **Primary**-Eigenschaft. Für ein vorhandenes **Index**-Objekt in einer **[Indexes](indexes-collection-dao.md)** -Auflistung ist die Eigenschaft schreibgeschützt. Wenn das **Index**-Objekt an das **[TableDef](tabledef-object-dao.md)** -Objekt angehängt wurde, aber das **TableDef**-Objekt nicht an die **[TableDefs](tabledefs-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für die **Index**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c5f6a-p101">The **Primary** property setting is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection. If the **Index** object is appended to the **[TableDef](tabledef-object-dao.md)** object but the **TableDef** object isn't appended to the **[TableDefs](tabledefs-collection-dao.md)** collection, the **Index** property is read/write.</span></span>

<span data-ttu-id="c5f6a-p102">Ein Primärschlüsselindex besteht aus einem oder mehreren Feldern, die alle Datensätze in einer Tabelle in einer vordefinierten Reihenfolge eindeutig identifizieren. Da das Indexfeld eindeutig sein muss, wird die **[Unique](index-unique-property-dao.md)** -Eigenschaft des **Index**-Objekts auf **True** festgelegt. Wenn der Primärschlüsselindex aus mehreren Feldern besteht, kann jedes Feld Duplikatwerte enthalten. Jede Kombination von Werten aus den indizierten Feldern muss jedoch eindeutig sein. Ein Primärschlüsselindex besteht aus einem Schlüssel für die Tabelle und enthält gewöhnlich dieselben Felder wie der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c5f6a-p102">A primary key index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the index field must be unique, the **[Unique](index-unique-property-dao.md)** property of the **Index** object is set to **True**. If the primary key index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique. A primary key index consists of a key for the table and usually contains the same fields as the primary key.</span></span>

> [!NOTE]
> <span data-ttu-id="c5f6a-p103">[!HINWEIS] Sie müssen keine Indizes für Tabellen erstellen, doch in großen, nicht-indizierten Tabellen kann der Zugriff auf einen Datensatz einige Zeit in Anspruch nehmen. Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft der einzelnen **[Field](field-object-dao.md)** -Objekte im **Index**-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher die für den betreffenden Index zu verwendenden Zugriffsverfahren. Wenn Sie in Ihrer Datenbank eine neue Tabelle erstellen, sollten Sie einen Index mit einem oder mehreren Feldern erstellen, der jeden Datensatz eindeutig identifiziert, und anschließend die **Primary**-Eigenschaft des **Index**-Objekts auf **True** festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5f6a-p103">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time. The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index. When you create a new table in your database, it's a good idea to create an index on one or more fields that uniquely identify each record, and then set the **Primary** property of the **Index** object to **True**.</span></span>

<span data-ttu-id="c5f6a-118">Wenn Sie einen Primärschlüssel für eine Tabelle festlegen, wird der Primärschlüssel automatisch als Primärschlüsselindex für die Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="c5f6a-118">When you set a primary key for a table, the primary key is automatically defined as the primary key index for the table.</span></span>

## <a name="example"></a><span data-ttu-id="c5f6a-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c5f6a-119">Example</span></span>

<span data-ttu-id="c5f6a-p104">In diesem Beispiel wird mithilfe der **Primary**-Eigenschaft ein neues **Index**-Objekt in einem neuen **TableDef**-Objekt als primärer **Index** für die Tabelle festgelegt. Beachten Sie, dass beim Festlegen der **Primary**-Eigenschaft auf **True** die Eigenschaften **Unique** und **Required** automatisch auf **True** gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c5f6a-p104">This example uses the **Primary** property to designate a new **Index** in a new **TableDef** as the primary **Index** for that table. Note that setting the **Primary** property to **True** automatically sets **Unique** and **Required** properties to **True** as well.</span></span>

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```

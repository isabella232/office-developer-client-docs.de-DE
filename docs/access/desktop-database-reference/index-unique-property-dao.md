---
title: Index. Unique-Eigenschaft (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5c94200245b4736ad244cb37beec617a98d6c367
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291692"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="eb1df-102">Index. Unique-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb1df-102">Index.Unique property (DAO)</span></span>

<span data-ttu-id="eb1df-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb1df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb1df-104">Legt einen Wert fest, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen eindeutigen Index (Schlüssel) für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="eb1df-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb1df-105">Syntax</span></span>

<span data-ttu-id="eb1df-106">*Ausdruck* . Eindeutige</span><span class="sxs-lookup"><span data-stu-id="eb1df-106">*expression* .Unique</span></span>

<span data-ttu-id="eb1df-107">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb1df-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1df-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1df-108">Remarks</span></span>

<span data-ttu-id="eb1df-109">Es besteht Lese-/Schreibzugriff für den Wert dieser Eigenschaft, bis das Objekt an eine Auflistung angefügt wird. Ab diesem Zeitpunkt ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="eb1df-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="eb1df-p101">Ein eindeutiger Index besteht aus einem oder mehreren Feldern, die alle Datensätze in einer Tabelle in einer eindeutigen, vordefinierten Reihenfolge logisch anordnen. Wenn der Index aus einem Feld besteht, müssen die Werte in diesem Feld für die gesamte Tabelle eindeutig sein. Wenn der Index aus mehreren Feldern besteht, kann jedes Feld doppelte Werte enthalten, doch jede Kombination der Werte der indizierten Felder muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="eb1df-p101">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order. If the index consists of one field, values in that field must be unique for the entire table. If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="eb1df-p102">Wenn sowohl die **Unique**- als auch die **[Primary](index-primary-property-dao.md)** -Eigenschaft eines **Index**-Objekts den Wert **True** hat, ist der Index eindeutig und primär, d. h. er identifiziert alle Datensätze in der Tabelle in einer vordefinierten, logischen Reihenfolge eindeutig. Wenn die **Primary**-Eigenschaft den Wert **False** hat, ist der Index ein sekundärer Index. Sekundäre Indizes (Schlüssel- als auch Nicht-Schlüsselindizes) ordnen Datensätze in einer vordefinierten Weise logisch an, ohne als Bezeichner für Datensätze in der Tabelle zu dienen.</span><span class="sxs-lookup"><span data-stu-id="eb1df-p102">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order. If the **Primary** property is set to **False**, the index is a secondary index. Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>

> [!NOTE]
> - <span data-ttu-id="eb1df-116">Sie müssen keine Indizes für Tabellen erstellen, doch in großen, nicht-indizierten Tabellen kann der Zugriff auf einen Datensatz einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="eb1df-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span>
> - <span data-ttu-id="eb1df-117">Datensätze, die aus Tabellen ohne Indizes abgerufen werden, werden in einer unbestimmten Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb1df-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="eb1df-118">Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft der einzelnen **[Field](field-object-dao.md)** -Objekte im **Index**-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher das für das betreffende **Index**-Objekt zu verwendende Zugriffsverfahren.</span><span class="sxs-lookup"><span data-stu-id="eb1df-118">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that **Index** object.</span></span>
> - <span data-ttu-id="eb1df-119">Mithilfe eines eindeutigen Indexes wird die Suche nach Datensätzen optimiert.</span><span class="sxs-lookup"><span data-stu-id="eb1df-119">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="eb1df-120">Indizes wirken sich nicht auf die physische Reihenfolge einer Basistabelle aus. Indizes wirken sich nur auf die Verwendung des **[Recordset](recordset-object-dao.md)** -Objekts vom Typ "Tabelle" aus, wenn ein bestimmter Index ausgewählt wird oder wenn das Microsoft Access-Datenbankmodul **Recordset** -Objekte erstellt.</span><span class="sxs-lookup"><span data-stu-id="eb1df-120">Indexes don't affect the physical order of a base table; indexes affect only how the records are accessed by the table-type **[Recordset](recordset-object-dao.md)** object when a particular index is chosen or when the Microsoft Access database engine creates **Recordset** objects.</span></span>

## <a name="example"></a><span data-ttu-id="eb1df-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eb1df-121">Example</span></span>

<span data-ttu-id="eb1df-p103">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="eb1df-p103">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```

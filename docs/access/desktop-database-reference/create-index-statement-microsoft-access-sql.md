---
title: CREATE INDEX-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295429"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="a42c4-102">CREATE INDEX-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a42c4-102">CREATE INDEX Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a42c4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a42c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a42c4-104">Erstellt einen neuen Index für eine vorhandene Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a42c4-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="a42c4-105">Bei Nicht-Microsoft Access-Datenbankmodulen wird die Verwendung von CREATE INDEX (außer zum Erstellen eines Pseudoindexes für eine verknüpfte ODBC-Tabelle) oder von DDL-Anweisungen (Data Definition Language) vom Microsoft Access-Datenbankmodul nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a42c4-105">For non-Microsoft Access atabse engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="a42c4-106">Verwenden Sie stattdessen die **Create**-Methoden von DAO.</span><span class="sxs-lookup"><span data-stu-id="a42c4-106">Use the DAO Create methods instead.</span></span> <span data-ttu-id="a42c4-107">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="a42c4-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="a42c4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a42c4-108">Syntax</span></span>

<span data-ttu-id="a42c4-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span><span class="sxs-lookup"><span data-stu-id="a42c4-109">CREATE [ UNIQUE ] INDEX index
    ON table (field [ASC|DESC][, field [ASC|DESC], …])
    [WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }]</span></span>

<span data-ttu-id="a42c4-110">Die CREATE INDEX-Anweisung setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="a42c4-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a42c4-111">Part</span><span class="sxs-lookup"><span data-stu-id="a42c4-111">Part</span></span></p></th>
<th><p><span data-ttu-id="a42c4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a42c4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a42c4-113"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="a42c4-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="a42c4-114">Der Name des zu erstellenden Index.</span><span class="sxs-lookup"><span data-stu-id="a42c4-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42c4-115"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="a42c4-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="a42c4-116">Der Name der vorhandenen Tabelle, die den Index enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="a42c4-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42c4-117"><em>field</em></span><span class="sxs-lookup"><span data-stu-id="a42c4-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="a42c4-p102">Der Name des oder der zu indizierenden Felder. Setzen Sie den Feldnamen in Klammern, und listen Sie ihn im Anschluss an den Tabellennamen auf, um einen Index mit einem Feld zu erstellen. Wenn Sie einen Index mit mehreren Feldern erstellen möchten, listen Sie jedes Feld auf, dass im Index eingeschlossen werden soll. Verwenden Sie das reservierte Wort DESC, um Indizes in absteigender Reihenfolge zu erstellen. Andernfalls wird davon ausgegangen, dass die Indizes in aufsteigender Reihenfolge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a42c4-p102">The name of the field or fields to be indexed. To create a single-field index, list the field name in parentheses following the table name. To create a multiple-field index, list the name of each field to be included in the index. To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a42c4-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a42c4-122">Remarks</span></span>

<span data-ttu-id="a42c4-123">Verwenden Sie das reservierte Wort UNIQUE, um doppelte Werte im indizierten Feld oder in Feldern verschiedener Datensätze zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="a42c4-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="a42c4-124">In der optionalen WITH-Klausel können Sie Gültigkeitsprüfungsregeln für Daten erzwingen.</span><span class="sxs-lookup"><span data-stu-id="a42c4-124">In the optional WITH clause you can enforce data validation rules.</span></span> <span data-ttu-id="a42c4-125">Sie können:</span><span class="sxs-lookup"><span data-stu-id="a42c4-125">You can:</span></span>

- <span data-ttu-id="a42c4-126">Sie können NULL-Einträge im indizierten Feld oder in Feldern neuer Datensätze untersagen, indem Sie die Option DISALLOW NULL verwenden.</span><span class="sxs-lookup"><span data-stu-id="a42c4-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="a42c4-127">Sie können verhindern, dass Datensätze mit **NULL**-Werten in dem/den indizierten Feld/Feldern in den Index aufgenommen werden, indem Sie die Option IGNORE NULL verwenden.</span><span class="sxs-lookup"><span data-stu-id="a42c4-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="a42c4-p104">Das oder die indizierten Felder unter Verwendung des reservierten Worts PRIMARY als Primärschlüssel bestimmen. Dies setzt voraus, dass der Schlüssel eindeutig ist, sodass das reservierte Wort UNIQUE ausgelassen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a42c4-p104">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word. This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="a42c4-130">Sie können CREATE INDEX verwenden, um einen Pseudoindex für eine verknüpfte Tabelle in einer ODBC-Datenquelle (wie z. B. Microsoft SQL Server) zu erstellen, die nicht bereits über einen Index verfügt.</span><span class="sxs-lookup"><span data-stu-id="a42c4-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft SQL Server, that does not already have an index.</span></span> <span data-ttu-id="a42c4-131">Sie benötigen keine Berechtigung für oder Zugriff auf den Remoteserver, um einen Pseudoindex erstellen zu können, und die Remotedatenbank erkennt den Pseudoindex nicht und ist auch nicht davon betroffen.</span><span class="sxs-lookup"><span data-stu-id="a42c4-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="a42c4-132">Für verknüpfte und systemeigene Tabellen wird dieselbe Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="a42c4-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="a42c4-133">Es kann besonders nützlich sein, einen Pseudoindex für eine Tabelle zu erstellen, die normalerweise schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="a42c4-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="a42c4-134">Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index mit einem oder mehreren Feldern zu einer Tabelle hinzuzufügen, und Sie können die ALTER TABLE-Anweisung oder die [DROP](drop-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index zu entfernen, der über die ALTER TABLE- oder CREATE INDEX-Anweisung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a42c4-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="a42c4-135">Verwenden Sie das reservierte Wort PRIMARY nicht, wenn Sie einen neuen Index für eine Tabelle erstellen, die bereits einen Primärschlüssel aufweist. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a42c4-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="a42c4-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a42c4-136">Example</span></span>

<span data-ttu-id="a42c4-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span><span class="sxs-lookup"><span data-stu-id="a42c4-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="a42c4-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span><span class="sxs-lookup"><span data-stu-id="a42c4-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```

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
ms.openlocfilehash: 7710dd89a645b10d20044e2eeaeb26986730c843
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861554"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="4d8e5-102">CREATE INDEX-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4d8e5-102">CREATE INDEX statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4d8e5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d8e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4d8e5-104">Erstellt einen neuen Index für eine vorhandene Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="4d8e5-105">Für Microsoft Access - Datenbanken unterstützt die Verwendung der CREATE INDEX (mit Ausnahme von So erstellen Sie einen Pseudoindex für eine verknüpfte ODBC-Tabelle) oder anderer Anweisungen in Data Definition Language, (Datendefinitionssprache DDL) Microsoft Access-Datenbankmodul nicht.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-105">For non-Microsoft Access database engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="4d8e5-106">Verwenden Sie stattdessen Methoden **DAO erstellen** .</span><span class="sxs-lookup"><span data-stu-id="4d8e5-106">Use the **DAO Create** methods instead.</span></span> <span data-ttu-id="4d8e5-107">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="4d8e5-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d8e5-108">Syntax</span></span>

<span data-ttu-id="4d8e5-109">Erstellen von \[ UNIQUE \] INDEX *Index* ON *Tabelle* (*Feld* \[ASC | DESC\]\[, *Feld* \[ASC | DESC\],... \]) \[WITH {PRIMARY | DISALLOW NULL | IGNORE NULL}\]</span><span class="sxs-lookup"><span data-stu-id="4d8e5-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span></span>

<span data-ttu-id="4d8e5-110">Die CREATE INDEX-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="4d8e5-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d8e5-111">Komponente</span><span class="sxs-lookup"><span data-stu-id="4d8e5-111">Part</span></span></p></th>
<th><p><span data-ttu-id="4d8e5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d8e5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d8e5-113"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="4d8e5-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="4d8e5-114">Der Name des zu erstellenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8e5-115"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="4d8e5-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="4d8e5-116">Der Name der vorhandenen Tabelle, in der der Index enthalten sein wird.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d8e5-117"><em>Feld</em></span><span class="sxs-lookup"><span data-stu-id="4d8e5-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="4d8e5-p102">Der Name des oder der zu indizierenden Felder. Setzen Sie den Feldnamen in Klammern, und listen Sie ihn im Anschluss an den Tabellennamen auf, um einen Index mit einem Feld zu erstellen. Wenn Sie einen Index mit mehreren Feldern erstellen möchten, listen Sie jedes Feld auf, dass im Index eingeschlossen werden soll. Verwenden Sie das reservierte Wort DESC, um Indizes in absteigender Reihenfolge zu erstellen. Andernfalls wird davon ausgegangen, dass die Indizes in aufsteigender Reihenfolge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-p102">The name of the field or fields to be indexed. To create a single-field index, list the field name in parentheses following the table name. To create a multiple-field index, list the name of each field to be included in the index. To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4d8e5-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d8e5-122">Remarks</span></span>

<span data-ttu-id="4d8e5-123">Um im indizierten Feld bzw. in den indizierten Feldern keine duplizierten Werte zuzulassen, verwenden Sie das reservierte Wort UNIQUE.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="4d8e5-124">In der optionalen WITH-Klausel können Sie Datenüberprüfungsregeln erzwingen.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-124">In the optional WITH clause, you can enforce data validation rules.</span></span> <span data-ttu-id="4d8e5-125">Es bestehen folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="4d8e5-125">You can:</span></span>

- <span data-ttu-id="4d8e5-126">Unter Verwendung der DISALLOW NULL-Option Einträge vom Typ Null in dem oder den indizierten Feldern neuer Datensätze nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="4d8e5-127">Datensätze mit **Null** -Werten in dem oder den indizierten Feldern unter Verwendung der IGNORE NULL-Option vom Index ausschließen.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="4d8e5-p104">Das oder die indizierten Felder unter Verwendung des reservierten Worts PRIMARY als Primärschlüssel bestimmen. Dies setzt voraus, dass der Schlüssel eindeutig ist, sodass das reservierte Wort UNIQUE ausgelassen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-p104">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word. This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="4d8e5-130">CREATE INDEX können Sie in einer verknüpften Tabelle in einer ODBC-Datenquelle, wie beispielsweise Microsoft SQL Server erstellen, die nicht bereits über einen Index verfügt.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft SQL Server, that does not already have an index.</span></span> <span data-ttu-id="4d8e5-131">Sie brauchen nicht mit der Berechtigung oder Zugriff auf den Remoteserver zu erstellen, und die Remotedatenbank und wird nicht von den Pseudoindex nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="4d8e5-132">Verwenden Sie dieselbe Syntax für verknüpfte und systemeigene Tabellen.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="4d8e5-133">Systemeigene für eine Tabelle, die normalerweise schreibgeschützt wären erstellen kann insbesondere dann hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="4d8e5-134">Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index mit einem oder mehreren Feldern zu einer Tabelle hinzuzufügen, und Sie können die ALTER TABLE-Anweisung oder die [DROP](drop-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index zu entfernen, der über die ALTER TABLE- oder CREATE INDEX-Anweisung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="4d8e5-135">[!HINWEIS] Verwenden Sie nicht das reservierte Wort PRIMARY, wenn Sie einen neuen Index für eine Tabelle erstellen, die bereits über einen Primärschlüssel verfügt. Andernfalls wird in diesem Fall ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="4d8e5-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4d8e5-136">Example</span></span>

<span data-ttu-id="4d8e5-137">Im folgenden Beispiel wird ein Index erstellt, der aus dem Home Phone-Feld (Telefon privat) und dem Extension-Feld (Durchwahl) in der Employees-Tabelle (Personal) besteht.</span><span class="sxs-lookup"><span data-stu-id="4d8e5-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

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

<span data-ttu-id="4d8e5-p106">Im folgenden Beispiel wird ein Index für die Customers-Tabelle (Kunden) unter Verwendung des CustomerID-Felds (Kunden-Nr) erstellt. Für das CustomerID-Feld sind keine duplizierten Datensätze zulässig, und darüber hinaus sind keine Nullwerte zulässig.

</span><span class="sxs-lookup"><span data-stu-id="4d8e5-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

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

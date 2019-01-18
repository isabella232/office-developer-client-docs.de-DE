---
title: INSERT INTO-Anweisung (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710804"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="92c82-102">INSERT INTO-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="92c82-102">INSERT INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="92c82-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92c82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92c82-p101">Fügt einen Datensatz oder mehrere Datensätze einer Tabelle hinzu. Dies wird als Anfügeabfrage bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="92c82-p101">Adds a record or multiple records to a table. This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c82-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="92c82-106">Syntax</span></span>

### <a name="multiple-record-append-query"></a><span data-ttu-id="92c82-107">Anfügeabfrage mit mehreren Datensätzen</span><span class="sxs-lookup"><span data-stu-id="92c82-107">Multiple-record append query</span></span>

<span data-ttu-id="92c82-108">INSERT INTO *Ziel* \[(*Feld1*\[, *Feld2*\[,... \] \])\] \[IN *externe Datenbank* \] auswählen \[ *Quelle*. \] *Feld1*\[, *Feld2*\[,... \] FROM *Tabellenausdruck]*</span><span class="sxs-lookup"><span data-stu-id="92c82-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

### <a name="single-record-append-query"></a><span data-ttu-id="92c82-109">Anfügeabfrage mit einem Datensatz</span><span class="sxs-lookup"><span data-stu-id="92c82-109">Single-record append query</span></span>

<span data-ttu-id="92c82-110">INSERT INTO *Ziel* \[(*Feld1*\[, *Feld2*\[,... \] \])\] Werte (*Wert1*\[, *Wert2*\[,... \])</span><span class="sxs-lookup"><span data-stu-id="92c82-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="92c82-111">Die INSERT INTO-Anweisung besteht aus folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="92c82-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92c82-112">Teil</span><span class="sxs-lookup"><span data-stu-id="92c82-112">Part</span></span></p></th>
<th><p><span data-ttu-id="92c82-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92c82-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92c82-114"><em>Ziel</em></span><span class="sxs-lookup"><span data-stu-id="92c82-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="92c82-115">Der Name der Tabelle oder Abfrage, an die Datensätze angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92c82-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c82-116"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="92c82-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="92c82-117">Namen der Felder, die angefügt werden, wenn ein Argument <em>Ziel</em> folgen, oder die Namen der Felder, die Daten abgerufen werden sollen, wenn ein Argument <em>Quelle</em> folgen.</span><span class="sxs-lookup"><span data-stu-id="92c82-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c82-118"><em>externeDatenbank</em></span><span class="sxs-lookup"><span data-stu-id="92c82-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="92c82-p102">Der Pfad zu einer externen Datenbank. Eine Beschreibung des Pfads finden Sie unter der <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>-Klausel.  </span><span class="sxs-lookup"><span data-stu-id="92c82-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c82-121"><em>Quelle</em></span><span class="sxs-lookup"><span data-stu-id="92c82-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="92c82-122">Der Name der Tabelle oder Abfrage, aus der Datensätze kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92c82-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92c82-123"><em>Tabellenausdruck</em></span><span class="sxs-lookup"><span data-stu-id="92c82-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="92c82-p103">Die Namen der Tabellen, aus denen Datensätze eingefügt werden. Dieses Argument kann ein einzelner Tabellenname oder eine Kombination aus den Vorgängen <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> oder <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> oder eine gespeicherte Abfrage sein.  </span><span class="sxs-lookup"><span data-stu-id="92c82-p103">The name of the table or tables from which records are inserted. This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92c82-126"><em>Wert1</em>, <em>Wert2</em></span><span class="sxs-lookup"><span data-stu-id="92c82-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="92c82-p104">Die Werte, die in die entsprechenden Felder des neuen Datensatzes eingefügt werden sollen. Jeder Wert wird in das Feld eingefügt, das der Position des Werts in der Liste entspricht: <em>Wert1</em> wird in <em>Feld1</em> des neuen Datensatzes eingefügt, <em>Wert2</em> in <em>Feld2</em> usw. Sie müssen Werte durch Kommata trennen und Textfelder in einfache Anführungszeichen (' ') einschließen.</span><span class="sxs-lookup"><span data-stu-id="92c82-p104">The values to insert into the specific fields of the new record. Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on. You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="92c82-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92c82-130">Remarks</span></span>

<span data-ttu-id="92c82-p105">Sie können die INSERT INTO-Anweisung verwenden, um einen einzelnen Datensatz einer Tabelle mit der Syntax der Anfügeabfrage für einzelne Datensätze hinzuzufügen. In diesem Fall gibt der Code den Namen und Wert für jedes Feld des Datensatzes an. Sie müssen jedes Feld des Datensatzes angeben, dem ein Wert zugewiesen werden soll, sowie einen Wert für dieses Feld. Wenn Sie nicht alle Felder angeben, wird der Standardwert oder **Null** für fehlende Spalten eingefügt. Datensätze werden am Ende der Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="92c82-p105">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above. In this case, your code specifies the name and value for each field of the record. You must specify each of the fields of the record that a value is to be assigned to and a value for that field. When you do not specify each field, the default value or **Null** is inserted for missing columns. Records are added to the end of the table.</span></span>

<span data-ttu-id="92c82-136">INSERT INTO-Anweisung können Sie auch eine Gruppe von Datensätzen aus einer anderen Tabelle oder Abfrage mithilfe der auswählen anfügen...</span><span class="sxs-lookup"><span data-stu-id="92c82-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="92c82-137">FROM-Klausel, wie oben dargestellt, in der mehrere Datensätze Append-Abfragesyntax.</span><span class="sxs-lookup"><span data-stu-id="92c82-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="92c82-138">In diesem Fall gibt die SELECT-Klausel die Felder an die angegebene *Ziel* -Tabelle anfügen.</span><span class="sxs-lookup"><span data-stu-id="92c82-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="92c82-139">Die *Quell-* oder *Ziel* -Tabelle kann eine Tabelle oder Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="92c82-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="92c82-140">Wenn eine Abfrage angegeben wird, fügt das Microsoft Access-Datenbankmodul Datensätze an alle in der Abfrage angegebenen Tabellen an.</span><span class="sxs-lookup"><span data-stu-id="92c82-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="92c82-141">INSERT INTO ist optional. Wenn es eingeschlossen wird, steht es aber vor der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="92c82-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="92c82-142">Wenn die Zieltabelle einen Primärschlüssel enthält, stellen Sie sicher, dass Sie eindeutige Nicht-**Null**-Werte an das Primärschlüsselfeld bzw. die Primärschlüsselfelder anfügen. Andernfalls fügt das Microsoft Access-Datenbankmodul die Datensätze nicht an.</span><span class="sxs-lookup"><span data-stu-id="92c82-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="92c82-p108">Wenn Sie Datensätze an eine Tabelle mit einem "AutoNumber"-Feld anfügen und die angefügten Datensätze neu nummerieren möchten, schließen Sie das Feld "AutoNumber" nicht in die Abfrage ein, Schließen Sie das Feld "AutoNumber" in die Abfrage ein, wenn Sie die ursprünglichen Werte aus dem Feld beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="92c82-p108">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query. Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="92c82-145">Verwenden Sie die IN-Klausel, um Datensätze an eine Tabelle in einer anderen Datenbank anzufügen.</span><span class="sxs-lookup"><span data-stu-id="92c82-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="92c82-146">Um eine neue Tabelle zu erstellen, verwenden Sie stattdessen die [SELECT… INTO](select-into-statement-microsoft-access-sql.md)-Anweisung, um eine Tabellenerstellungsabfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="92c82-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="92c82-147">Um herauszufinden, welche Datensätze angefügt werden, bevor Sie die Anfügeabfrage ausführen, müssen Sie zuerst eine Auswahlabfrage ausführen, die die gleichen Auswahlkriterien verwendet, und sich die Ergebnisse ansehen.</span><span class="sxs-lookup"><span data-stu-id="92c82-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="92c82-p109">Eine Anfügeabfrage kopiert Datensätze aus einer oder mehreren Tabellen in eine andere. Die Tabellen mit den Datensätzen, die Sie anfügen, werden von der Anfügeabfrage nicht beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="92c82-p109">An append query copies records from one or more tables to another. The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="92c82-p110">Anstatt vorhandene Datensätze aus einer anderen Tabelle anzufügen, können Sie den Wert für die einzelnen Felder in einem einzigen neuen Datensatz mit der VALUES-Klausel angeben. Wenn Sie die Feldliste auslassen, muss die VALUES-Klausel einen Wert für jedes Feld in der Tabelle enthalten. Andernfalls schlägt der INSERT-Vorgang fehl. Verwenden Sie eine zusätzliche INSERT INTO-Anweisung mit einer VALUES-Klausel für jeden zusätzlichen Datensatz, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="92c82-p110">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause. If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail. Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="92c82-153">**Links bereitgestellt werden, von** der Community [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="92c82-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="92c82-154">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="92c82-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="92c82-155">Generieren fortlaufender Nummern für INSERT/UPDATE-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="92c82-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="92c82-156">SQL-zu-VBA-Formatierungsprogramm</span><span class="sxs-lookup"><span data-stu-id="92c82-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="92c82-157">Beispiel</span><span class="sxs-lookup"><span data-stu-id="92c82-157">Example</span></span>

<span data-ttu-id="92c82-p112">Dieses Beispiel wählt alle Datensätze in einer hypothetischen Tabelle "New Customers" aus und fügt sie der Tabelle "Customers" hinzu. Wenn einzelne Spalten nicht angegeben werden, müssen die SELECT-Tabellenspaltennamen exakt mit denen in der INSERT INTO-Tabelle übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="92c82-p112">This example selects all records in a hypothetical New Customers table and adds them to the Customers table. When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="92c82-160">Dieses Beispiel erstellt einen neuen Datensatz in der Tabelle "Employees".</span><span class="sxs-lookup"><span data-stu-id="92c82-160">This example creates a new record in the Employees table.</span></span>

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```


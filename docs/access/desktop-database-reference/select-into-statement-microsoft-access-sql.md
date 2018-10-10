---
title: SELECT.INTO-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT.INTO Statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4122421642b9746b5832984bf784faf65c603fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473216"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="2c26a-102">SELECT.INTO-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2c26a-102">SELECT.INTO Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="2c26a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c26a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2c26a-104">Erstellt eine make-table-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="2c26a-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c26a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c26a-105">Syntax</span></span>

<span data-ttu-id="2c26a-106">SELECT *Feld1*\[, *Feld2*\[,... \] \] INTO *neue Tabelle* \[IN *externe Datenbank* \] aus der *Datenquelle*</span><span class="sxs-lookup"><span data-stu-id="2c26a-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="2c26a-107">Die Anweisung SELECT…INTO besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="2c26a-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c26a-108">Teil</span><span class="sxs-lookup"><span data-stu-id="2c26a-108">Part</span></span></p></th>
<th><p><span data-ttu-id="2c26a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c26a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c26a-110"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="2c26a-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="2c26a-111">Die Namen der Felder, die in die neue Tabelle kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c26a-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c26a-112"><em>neueTabelle</em></span><span class="sxs-lookup"><span data-stu-id="2c26a-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="2c26a-113">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2c26a-113">The name of the table to be created.</span></span> <span data-ttu-id="2c26a-114">Er muss den üblichen Benennungskonventionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2c26a-114">It must conform to standard naming conventions.</span></span> <span data-ttu-id="2c26a-115">Wenn die <em>neue Tabelle</em> den Namen einer vorhandenen Tabelle identisch ist, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2c26a-115">If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c26a-116"><em>externeDatenbank</em></span><span class="sxs-lookup"><span data-stu-id="2c26a-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="2c26a-p102">Der Pfad zu einer externen Datenbank. Eine Beschreibung des Pfads finden Sie unter der <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">IN</a>-Klausel.  </span><span class="sxs-lookup"><span data-stu-id="2c26a-p102">The path to an external database. For a description of the path, see the <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c26a-119"><em>Quelle</em></span><span class="sxs-lookup"><span data-stu-id="2c26a-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="2c26a-p103">Der Name einer bereits bestehenden Tabelle, in der Datensätze ausgewählt werden. Dabei kann es es sich um eine oder mehrere Tabellen sowie eine Abfrage handeln.</span><span class="sxs-lookup"><span data-stu-id="2c26a-p103">The name of the existing table from which records are selected. This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2c26a-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c26a-122">Remarks</span></span>

<span data-ttu-id="2c26a-p104">Sie können make-table-Abfragen zur Archivierung von Datensätzen, Sicherung Ihrer Tabellen, Anlage von Kopien zum Export in eine andere Datenbank oder als Grundlage für Berichte auf Basis der Daten aus einem bestimmten Zeitraum verwenden. Beispielsweise könnten Sie  mithilfe derselben make-table-Abfrage monatlich einen Bericht über die Verkäufe in diesem Monat nach Region erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c26a-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="2c26a-p105">Möglicherweise sollten Sie einen Primärschlüssel für die neue Tabelle festlegen. Bei der Erstellung der Tabelle werden die Datentypen und Feldgrößen aller Felder der der Abfrage zugrunde liegenden Tabellen an die Felder der neuen Tabelle vererbt. Es werden jedoch keine weiteren Feld- oder Tabelleneigenschaften übertragen.</span><span class="sxs-lookup"><span data-stu-id="2c26a-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span></P>
> <LI>
> <P><span data-ttu-id="2c26a-127">Um einer bereits bestehenden Tabelle Daten hinzuzufügen, verwenden Sie die <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A>-Anweisung anstelle einer Anfügeabfrage.</span><span class="sxs-lookup"><span data-stu-id="2c26a-127">To add data to an existing table, use the <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A> statement instead to create an append query.</span></span></P>
> <LI>
> <P><span data-ttu-id="2c26a-128">Um herauszufinden, welche Datensätze ausgewählt werden, bevor Sie die make-table-Abfrage ausführen, führen Sie erst einmal eine <A href="select-statement-microsoft-access-sql.md">SELECT</A>-Anweisung mit denselben Auswahlkriterien aus.</span><span class="sxs-lookup"><span data-stu-id="2c26a-128">To find out which records will be selected before you run the make-table query, first examine the results of a <A href="select-statement-microsoft-access-sql.md">SELECT</A> statement that uses the same selection criteria.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="2c26a-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c26a-129">Example</span></span>

<span data-ttu-id="2c26a-130">In diesem Beispiel werden alle Datensätze in der Tabelle "Employees" ausgewählt und in eine neue Tabelle namens "Emp Backup" kopiert.</span><span class="sxs-lookup"><span data-stu-id="2c26a-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```

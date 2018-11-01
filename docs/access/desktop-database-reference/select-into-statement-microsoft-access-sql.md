---
title: WÄHLEN SIE AUS. INTO-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a744f67eba768ac2924d73782dbe70fd57e0333c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885535"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="dc0ac-102">WÄHLEN SIE AUS. INTO-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="dc0ac-102">SELECT.INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="dc0ac-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc0ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc0ac-104">Erstellt eine make-table-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc0ac-105">Syntax</span></span>

<span data-ttu-id="dc0ac-106">SELECT *Feld1*\[, *Feld2*\[,... \] \] INTO *neue Tabelle* \[IN *externe Datenbank* \] aus der *Datenquelle*</span><span class="sxs-lookup"><span data-stu-id="dc0ac-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="dc0ac-107">Die Anweisung SELECT…INTO besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="dc0ac-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc0ac-108">Teil</span><span class="sxs-lookup"><span data-stu-id="dc0ac-108">Part</span></span></p></th>
<th><p><span data-ttu-id="dc0ac-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc0ac-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc0ac-110"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="dc0ac-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="dc0ac-111">Die Namen der Felder, die in die neue Tabelle kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc0ac-112"><em>neueTabelle</em></span><span class="sxs-lookup"><span data-stu-id="dc0ac-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="dc0ac-113">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-113">The name of the table to be created.</span></span> <span data-ttu-id="dc0ac-114">Er muss den üblichen Benennungskonventionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-114">It must conform to standard naming conventions.</span></span> <span data-ttu-id="dc0ac-115">Wenn die <em>neue Tabelle</em> den Namen einer vorhandenen Tabelle identisch ist, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-115">If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc0ac-116"><em>externeDatenbank</em></span><span class="sxs-lookup"><span data-stu-id="dc0ac-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="dc0ac-p102">Der Pfad zu einer externen Datenbank. Eine Beschreibung des Pfads finden Sie unter der <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>-Klausel.  </span><span class="sxs-lookup"><span data-stu-id="dc0ac-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc0ac-119"><em>Quelle</em></span><span class="sxs-lookup"><span data-stu-id="dc0ac-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="dc0ac-p103">Der Name einer bereits bestehenden Tabelle, in der Datensätze ausgewählt werden. Dabei kann es es sich um eine oder mehrere Tabellen sowie eine Abfrage handeln.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-p103">The name of the existing table from which records are selected. This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dc0ac-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc0ac-122">Remarks</span></span>

<span data-ttu-id="dc0ac-p104">Sie können make-table-Abfragen zur Archivierung von Datensätzen, Sicherung Ihrer Tabellen, Anlage von Kopien zum Export in eine andere Datenbank oder als Grundlage für Berichte auf Basis der Daten aus einem bestimmten Zeitraum verwenden. Beispielsweise könnten Sie  mithilfe derselben make-table-Abfrage monatlich einen Bericht über die Verkäufe in diesem Monat nach Region erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc0ac-p105">Möglicherweise sollten Sie einen Primärschlüssel für die neue Tabelle festlegen. Bei der Erstellung der Tabelle werden die Datentypen und Feldgrößen aller Felder der der Abfrage zugrunde liegenden Tabellen an die Felder der neuen Tabelle vererbt. Es werden jedoch keine weiteren Feld- oder Tabelleneigenschaften übertragen.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="dc0ac-127">Um einer bereits bestehenden Tabelle Daten hinzuzufügen, verwenden Sie die [INSERT INTO](insert-into-statement-microsoft-access-sql.md)-Anweisung anstelle einer Anfügeabfrage.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="dc0ac-128">Um herauszufinden, welche Datensätze ausgewählt werden, bevor Sie die make-table-Abfrage ausführen, führen Sie erst einmal eine [SELECT](select-statement-microsoft-access-sql.md)-Anweisung mit denselben Auswahlkriterien aus.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="dc0ac-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dc0ac-129">Example</span></span>

<span data-ttu-id="dc0ac-130">In diesem Beispiel werden alle Datensätze in der Tabelle "Employees" ausgewählt und in eine neue Tabelle namens "Emp Backup" kopiert.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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

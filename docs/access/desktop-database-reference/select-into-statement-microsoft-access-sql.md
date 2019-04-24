---
title: SELECT.INTO-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308722"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="dc481-102">SELECT.INTO-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="dc481-102">SELECT…INTO Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="dc481-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc481-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc481-104">Erstellt eine make-table-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="dc481-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc481-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc481-105">Syntax</span></span>

<span data-ttu-id="dc481-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span><span class="sxs-lookup"><span data-stu-id="dc481-106">SELECT field1[, field2[, …]] INTO newtable [IN externaldatabase] 
    FROM source</span></span>

<span data-ttu-id="dc481-107">Die Anweisung SELECT…INTO besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="dc481-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc481-108">Part</span><span class="sxs-lookup"><span data-stu-id="dc481-108">Part</span></span></p></th>
<th><p><span data-ttu-id="dc481-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc481-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc481-110"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="dc481-110"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="dc481-111">Die Namen der Felder, die in die neue Tabelle kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc481-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc481-112"><em>neue_Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="dc481-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="dc481-p101">Der Name der zu erstellenden Tabelle. Er muss den üblichen Benennungskonventionen entsprechen. Wenn <em>neueTabelle</em> denselben Namen wie eine bereits vorhanden Tabelle hat, tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="dc481-p101">The name of the table to be created. It must conform to standard naming conventions. If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc481-116"><em>externeDatenbank</em></span><span class="sxs-lookup"><span data-stu-id="dc481-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="dc481-p102">Ich bin für diese Woche leider bereits ausgebucht. Eine Beschreibung des Pfads finden Sie unter der <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>-Klausel.</span><span class="sxs-lookup"><span data-stu-id="dc481-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc481-119"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="dc481-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="dc481-p103">Der Name der vorhandenen Tabelle, in der Datensätze ausgewählt werden. Dabei kann es sich um eine einzelne oder mehrere Tabellen oder eine Abfrage handeln.</span><span class="sxs-lookup"><span data-stu-id="dc481-p103">The name of the existing table from which records are selected. This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dc481-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc481-122">Remarks</span></span>

<span data-ttu-id="dc481-p104">Mithilfe von Tabellenerstellungsabfragen können Sie Datensätze archivieren, Sicherungskopien der Tabellen erstellen, Kopien zum Exportieren in eine andere Datenbank erstellen oder Berichte anfertigen, die Daten für einen bestimmten Zeitraum enthalten. Beispielsweise könnten Sie einen Bericht "Monatsumsatz nach Region" erstellen, indem Sie jeden Monat dieselbe Tabellenerstellungsabfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc481-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc481-p105">Möglicherweise sollten Sie einen Primärschlüssel für die neue Tabelle festlegen. Bei der Erstellung der Tabelle werden die Datentypen und Feldgrößen aller Felder der der Abfrage zugrunde liegenden Tabellen an die Felder der neuen Tabelle vererbt. Es werden jedoch keine weiteren Feld- oder Tabelleneigenschaften übertragen.</span><span class="sxs-lookup"><span data-stu-id="dc481-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="dc481-127">Um einer bereits bestehenden Tabelle Daten hinzuzufügen, verwenden Sie die [INSERT INTO](insert-into-statement-microsoft-access-sql.md)-Anweisung anstelle einer Anfügeabfrage.</span><span class="sxs-lookup"><span data-stu-id="dc481-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="dc481-128">Um herauszufinden, welche Datensätze ausgewählt werden, bevor Sie die make-table-Abfrage ausführen, führen Sie erst einmal eine [SELECT](select-statement-microsoft-access-sql.md)-Anweisung mit denselben Auswahlkriterien aus.</span><span class="sxs-lookup"><span data-stu-id="dc481-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="dc481-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dc481-129">Example</span></span>

<span data-ttu-id="dc481-130">In diesem Beispiel werden alle Datensätze in der Tabelle "Employees" ausgewählt und in eine neue Tabelle namens "Emp Backup" kopiert.</span><span class="sxs-lookup"><span data-stu-id="dc481-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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

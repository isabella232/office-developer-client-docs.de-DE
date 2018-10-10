---
title: DELETE-Anweisung (Microsoft Access SQL)
TOCTitle: DELETE Statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8a0d78350a9689af67f33262ff510d8638de40c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474391"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="26112-102">DELETE Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="26112-102">DELETE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="26112-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="26112-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="26112-104">Erstellt eine Löschabfrage, die Datensätze aus einer oder mehreren Tabellen in der [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\))-Klausel löscht, die die Kriterien der [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\))-Klausel erfüllen.</span><span class="sxs-lookup"><span data-stu-id="26112-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause that satisfy the [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="26112-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26112-105">Syntax</span></span>

<span data-ttu-id="26112-106">Löschen von \[ *Tabelle*. \* \] Aus *Tabelle* WHERE *Kriterien*</span><span class="sxs-lookup"><span data-stu-id="26112-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="26112-107">Die DELETE-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="26112-107">The DELETE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26112-108">Komponente</span><span class="sxs-lookup"><span data-stu-id="26112-108">Part</span></span></p></th>
<th><p><span data-ttu-id="26112-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26112-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26112-110"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="26112-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="26112-111">Der optionale Name der Tabelle aus der Datensätze gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="26112-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26112-112"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="26112-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="26112-113">Der Name der Tabelle, aus der Datensätze gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="26112-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26112-114"><em>Kriterien</em></span><span class="sxs-lookup"><span data-stu-id="26112-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="26112-115">Ein Ausdruck, der bestimmt, welche Datensätze gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26112-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="26112-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26112-116">Remarks</span></span>

<span data-ttu-id="26112-117">Die DELETE-Anweisung ist besonders hilfreich, wenn viele Datensätze gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26112-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="26112-p101">Wenn Sie eine Tabelle vollständig aus der Datenbank löschen möchten, können Sie die **Execute**-Methode mit einer [DROP](drop-statement-microsoft-access-sql.md)-Anweisung verwenden. Beim Löschen der Tabelle geht allerdings auch die Struktur verloren. Wenn Sie dagegen die DELETE-Anweisung verwenden, werden nur die Daten gelöscht, die Tabellenstruktur und alle Tabelleneigenschaften wie Feldattribute und Indizes bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="26112-p101">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement. If you delete the table, however, the structure is lost. In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="26112-p102">Sie können die DELETE-Anweisung verwenden, um Datensätze aus Tabellen zu entfernen, die in einer 1:n-Beziehung mit anderen Tabellen stehen. Durch Löschweitergaben werden Datensätze in Tabellen, die sich auf der n-Seite der Beziehung befinden, gelöscht, wenn der entsprechende Datensatz auf der 1-Seite der Beziehung in der Abfrage gelöscht wird. In der Beziehung zwischen der Customers-Tabelle (Kunden) und der Orders-Tabelle (Bestellungen) stellt erstgenannte Tabelle die 1-Seite und letztgenannte Tabelle die n-Seite der Beziehung zwischen den Tabellen dar. Wird ein Datensatz aus der Customers-Tabelle gelöscht, werden die entsprechenden Datensätze auch aus der Orders-Tabelle gelöscht, wenn die Option für Löschweitergaben angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="26112-p102">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables. Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query. For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship. Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="26112-p103">Über eine Löschabfrage werden Datensätze vollständig gelöscht, nicht nur die Daten in spezifischen Feldern. Wenn Sie Daten aus einem spezifischen Feld löschen möchten, erstellen Sie eine Aktualisierungabfrage, die die Werte in diesen Feldern in den Wert **Null** ändert.</span><span class="sxs-lookup"><span data-stu-id="26112-p103">A delete query deletes entire records, not just data in specific fields. If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="26112-p104">Nachdem Sie Datensätze über eine Löschabfrage entfernt haben, können Sie diesen Vorgang nicht rückgängig machen. Wenn Sie zunächst wissen möchten, welche Datensätze gelöscht werden, überprüfen Sie im Vorfeld die Ergebnisse einer Auswahlabfrage, die die gleichen Kriterien wie die Löschabfrage verwendet, und führen Sie dann erst die Löschabfrage aus.</span><span class="sxs-lookup"><span data-stu-id="26112-p104">After you remove records using a delete query, you cannot undo the operation. If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="26112-p105">Bewahren Sie immer eine Sicherungskopie Ihrer Daten auf. Auf diese Weise können Sie irrtümlich gelöschte Datensätze aus den Sicherungskopien abrufen.</span><span class="sxs-lookup"><span data-stu-id="26112-p105">Maintain backup copies of your data at all times. If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="26112-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="26112-131">Example</span></span>

<span data-ttu-id="26112-p106">Im folgenden Beispiel werden alle Datensätze der Mitarbeiter gelöscht, die über die Position eines Trainees verfügen. Wenn die FROM-Klausel nur eine Tabelle einschließt, muss der Tabellenname nicht in der DELETE-Anweisung aufgelistet werden.

</span><span class="sxs-lookup"><span data-stu-id="26112-p106">This example deletes all records for employees whose title is Trainee. When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```

---
title: DROP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293651"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="5a9f2-102">DROP-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="5a9f2-102">DROP Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="5a9f2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a9f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a9f2-104">Löscht eine vorhandene Tabelle, Prozedur oder Sicht aus einer Datenbank, oder löscht einen vorhandenen Index aus einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="5a9f2-p101">Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der DROP-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen. Verwenden Sie stattdessen die **Delete**-Methode für Datenzugriffsobjekte (DAO).</span><span class="sxs-lookup"><span data-stu-id="5a9f2-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a9f2-107">Syntax</span></span>

<span data-ttu-id="5a9f2-108">DROP {TABLE *Tabelle* | INDEX *Index* ON *Tabelle* | PROCEDURE *Prozedur* | VIEW *Sicht*}</span><span class="sxs-lookup"><span data-stu-id="5a9f2-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="5a9f2-109">Die DROP-Anweisung setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="5a9f2-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a9f2-110">Part</span><span class="sxs-lookup"><span data-stu-id="5a9f2-110">Part</span></span></p></th>
<th><p><span data-ttu-id="5a9f2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a9f2-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a9f2-112"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="5a9f2-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="5a9f2-113">Der Name der zu löschenden Tabelle oder der Tabelle, aus der ein Index gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9f2-114"><em>Prozedur</em></span><span class="sxs-lookup"><span data-stu-id="5a9f2-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="5a9f2-115">Der Name der zu löschenden Prozedur.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a9f2-116"><em>Sicht</em></span><span class="sxs-lookup"><span data-stu-id="5a9f2-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="5a9f2-117">Der Name der zu löschenden Sicht.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a9f2-118"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="5a9f2-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="5a9f2-119">Der Name des aus der <em>Tabelle</em> zu löschenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5a9f2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a9f2-120">Remarks</span></span>

<span data-ttu-id="5a9f2-121">Sie müssen die Tabelle schließen, bevor Sie sie löschen oder einen Index daraus entfernen können.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="5a9f2-122">Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index aus einer Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="5a9f2-p102">Die [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung kann zum Erstellen einer Tabelle und die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)- oder ALTER TABLE-Anweisung zum Erstellen eines Indexes verwendet werden. Verwenden Sie die ALTER TABLE-Anweisung ebenfalls, wenn Sie eine Tabelle ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="5a9f2-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a9f2-125">Example</span></span>

<span data-ttu-id="5a9f2-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="5a9f2-127">This example deletes the index MyIndex from the Employees table.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-127">This example deletes the index MyIndex from the Employees table.</span></span>

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="5a9f2-128">This example deletes the Employees table from the database.</span><span class="sxs-lookup"><span data-stu-id="5a9f2-128">This example deletes the Employees table from the database.</span></span>

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```

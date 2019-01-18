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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718294"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="296f7-102">DROP-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="296f7-102">DROP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="296f7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="296f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="296f7-104">Löscht eine vorhandene Tabelle, Prozedur oder Sicht aus einer Datenbank, oder löscht einen vorhandenen Index aus einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="296f7-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="296f7-p101">[!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der DROP-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen. Verwenden Sie stattdessen die **Delete** -Methode für Datenzugriffsobjekte (DAO).</span><span class="sxs-lookup"><span data-stu-id="296f7-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="296f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="296f7-107">Syntax</span></span>

<span data-ttu-id="296f7-108">DROP {TABLE *Tabelle* | INDEX *Index* ON *Tabelle* | PROCEDURE *Prozedur* | VIEW *Sicht*}</span><span class="sxs-lookup"><span data-stu-id="296f7-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="296f7-109">Die DROP-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="296f7-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="296f7-110">Komponente</span><span class="sxs-lookup"><span data-stu-id="296f7-110">Part</span></span></p></th>
<th><p><span data-ttu-id="296f7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="296f7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="296f7-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="296f7-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="296f7-113">Der Name der zu löschenden Tabelle oder der Tabelle, die den zu löschenden Index enthält.</span><span class="sxs-lookup"><span data-stu-id="296f7-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f7-114"><em>Prozedur</em></span><span class="sxs-lookup"><span data-stu-id="296f7-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="296f7-115">Der Name der zu löschenden Prozedur.</span><span class="sxs-lookup"><span data-stu-id="296f7-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="296f7-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="296f7-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="296f7-117">Der Name der zu löschenden Sicht.</span><span class="sxs-lookup"><span data-stu-id="296f7-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="296f7-118"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="296f7-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="296f7-119">Der Name des aus der <em>Tabelle</em> zu löschenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="296f7-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="296f7-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="296f7-120">Remarks</span></span>

<span data-ttu-id="296f7-121">Die Tabelle muss geschlossen werden, bevor ein Index daraus gelöscht oder entfernt werden kann.</span><span class="sxs-lookup"><span data-stu-id="296f7-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="296f7-122">Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index aus einer Tabelle zu löschen.</span><span class="sxs-lookup"><span data-stu-id="296f7-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="296f7-p102">Die [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung kann zum Erstellen einer Tabelle und die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)- oder ALTER TABLE-Anweisung zum Erstellen eines Indexes verwendet werden. Verwenden Sie die ALTER TABLE-Anweisung ebenfalls, wenn Sie eine Tabelle ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="296f7-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="296f7-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="296f7-125">Example</span></span>

<span data-ttu-id="296f7-126">Im folgenden Beispiel wird davon ausgegangen, dass der hypothetische NewIndex-Index zur Angabe eines neuen Indexes in der Employees-Tabelle (Personal) in der Datenbank Northwind.mdb (Nordwind.mdb) vorhanden ist. 

</span><span class="sxs-lookup"><span data-stu-id="296f7-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="296f7-127">Im folgenden Beispiel wird der MyIndex-Index aus der Employees-Tabelle (Personal) gelöscht.

</span><span class="sxs-lookup"><span data-stu-id="296f7-127">This example deletes the index MyIndex from the Employees table.</span></span>

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

<span data-ttu-id="296f7-128">Im folgenden Beispiel wird die Employees-Tabelle (Personal) aus der Datenbank gelöscht.

</span><span class="sxs-lookup"><span data-stu-id="296f7-128">This example deletes the Employees table from the database.</span></span>

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

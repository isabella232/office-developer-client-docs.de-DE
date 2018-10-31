---
title: UPDATE-Anweisung (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7a761fbc6404cf72818271b956bfc63516942d25
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863283"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="fbbb5-102">UPDATE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fbbb5-102">UPDATE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="fbbb5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbbb5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fbbb5-104">Erstellt eine Aktualisierungsabfrage, die Werte in Feldern in einer angegebenen Tabelle basierend auf angegebenen Kriterien ändert.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbb5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbbb5-105">Syntax</span></span>

<span data-ttu-id="fbbb5-106">UPDATE *Tabelle* SET *Neuer Wert* WHERE *Kriterien*;</span><span class="sxs-lookup"><span data-stu-id="fbbb5-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span></span>

<span data-ttu-id="fbbb5-107">Die UPDATE-Anweisung hat diese Teile:</span><span class="sxs-lookup"><span data-stu-id="fbbb5-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbbb5-108">Teil</span><span class="sxs-lookup"><span data-stu-id="fbbb5-108">Part</span></span></p></th>
<th><p><span data-ttu-id="fbbb5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbbb5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbbb5-110"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="fbbb5-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="fbbb5-111">Der Name der Tabelle mit den zu ändernden Daten.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbbb5-112"><em>newvalue</em></span><span class="sxs-lookup"><span data-stu-id="fbbb5-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="fbbb5-113">Ein Ausdruck, der den Wert bestimmt, der in ein bestimmtes Feld in die aktualisierten Datensätze eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbbb5-114"><em>Kriterien</em></span><span class="sxs-lookup"><span data-stu-id="fbbb5-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="fbbb5-p101">Ein Ausdruck, der bestimmt, welche Datensätze aktualisiert werden. Nur Datensätze, die dem Ausdruck entsprechen, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-p101">An expression that determines which records will be updated. Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fbbb5-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbbb5-117">Remarks</span></span>

<span data-ttu-id="fbbb5-118">UPDATE ist besonders dann nützlich, wenn Sie viele Datensätze ändern möchten oder wenn sich die zu ändernden Datensätze in mehreren Tabellen befinden.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="fbbb5-p102">Sie können mehrere Felder gleichzeitig ändern. Das folgende Beispiel erhöht für Versender in Großbritannien den Wert der Bestellmenge um zehn Prozent und den Wert der Fracht um drei Prozent.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-p102">You can change several fields at the same time. The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- <span data-ttu-id="fbbb5-p103">UPDATE generiert kein Resultset. Nach dem Aktualisieren von Datensätzen mit einer Aktualisierungsabfrage können Sie den Vorgang außerdem nicht rückgängig machen. Wenn Sie wissen möchten, welche Datensätze aktualisiert wurden, untersuchen Sie zunächst die Ergebnisse einer Auswahlabfrage, die die gleichen Kriterien verwendet, und führen Sie dann die Aktualisierungsabfrage aus.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-p103">UPDATE does not generate a result set. Also, after you update records using an update query, you cannot undo the operation. If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span>
- <span data-ttu-id="fbbb5-p104">Behalten Sie immer Sicherungskopien Ihrer Daten. Wenn Sie die falschen Datensätze aktualisieren, können Sie sie aus den Sicherungskopien abrufen.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-p104">Maintain backup copies of your data at all times. If you update the wrong records, you can retrieve them from your backup copies.</span></span>



## <a name="example"></a><span data-ttu-id="fbbb5-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fbbb5-126">Example</span></span>

<span data-ttu-id="fbbb5-127">Dieses Beispiel ändert Werte im Feld "ReportsTo" für alle Mitarbeiterdatensätze, für die "ReportsTo" aktuell auf den Wert "2" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fbbb5-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```

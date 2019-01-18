---
title: Recordset2.Sort-Eigenschaft (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722886"
---
# <a name="recordset2sort-property-dao"></a><span data-ttu-id="63df5-102">Recordset2.Sort-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="63df5-102">Recordset2.Sort property (DAO)</span></span>

<span data-ttu-id="63df5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63df5-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="63df5-104">Legt die Sortierreihenfolge für Datensätze in einem **[Recordset](recordset-object-dao.md)** -Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="63df5-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="63df5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63df5-105">Syntax</span></span>

<span data-ttu-id="63df5-106">*Ausdruck* . Sortieren</span><span class="sxs-lookup"><span data-stu-id="63df5-106">*expression* .Sort</span></span>

<span data-ttu-id="63df5-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="63df5-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="63df5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63df5-108">Remarks</span></span>

<span data-ttu-id="63df5-109">Sie können die **Sort** -Eigenschaft mit – und Snapshot – vom Typ Dynaset **Recordset** -Objekte.</span><span class="sxs-lookup"><span data-stu-id="63df5-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="63df5-p101">Wenn Sie diese Eigenschaft für ein Objekt festlegen, wird die Sortierung vorgenommen, wenn anhand dieses Objekts ein nachfolgendes **Recordset**-Objekt erstellt wird. Die Einstellung der **Sort**-Eigenschaft hat Vorrang vor allen für ein **[QueryDef](querydef-object-dao.md)** -Objekt festgelegten Sortierreihenfolgen.</span><span class="sxs-lookup"><span data-stu-id="63df5-p101">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object. The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="63df5-112">Die Standardsortierreihenfolge ist aufsteigend (A bis Z bzw. 0 bis 100).</span><span class="sxs-lookup"><span data-stu-id="63df5-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="63df5-113">Die **Sort** -Eigenschaft wird nicht auf Tabelle oder Weiterleiten – Typ **Recordset** -Objekte angewendet.</span><span class="sxs-lookup"><span data-stu-id="63df5-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="63df5-114">Um ein **Recordset** -Objekt vom Typ Tabelle sortieren möchten, verwenden Sie die **[Index](recordset2-index-property-dao.md)** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="63df5-114">To sort a table–type **Recordset** object, use the **[Index](recordset2-index-property-dao.md)** property.</span></span>

> [!NOTE]
> <span data-ttu-id="63df5-115">[!HINWEIS] In vielen Fällen ist es schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die die Sortierkriterien enthält.</span><span class="sxs-lookup"><span data-stu-id="63df5-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes the sorting criteria.</span></span>

## <a name="example"></a><span data-ttu-id="63df5-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="63df5-116">Example</span></span>

<span data-ttu-id="63df5-p103">In diesem Beispiel wird die **Sort** -Eigenschaft veranschaulicht, indem ihr Wert geändert und ein neues **Recordset** erstellt wird. Die SortOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63df5-p103">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**. The SortOutput function is required for this procedure to run.</span></span>

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="63df5-p104">Wenn Sie die auszuwählenden Daten kennen, ist es in der Regel effizienter, ein **Recordset** mit einer SQL-Anweisung zu erstellen. In diesem Beispiel wird gezeigt, wie Sie nur ein **Recordset** erstellen und die gleichen Ergebnisse wie im vorherigen Beispiel erhalten.</span><span class="sxs-lookup"><span data-stu-id="63df5-p104">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement. This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```

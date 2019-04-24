---
title: Recordset2. Sort-Eigenschaft (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309269"
---
# <a name="recordset2sort-property-dao"></a><span data-ttu-id="28601-102">Recordset2. Sort-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="28601-102">Recordset2.Sort property (DAO)</span></span>

<span data-ttu-id="28601-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28601-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="28601-104">Legt die Sortierreihenfolge für Datensätze in einem **[Recordset](recordset-object-dao.md)** -Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="28601-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="28601-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28601-105">Syntax</span></span>

<span data-ttu-id="28601-106">*Ausdruck* . Sortieren</span><span class="sxs-lookup"><span data-stu-id="28601-106">*expression* .Sort</span></span>

<span data-ttu-id="28601-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="28601-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="28601-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28601-108">Remarks</span></span>

<span data-ttu-id="28601-109">Sie können die **Sort**-Eigenschaft mit **Recordset**-Objekten vom Typ „Dynaset“ und „Snapshot“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="28601-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="28601-p101">Wenn Sie diese Eigenschaft für ein Objekt festlegen, wird die Sortierung vorgenommen, wenn anhand dieses Objekts ein nachfolgendes **Recordset**-Objekt erstellt wird. Die Einstellung der **Sort**-Eigenschaft hat Vorrang vor allen für ein **[QueryDef](querydef-object-dao.md)** -Objekt festgelegten Sortierreihenfolgen.</span><span class="sxs-lookup"><span data-stu-id="28601-p101">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object. The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="28601-112">Die Standardsortierreihenfolge ist aufsteigend (A bis Z bzw. 0 bis 100).</span><span class="sxs-lookup"><span data-stu-id="28601-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="28601-113">Die **Sort**-Eigenschaft gilt nicht für **Recordset**-Objekte vom Typ „Tabelle“ oder „Vorwärts“.</span><span class="sxs-lookup"><span data-stu-id="28601-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="28601-114">Verwenden Sie die **[Index](recordset2-index-property-dao.md)** -Eigenschaft, um ein **Recordset** -Objekt vom Typ Tabelle zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="28601-114">To sort a table–type **Recordset** object, use the **[Index](recordset2-index-property-dao.md)** property.</span></span>

> [!NOTE]
> <span data-ttu-id="28601-115">In vielen Fällen ist geht schneller, ein neues **Recordset**-Objekt mithilfe einer SQL-Anweisung zu öffnen, die die Sortierkriterien enthält.</span><span class="sxs-lookup"><span data-stu-id="28601-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes the sorting criteria.</span></span>

## <a name="example"></a><span data-ttu-id="28601-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28601-116">Example</span></span>

<span data-ttu-id="28601-p103">In diesem Beispiel wird die **Sort** -Eigenschaft veranschaulicht, indem ihr Wert geändert und ein neues **Recordset** erstellt wird. Die SortOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="28601-p103">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**. The SortOutput function is required for this procedure to run.</span></span>

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

<span data-ttu-id="28601-p104">Wenn Sie die auszuwählenden Daten kennen, ist es in der Regel effizienter, ein **Recordset** mit einer SQL-Anweisung zu erstellen. In diesem Beispiel wird gezeigt, wie Sie nur ein **Recordset** erstellen und die gleichen Ergebnisse wie im vorherigen Beispiel erhalten.</span><span class="sxs-lookup"><span data-stu-id="28601-p104">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement. This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

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

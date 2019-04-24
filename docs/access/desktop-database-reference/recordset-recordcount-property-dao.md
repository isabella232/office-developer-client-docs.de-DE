---
title: Recordset.RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307637"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="3374b-102">Recordset.RecordCount-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="3374b-102">Recordset.RecordCount Property (DAO)</span></span>

<span data-ttu-id="3374b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3374b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3374b-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span><span class="sxs-lookup"><span data-stu-id="3374b-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3374b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3374b-107">Syntax</span></span>

<span data-ttu-id="3374b-108">*expression* .RecordCount</span><span class="sxs-lookup"><span data-stu-id="3374b-108">expression  . RecordCount</span></span>

<span data-ttu-id="3374b-109">*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3374b-109">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3374b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3374b-110">Remarks</span></span>

<span data-ttu-id="3374b-111">Verwenden Sie die **RecordCount**-Eigenschaft, um herauszufinden, auf wie viele Datensätze in einem **Recordset**- oder **TableDef**-Objekt zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="3374b-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="3374b-112">Die **RecordCount**-Eigenschaft gibt erst an, wie viele Datensätze in einem **Recordset**-Objekt vom "dynaset"-, "snapshot"- oder "forward-only"-Typ enthalten sind, wenn auf alle Datensätze zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="3374b-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="3374b-113">Sobald auf den letzten Datensatz zugegriffen wurde, gibt die **RecordCount**-Eigenschaft die Gesamtzahl ungelöschter Datensätze im **Recordset**- oder **TableDef**-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3374b-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="3374b-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span><span class="sxs-lookup"><span data-stu-id="3374b-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="3374b-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span><span class="sxs-lookup"><span data-stu-id="3374b-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="3374b-p103">Die Verwendung der **MoveLast**-Methode zum Auffüllen eines neu geöffneten **Recordset**-Objekts hat negative Auswirkungen auf die Leistung. Sofern beim Öffnen eines **Recordset**-Objekts nicht sofort ein genauer **RecordCount**-Wert erforderlich ist, sollte das **Recordset**-Objekt mit anderen Codeteilen aufgefüllt werden, bevor die **RecordCount**-Eigenschaft geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3374b-p103">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance. Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="3374b-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span><span class="sxs-lookup"><span data-stu-id="3374b-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="3374b-121">Die **RecordCount**-Eigenschaft eines **Recordset**-Objekts vom "snapshot"- oder "forward-only"-Typ ist nicht von den Änderungen in zugrunde liegenden Tabellen betroffen.</span><span class="sxs-lookup"><span data-stu-id="3374b-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="3374b-122">Ein **Recordset**- oder **TableDef**-Objekt ohne Datensätze hat eine **RecordCount**-Eigenschaftseinstellung von "0".</span><span class="sxs-lookup"><span data-stu-id="3374b-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="3374b-123">Bei der Verwendung der **[Requery](recordset-requery-method-dao.md)** -Methode für ein **Recordset**-Objekt wird die **RecordCount**-Eigenschaft zurückgesetzt, so als würde die Abfrage erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3374b-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="3374b-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3374b-124">Example</span></span>

<span data-ttu-id="3374b-125">Dieses Beispiel demonstriert die **RecordCount**-Eigenschaft mit verschiedenen **Recordset**-Typen vor und nach der Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="3374b-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```

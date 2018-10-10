---
title: Recordset2.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 999cebd7fa038d3efeeac963ba6844545a41373a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476004"
---
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="becad-102">Recordset2.RecordCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="becad-102">Recordset2.RecordCount Property (DAO)</span></span>


<span data-ttu-id="becad-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="becad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="becad-p101">Gibt die Anzahl der Datensätze zurück, auf die in einem **[Recordset](recordset-object-dao.md)** -Objekt zugegriffen wird, oder die Gesamtzahl der Datensätze in einem **Recordset** -Objekt vom "table"-Typ oder in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschütztes **Long** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="becad-p101">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object. or **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="becad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="becad-107">Syntax</span></span>

<span data-ttu-id="becad-108">*Ausdruck* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="becad-108">*expression* .RecordCount</span></span>

<span data-ttu-id="becad-109">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="becad-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="becad-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="becad-110">Remarks</span></span>

<span data-ttu-id="becad-111">Verwenden Sie die **RecordCount** -Eigenschaft, um herauszufinden, auf wie viele Datensätze in einem **Recordset** - oder **TableDef** -Objekt zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="becad-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="becad-112">Die **RecordCount** -Eigenschaft gibt nicht an, wie viele Datensätze in einem Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt enthalten sind, bis alle Datensätze zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="becad-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="becad-113">Sobald auf den letzten Datensatz zugegriffen wurde, gibt die **RecordCount** -Eigenschaft die Gesamtzahl ungelöschter Datensätze im **Recordset** - oder **TableDef** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="becad-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="becad-114">Um den Zugriff auf den letzten Datensatz zu erzwingen, verwenden Sie die **[MoveLast](recordset2-movelast-method-dao.md)** -Methode für das **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="becad-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="becad-115">Sie können auch eine SQL- **Count** -Funktion verwenden, um die ungefähre Anzahl von Datensätzen zu bestimmen, die die Abfrage zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="becad-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>


> [!NOTE]
> <P><span data-ttu-id="becad-p103">[!HINWEIS] Die Verwendung der <STRONG>MoveLast</STRONG>-Methode zum Auffüllen eines neu geöffneten <STRONG>Recordset</STRONG>-Objekts hat negative Auswirkungen auf die Leistung. Sofern beim Öffnen eines <STRONG>Recordset</STRONG>-Objekts nicht sofort ein genauer <STRONG>RecordCount</STRONG>-Wert erforderlich ist, sollte das <STRONG>Recordset</STRONG>-Objekt mit anderen Codeteilen aufgefüllt werden, bevor die <STRONG>RecordCount</STRONG>-Eigenschaft geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="becad-p103">Using the <STRONG>MoveLast</STRONG> method to populate a newly opened <STRONG>Recordset</STRONG> negatively impacts performance. Unless it is necessary to have an accurate <STRONG>RecordCount</STRONG> as soon as you open a <STRONG>Recordset</STRONG>, it's better to wait until you populate the <STRONG>Recordset</STRONG> with other portions of code before checking the <STRONG>RecordCount</STRONG> property.</span></span></P>



<span data-ttu-id="becad-p104">Wenn Ihre Anwendung Datensätze in einem **Recordset** -Objekt vom "dynaset"-Typ löscht, nimmt der Wert der **RecordCount** -Eigenschaft ab. Datensätze, die von anderen Benutzern gelöscht werden, werden allerdings erst von der **RecordCount** -Eigenschaft wiedergegeben, wenn der aktuelle Datensatz auf einem gelöschten Datensatz positioniert wird. Wenn Sie eine Transaktion ausführen, die sich auf die Einstellung der **RecordCount** -Eigenschaft auswirkt und Sie dann ein Rollback für die Transaktion ausführen, gibt die **RecordCount** -Eigenschaft nicht die tatsächliche Anzahl verbleibender Datensätze wieder.</span><span class="sxs-lookup"><span data-stu-id="becad-p104">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases. However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record. If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="becad-121">Änderungen in den zugrunde liegenden Tabellen wirkt sich nicht auf die **RecordCount** -Eigenschaft eines **Recordset** -Objekts Snapshot oder vorwärts – Typ aus.</span><span class="sxs-lookup"><span data-stu-id="becad-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="becad-122">Die **RecordCount**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts ohne Datensätze hat den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="becad-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="becad-123">Bei der Verwendung der **[Requery](recordset2-requery-method-dao.md)** -Methode für ein **Recordset**-Objekt wird die **RecordCount**-Eigenschaft zurückgesetzt, so als würde die Abfrage erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="becad-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="becad-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="becad-124">Example</span></span>

<span data-ttu-id="becad-125">Dieses Beispiel veranschaulicht die **RecordCount**-Eigenschaft für unterschiedliche Typen von **Recordsets**-Objekten vor und nach ihrer Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="becad-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
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

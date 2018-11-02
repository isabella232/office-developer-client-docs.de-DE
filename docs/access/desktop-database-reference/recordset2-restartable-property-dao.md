---
title: Recordset2.Restartable-Eigenschaft (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5aea96ca6293583eaae8b6b1b8c913f1956c3919
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919822"
---
# <a name="recordset2restartable-property-dao"></a><span data-ttu-id="cbc8f-102">Recordset2.Restartable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="cbc8f-102">Recordset2.Restartable property (DAO)</span></span>


<span data-ttu-id="cbc8f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbc8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbc8f-104">Gibt einen Wert zurück, der angibt, ob ein **[Recordset](recordset-object-dao.md)** -Objekt die **[Requery](recordset2-requery-method-dao.md)** -Methode unterstützt, die die Abfrage, auf der das **Recordset**-Objekt basiert, erneut ausführt.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset2-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc8f-105">Syntax</span></span>

<span data-ttu-id="cbc8f-106">*Ausdruck* . Restartable</span><span class="sxs-lookup"><span data-stu-id="cbc8f-106">*expression* .Restartable</span></span>

<span data-ttu-id="cbc8f-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc8f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbc8f-108">Remarks</span></span>

<span data-ttu-id="cbc8f-109">Recordset-Objekte vom Typ Tabelle geben immer False zurück.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="cbc8f-p101">Überprüfen Sie die **Restartable**-Eigenschaft vor der Verwendung der **Requery**-Methode für ein **Recordset**-Objekt. Wenn die **Restartable**-Eigenschaft des Objekts den Wert **False** hat, verwenden Sie die **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode für das zugrunde liegende **[QueryDef](querydef-object-dao.md)** -Objekt, um die Abfrage erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-p101">Check the **Restartable** property before using the **Requery** method on a **Recordset** object. If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="cbc8f-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cbc8f-112">Example</span></span>

<span data-ttu-id="cbc8f-113">Dieses Beispiel veranschaulicht die **Restartable**-Eigenschaft für verschiedene **Recordset**-Objekte.</span><span class="sxs-lookup"><span data-stu-id="cbc8f-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

```vb
    Sub RestartableX()
    
       Dim dbsNorthwind As Database
       Dim rstTemp As Recordset2
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
          ' Open a table-type Recordset and print its 
          ' Restartable property.
          Set rstTemp = .OpenRecordset("Employees", dbOpenTable)
          Debug.Print _
             "Table-type recordset from Employees table"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from an SQL statement and print its 
          ' Restartable property.
          Set rstTemp = _
             .OpenRecordset("SELECT * FROM Employees")
          Debug.Print "Recordset based on SQL statement"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from a saved QueryDef object and 
          ' print its Restartable property.
          Set rstTemp = .OpenRecordset("Current Product List")
          Debug.Print _
             "Recordset based on permanent QueryDef (" & _
             rstTemp.Name & ")"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          .Close
       End With
    
    End Sub
```

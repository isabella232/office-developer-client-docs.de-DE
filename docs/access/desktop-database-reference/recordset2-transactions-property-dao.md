---
title: Recordset2. transActions-Eigenschaft (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309241"
---
# <a name="recordset2transactions-property-dao"></a><span data-ttu-id="6c582-102">Recordset2. transActions-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c582-102">Recordset2.Transactions property (DAO)</span></span>


<span data-ttu-id="6c582-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c582-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c582-104">Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c582-104">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="6c582-105">Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="6c582-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c582-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c582-106">Syntax</span></span>

<span data-ttu-id="6c582-107">*Ausdruck* . Transaktionen</span><span class="sxs-lookup"><span data-stu-id="6c582-107">*expression* .Transactions</span></span>

<span data-ttu-id="6c582-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c582-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c582-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c582-109">Remarks</span></span>

<span data-ttu-id="6c582-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span><span class="sxs-lookup"><span data-stu-id="6c582-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="6c582-111">Snapshot-und Forward-Type **[Recordset](recordset-object-dao.md)** -Objekte geben immer **false**zurück.</span><span class="sxs-lookup"><span data-stu-id="6c582-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="6c582-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span><span class="sxs-lookup"><span data-stu-id="6c582-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="6c582-p104">Überprüfen Sie die **Transactions**-Eigenschaft, bevor Sie die **[BeginTrans](dbengine-begintrans-method-dao.md)** -Methode für das [**Workspace**](workspace-object-dao.md) -Objekt des **Recordset**-Objekts verwenden, um sicherzustellen, dass Transaktionen unterstützt werden. Das Anwenden der Methoden **BeginTrans**, **CommitTrans** und **Rollback** auf nicht unterstützte Objekte hat keine Wirkung.</span><span class="sxs-lookup"><span data-stu-id="6c582-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="6c582-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c582-117">Example</span></span>

<span data-ttu-id="6c582-118">In diesem Beispiel wird die **Transactions**-Eigenschaft in Microsoft Access-Arbeitsbereichen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6c582-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```


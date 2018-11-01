---
title: Recordset.Transactions Property (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3b34f8f027b2e70ada94c6d15584cf25a4aec1c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873291"
---
# <a name="recordsettransactions-property-dao"></a><span data-ttu-id="3762a-102">Recordset.Transactions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="3762a-102">Recordset.Transactions Property (DAO)</span></span>


<span data-ttu-id="3762a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3762a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3762a-p101">Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="3762a-p101">Returns a value that indicates whether an object supports transactions. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3762a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3762a-106">Syntax</span></span>

<span data-ttu-id="3762a-107">*Ausdruck* . Transaktionen</span><span class="sxs-lookup"><span data-stu-id="3762a-107">*expression* .Transactions</span></span>

<span data-ttu-id="3762a-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3762a-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3762a-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3762a-109">Remarks</span></span>

<span data-ttu-id="3762a-p102">In einem Microsoft Access-Arbeitsbereich können Sie auch die Transactions-Eigenschaft auf Recordset-Objekte vom Typ Dynaset oder Tabelle anwenden. Recordset-Objekte vom Typ Snapshot und vorwärtsgerichtet geben immer False zurück.</span><span class="sxs-lookup"><span data-stu-id="3762a-p102">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects. Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="3762a-p103">Wenn ein Recordset-Objekt vom Typ Dynaset oder Tabelle auf einer Tabelle einer Microsoft Access-Datenbank-Engine basiert, hat die Transactions-Eigenschaft den Wert True, und Sie können Transaktionen verwenden. Andere Datenbank-Engines unterstützen möglicherweise keine Transaktionen. In einem Recordset-Objekt vom Typ Dynaset, das auf einer Paradox-Tabelle basiert, können z. B. keine Transaktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3762a-p103">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="3762a-p104">Überprüfen Sie die **Transactions**-Eigenschaft, bevor Sie die **[BeginTrans](dbengine-begintrans-method-dao.md)** -Methode für das [**Workspace**](workspace-object-dao.md) -Objekt des **Recordset**-Objekts verwenden, um sicherzustellen, dass Transaktionen unterstützt werden. Das Anwenden der Methoden **BeginTrans**, **CommitTrans** und **Rollback** auf nicht unterstützte Objekte hat keine Wirkung.</span><span class="sxs-lookup"><span data-stu-id="3762a-p104">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported. Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="3762a-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3762a-117">Example</span></span>

<span data-ttu-id="3762a-118">In diesem Beispiel wird die **Transactions**-Eigenschaft in Microsoft Access-Arbeitsbereichen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3762a-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

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


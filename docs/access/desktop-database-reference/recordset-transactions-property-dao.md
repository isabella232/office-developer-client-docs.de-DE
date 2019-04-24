---
title: Recordset. transActions-Eigenschaft (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b23568e0830ef07e58119d02c4d221dad4b1d015
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307595"
---
# <a name="recordsettransactions-property-dao"></a>Recordset. transActions-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter **Boolean**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Transaktionen

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects. Snapshot-und Forward-Type **[Recordset](recordset-object-dao.md)** -Objekte geben immer **false**zurück.

If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions. Other database engines may not support transactions. For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.

Überprüfen Sie die **Transactions**-Eigenschaft, bevor Sie die **[BeginTrans](dbengine-begintrans-method-dao.md)** -Methode für das [**Workspace**](workspace-object-dao.md) -Objekt des **Recordset**-Objekts verwenden, um sicherzustellen, dass Transaktionen unterstützt werden. Das Anwenden der Methoden **BeginTrans**, **CommitTrans** und **Rollback** auf nicht unterstützte Objekte hat keine Wirkung.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Transactions**-Eigenschaft in Microsoft Access-Arbeitsbereichen veranschaulicht.

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


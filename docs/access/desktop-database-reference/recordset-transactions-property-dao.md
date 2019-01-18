---
title: Recordset.Transactions-Eigenschaft (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b23568e0830ef07e58119d02c4d221dad4b1d015
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709635"
---
# <a name="recordsettransactions-property-dao"></a>Recordset.Transactions-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter **Boolean**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Transaktionen

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

In einem Microsoft Access-Arbeitsbereich können Sie auch die Transactions-Eigenschaft auf Recordset-Objekte vom Typ Dynaset oder Tabelle anwenden. Recordset-Objekte vom Typ Snapshot und vorwärtsgerichtet geben immer False zurück.

Wenn ein Recordset-Objekt vom Typ Dynaset oder Tabelle auf einer Tabelle einer Microsoft Access-Datenbank-Engine basiert, hat die Transactions-Eigenschaft den Wert True, und Sie können Transaktionen verwenden. Andere Datenbank-Engines unterstützen möglicherweise keine Transaktionen. In einem Recordset-Objekt vom Typ Dynaset, das auf einer Paradox-Tabelle basiert, können z. B. keine Transaktionen verwendet werden.

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


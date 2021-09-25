---
title: Recordset2.Restartable-Eigenschaft (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a5a050b735a22f99bd53d78fe1d679e39bef3ca3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562335"
---
# <a name="recordset2restartable-property-dao"></a>Recordset2.Restartable-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob ein **[Recordset](recordset-object-dao.md)** -Objekt die **[Requery](recordset2-requery-method-dao.md)** -Methode unterstützt, die die Abfrage, auf der das **Recordset**-Objekt basiert, erneut ausführt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Neustartbar

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Table-type **Recordset** objects always return **False**.

Überprüfen Sie die **Restartable**-Eigenschaft vor der Verwendung der **Requery**-Methode für ein **Recordset**-Objekt. Wenn die **Restartable**-Eigenschaft des Objekts den Wert **False** hat, verwenden Sie die **[OpenRecordset](connection-openrecordset-method-dao.md)** -Methode für das zugrunde liegende **[QueryDef](querydef-object-dao.md)** -Objekt, um die Abfrage erneut auszuführen.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht die **Restartable**-Eigenschaft für verschiedene **Recordset**-Objekte.

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

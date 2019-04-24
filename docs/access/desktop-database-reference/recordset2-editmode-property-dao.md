---
title: Recordset2. EditMode-Eigenschaft (DAO)
TOCTitle: EditMode Property
ms:assetid: fd61ea2b-e7d7-195f-4114-87e54eba2451
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837240(v=office.15)
ms:contentKeyID: 48548914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053080
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d4043a442bec8c5ce421d85de6256eb9c5cb353f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307350"
---
# <a name="recordset2editmode-property-dao"></a>Recordset2. EditMode-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der den Bearbeitungsstatus für den aktuellen Datensatz angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . EditMode

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist ein **Long**-Datentyp, der den Bearbeitungsstatus angibt. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.

Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wurde, wie z. B. bei einem Fehler bei der Gültigkeitsprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft feststellen, ob die **[Update](recordset2-update-method-dao.md)** - oder die **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** -Methode verwendet werden soll.

Sie können auch überprüfen, ob der Wert der **[LockEdits](recordset2-lockedits-property-dao.md)** -Einstellung **True** und der Wert der **EditMode**-Einstellung **dbEditInProgress** ist, um festzustellen, ob die aktuelle Seite gesperrt ist.

## <a name="example"></a>Beispiel

This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Show the EditMode property under different editing 
     ' states. 
     With rstEmployees 
     EditModeOutput "Before any Edit or AddNew:", .EditMode 
     .Edit 
     EditModeOutput "After Edit:", .EditMode 
     .Update 
     EditModeOutput "After Update:", .EditMode 
     .AddNew 
     EditModeOutput "After AddNew:", .EditMode 
     .CancelUpdate 
     EditModeOutput "After CancelUpdate:", .EditMode 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function EditModeOutput(strTemp As String, _ 
     intEditMode As Integer) 
     
     ' Print report based on the value of the EditMode 
     ' property. 
     Debug.Print strTemp 
     Debug.Print " EditMode = "; 
     
     Select Case intEditMode 
     Case dbEditNone 
     Debug.Print "dbEditNone" 
     Case dbEditInProgress 
     Debug.Print "dbEditInProgress" 
     Case dbEditAdd 
     Debug.Print "dbEditAdd" 
     End Select 
     
    End Function
```

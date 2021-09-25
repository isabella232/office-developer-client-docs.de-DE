---
title: Recordset.EditMode-Eigenschaft (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 086c909e292f58f6403a62bc1b2c307219806788
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606289"
---
# <a name="recordseteditmode-property-dao"></a>Recordset.EditMode-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der den Bearbeitungsstatus für den aktuellen Datensatz angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Editmode

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist ein **Long**-Datentyp, der den Bearbeitungsstatus angibt. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.

Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wurde, wie z. B. bei einem Fehler bei der Gültigkeitsprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft feststellen, ob die **[Update](recordset-update-method-dao.md)** - oder die **[CancelUpdate](recordset-cancelupdate-method-dao.md)** -Methode verwendet werden soll.

Sie können auch überprüfen, ob der Wert der **[LockEdits](recordset-lockedits-property-dao.md)** -Einstellung **True** und der Wert der **EditMode**-Einstellung **dbEditInProgress** ist, um festzustellen, ob die aktuelle Seite gesperrt ist.

## <a name="example"></a>Beispiel

This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.

```vb
    Sub EditModeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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

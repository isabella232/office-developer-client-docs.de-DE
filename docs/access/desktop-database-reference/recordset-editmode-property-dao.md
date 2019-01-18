---
title: Recordset.EditMode-Eigenschaft (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718644"
---
# <a name="recordseteditmode-property-dao"></a>Recordset.EditMode-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt einen Wert zurück, der den Status der Bearbeitung für den aktuellen Datensatz angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . EditMode

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist vom Datentyp **Long** und gibt den Status der Bearbeitung an. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.

Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wird, z. B. durch einen Fehler während der Überprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft ermitteln, ob Sie die Methode **[Update](recordset-update-method-dao.md)** oder **[CancelUpdate](recordset-cancelupdate-method-dao.md)** verwenden sollten.

Sie können auch überprüfen, ob die Einstellung der **[LockEdits](recordset-lockedits-property-dao.md)** -Eigenschaft auf **True** und die Einstellung der **EditMode**-Eigenschaft auf **dbEditInProgress** festgelegt ist, um festzustellen, ob die aktuelle Seite gesperrt ist.

## <a name="example"></a>Beispiel

In diesem Beispiel wird der Wert der EditMode-Eigenschaft unter verschiedenen Bedingungen veranschaulicht. Zum Ausführen dieser Prozedur ist die EditModeOutput-Funktion erforderlich.

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

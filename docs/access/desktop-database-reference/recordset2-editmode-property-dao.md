---
title: Recordset2.EditMode Property (DAO)
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
ms.openlocfilehash: 7b8ff4fa104dd153faf6eb1a50d2e922e5e5021d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472857"
---
# <a name="recordset2editmode-property-dao"></a>Recordset2.EditMode Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt einen Wert zurück, der den Status der Bearbeitung für den aktuellen Datensatz angibt.

## <a name="syntax"></a>Syntax

*Ausdruck* . EditMode

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist vom Datentyp **Long** und gibt den Status der Bearbeitung an. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.

Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wird, z. B. durch einen Fehler während der Überprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft ermitteln, ob Sie die Methode **[Update](recordset2-update-method-dao.md)** oder **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** verwenden sollten.

Sie können auch überprüfen, ob die Einstellung der **[LockEdits](recordset2-lockedits-property-dao.md)** -Eigenschaft auf **True** und die Einstellung der **EditMode**-Eigenschaft auf **dbEditInProgress** festgelegt ist, um festzustellen, ob die aktuelle Seite gesperrt ist.

## <a name="example"></a>Beispiel

In diesem Beispiel wird der Wert der EditMode-Eigenschaft unter verschiedenen Bedingungen veranschaulicht. Zum Ausführen dieser Prozedur ist die EditModeOutput-Funktion erforderlich.

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

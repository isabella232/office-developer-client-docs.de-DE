---
title: Recordset. EditMode-Eigenschaft (DAO)
TOCTitle: EditMode Property
ms:assetid: 3cf67f64-c8c3-ad0a-ce00-6f37a3c264ee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192697(v=office.15)
ms:contentKeyID: 48544329
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 326f23f95f9ccf8763f76b21df8955c39198a88c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307651"
---
# <a name="recordseteditmode-property-dao"></a><span data-ttu-id="2e03e-102">Recordset. EditMode-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="2e03e-102">Recordset.EditMode property (DAO)</span></span>


<span data-ttu-id="2e03e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e03e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e03e-104">Gibt einen Wert zurück, der den Bearbeitungsstatus für den aktuellen Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="2e03e-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e03e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e03e-105">Syntax</span></span>

<span data-ttu-id="2e03e-106">*Ausdruck* . EditMode</span><span class="sxs-lookup"><span data-stu-id="2e03e-106">*expression* .EditMode</span></span>

<span data-ttu-id="2e03e-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e03e-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e03e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e03e-108">Remarks</span></span>

<span data-ttu-id="2e03e-p101">Der Rückgabewert ist ein **Long**-Datentyp, der den Bearbeitungsstatus angibt. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="2e03e-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="2e03e-p102">Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wurde, wie z. B. bei einem Fehler bei der Gültigkeitsprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft feststellen, ob die **[Update](recordset-update-method-dao.md)** - oder die **[CancelUpdate](recordset-cancelupdate-method-dao.md)** -Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e03e-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset-update-method-dao.md)** or **[CancelUpdate](recordset-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="2e03e-113">Sie können auch überprüfen, ob der Wert der **[LockEdits](recordset-lockedits-property-dao.md)** -Einstellung **True** und der Wert der **EditMode**-Einstellung **dbEditInProgress** ist, um festzustellen, ob die aktuelle Seite gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="2e03e-113">You can also check to see if the **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="2e03e-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e03e-114">Example</span></span>

<span data-ttu-id="2e03e-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="2e03e-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

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

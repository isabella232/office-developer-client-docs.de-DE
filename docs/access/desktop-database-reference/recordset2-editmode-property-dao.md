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
# <a name="recordset2editmode-property-dao"></a><span data-ttu-id="ceecb-102">Recordset2. EditMode-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="ceecb-102">Recordset2.EditMode property (DAO)</span></span>


<span data-ttu-id="ceecb-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ceecb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ceecb-104">Gibt einen Wert zurück, der den Bearbeitungsstatus für den aktuellen Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="ceecb-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceecb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceecb-105">Syntax</span></span>

<span data-ttu-id="ceecb-106">*Ausdruck* . EditMode</span><span class="sxs-lookup"><span data-stu-id="ceecb-106">*expression* .EditMode</span></span>

<span data-ttu-id="ceecb-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ceecb-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceecb-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ceecb-108">Remarks</span></span>

<span data-ttu-id="ceecb-p101">Der Rückgabewert ist ein **Long**-Datentyp, der den Bearbeitungsstatus angibt. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="ceecb-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="ceecb-p102">Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wurde, wie z. B. bei einem Fehler bei der Gültigkeitsprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft feststellen, ob die **[Update](recordset2-update-method-dao.md)** - oder die **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** -Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ceecb-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset2-update-method-dao.md)** or **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="ceecb-113">Sie können auch überprüfen, ob der Wert der **[LockEdits](recordset2-lockedits-property-dao.md)** -Einstellung **True** und der Wert der **EditMode**-Einstellung **dbEditInProgress** ist, um festzustellen, ob die aktuelle Seite gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="ceecb-113">You can also check to see if the **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="ceecb-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ceecb-114">Example</span></span>

<span data-ttu-id="ceecb-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="ceecb-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

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

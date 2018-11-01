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
ms.openlocfilehash: e6169169b5152e47063e2f679f2494c87581eb02
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889350"
---
# <a name="recordset2editmode-property-dao"></a><span data-ttu-id="fb87f-102">Recordset2.EditMode Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb87f-102">Recordset2.EditMode Property (DAO)</span></span>


<span data-ttu-id="fb87f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb87f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb87f-104">Gibt einen Wert zurück, der den Status der Bearbeitung für den aktuellen Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="fb87f-104">Returns a value that indicates the state of editing for the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb87f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb87f-105">Syntax</span></span>

<span data-ttu-id="fb87f-106">*Ausdruck* . EditMode</span><span class="sxs-lookup"><span data-stu-id="fb87f-106">*expression* .EditMode</span></span>

<span data-ttu-id="fb87f-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb87f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb87f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb87f-108">Remarks</span></span>

<span data-ttu-id="fb87f-p101">Der Rückgabewert ist vom Datentyp **Long** und gibt den Status der Bearbeitung an. Der Wert kann eine der **[EditModeEnum](editmodeenum-enumeration-dao.md)** -Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="fb87f-p101">The return value is a **Long** that indicates the state of editing. The value can be one of the **[EditModeEnum](editmodeenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="fb87f-p102">Die **EditMode**-Eigenschaft ist nützlich, wenn ein Bearbeitungsvorgang unterbrochen wird, z. B. durch einen Fehler während der Überprüfung. Sie können mit dem Wert der **EditMode**-Eigenschaft ermitteln, ob Sie die Methode **[Update](recordset2-update-method-dao.md)** oder **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="fb87f-p102">The **EditMode** property is useful when an editing process is interrupted, for example, by an error during validation. You can use the value of the **EditMode** property to determine whether you should use the **[Update](recordset2-update-method-dao.md)** or **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** method.</span></span>

<span data-ttu-id="fb87f-113">Sie können auch überprüfen, ob die Einstellung der **[LockEdits](recordset2-lockedits-property-dao.md)** -Eigenschaft auf **True** und die Einstellung der **EditMode**-Eigenschaft auf **dbEditInProgress** festgelegt ist, um festzustellen, ob die aktuelle Seite gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="fb87f-113">You can also check to see if the **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** and the **EditMode** property setting is **dbEditInProgress** to determine whether the current page is locked.</span></span>

## <a name="example"></a><span data-ttu-id="fb87f-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fb87f-114">Example</span></span>

<span data-ttu-id="fb87f-p103">In diesem Beispiel wird der Wert der EditMode-Eigenschaft unter verschiedenen Bedingungen veranschaulicht. Zum Ausführen dieser Prozedur ist die EditModeOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb87f-p103">This example shows the value of the **EditMode** property under various conditions. The EditModeOutput function is required for this procedure to run.</span></span>

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

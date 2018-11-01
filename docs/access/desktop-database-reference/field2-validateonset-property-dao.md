---
title: Field2.ValidateOnSet Property (DAO)
TOCTitle: ValidateOnSet Property
ms:assetid: 07612730-8dad-4ef0-b19b-f76845973fc3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844969(v=office.15)
ms:contentKeyID: 48543075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5637abc3fc956bd6e562b4200257da8f787a5dab
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890967"
---
# <a name="field2validateonset-property-dao"></a><span data-ttu-id="bac86-102">Field2.ValidateOnSet Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="bac86-102">Field2.ValidateOnSet Property (DAO)</span></span>


<span data-ttu-id="bac86-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bac86-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bac86-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob der Wert eines **Field2**-Objekts sofort beim Festlegen der **Value**-Eigenschaft überprüft wird (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="bac86-104">Sets or returns a value that specifies whether or not the value of a **Field2** object is immediately validated when the object's **Value** property is set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="bac86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bac86-105">Syntax</span></span>

<span data-ttu-id="bac86-106">*Ausdruck* . ValidateOnSet</span><span class="sxs-lookup"><span data-stu-id="bac86-106">*expression* .ValidateOnSet</span></span>

<span data-ttu-id="bac86-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bac86-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac86-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bac86-108">Remarks</span></span>

<span data-ttu-id="bac86-109">Nur **Field2**-Objekte in **Recordset**-Objekten unterstützen den Lese-/Schreibzugriff der **ValidateOnSet**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bac86-109">Only **Field2** objects in **Recordset** objects support the **ValidateOnSet** property as read/write.</span></span>

<span data-ttu-id="bac86-p101">In Situationen, in denen ein Benutzer Datensätze eingibt, die umfangreiche Daten vom Typ Memo einschließen, kann es nützlich sein, die ValidateOnSet-Eigenschaft auf True festzulegen. Falls gewartet wird, bis die Daten mit dem Update-Aufruf überprüft werden, geht gegebenenfalls unnötig viel Zeit mit der Eingabe langer Memodaten in die Datenbank verloren. Letztendlich stellt sich möglicherweise heraus, dass die Daten aufgrund eines Verstoßes gegen eine Gültigkeitsregel in einem anderen Feld ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="bac86-p101">Setting the **ValidateOnSet** property to **True** can be useful in a situation when a user is entering records that include substantial Memo data. Waiting until the **Update** call to validate the data can result in unnecessary time spent writing the lengthy Memo data to the database if it turns out that the data was invalid anyway because a validation rule was broken in another field.</span></span>

## <a name="example"></a><span data-ttu-id="bac86-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bac86-112">Example</span></span>

<span data-ttu-id="bac86-p102">Diese Beispiel veranschaulicht mit der ValidateOnSet-Eigenschaft, wie Fehler bei der Dateneingabe abgefangen werden können. Zum Ausführen dieser Prozedur ist die ValidateData-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bac86-p102">This example uses the **ValidateOnSet** property to demonstrate how one might trap for errors during data entry. The ValidateData function is required for this procedure to run.</span></span>

```vb
    Sub ValidateOnSetX() 
     
     Dim dbsNorthwind As Database 
     Dim fldDays As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new Field object to the Fields 
     ' collection of the Employees table. 
     Set fldDays = _ 
     dbsNorthwind.TableDefs!Employees.CreateField( _ 
     "DaysOfVacation", dbInteger, 2) 
     fldDays.ValidationRule = "BETWEEN 1 AND 20" 
     fldDays.ValidationText = _ 
     "Number must be between 1 and 20!" 
     dbsNorthwind.TableDefs!Employees.Fields.Append fldDays 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     
     Do While True 
     ' Add new record. 
     .AddNew 
     
     ' Get user input for three fields. Verify that the 
     ' data do not violate the validation rules for any 
     ' of the fields. 
     If ValidateData(!FirstName, _ 
     "Enter first name.") = False Then Exit Do 
     If ValidateData(!LastName, _ 
     "Enter last name.") = False Then Exit Do 
     If ValidateData(!DaysOfVacation, _ 
     "Enter days of vacation.") = False Then Exit Do 
     
     .Update 
     .Bookmark = .LastModified 
     Debug.Print !FirstName & " " & !LastName & _ 
     " - " & "DaysOfVacation = " & !DaysOfVacation 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     Exit Do 
     Loop 
     
     ' Cancel AddNew method if any of the validation rules 
     ' were broken. 
     If .EditMode <> dbEditNone Then .CancelUpdate 
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     dbsNorthwind.TableDefs!Employees.Fields.Delete _ 
     fldDays.Name 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function ValidateData(fldTemp As Field2, _ 
     strMessage As String) As Boolean 
     
     Dim strInput As String 
     Dim errLoop As Error 
     
     ValidateData = True 
     ' ValidateOnSet is only read/write for Field objects in 
     ' Recordset objects. 
     fldTemp.ValidateOnSet = True 
     
     Do While True 
     strInput = InputBox(strMessage) 
     If strInput = "" Then Exit Do 
     ' Trap for errors when setting the Field value. 
     On Error GoTo Err_Data 
     If fldTemp.Type = dbInteger Then 
     fldTemp = Val(strInput) 
     Else 
     fldTemp = strInput 
     End If 
     On Error GoTo 0 
     If Not IsNull(fldTemp) Then Exit Do 
     Loop 
     
     If strInput = "" Then ValidateData = False 
     
     Exit Function 
     
    Err_Data: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. The description 
     ' property of the last Error object will be set to 
     ' the ValidationText property of the relevant 
     ' field. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Function
```

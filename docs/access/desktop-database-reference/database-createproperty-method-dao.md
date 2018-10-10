---
title: Database.CreateProperty Method (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f7e405410f19178a7f4845cf95fcb6e980adeb9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472682"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="c4273-102">Database.CreateProperty Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="c4273-102">Database.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="c4273-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4273-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4273-p101">Erstellt ein neues, benutzerdefiniertes **[Property](property-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="c4273-p101">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="c4273-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4273-106">Syntax</span></span>

<span data-ttu-id="c4273-107">*Ausdruck* . CreateProperty (***Name***, ***Typ***, ***Wert***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="c4273-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="c4273-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c4273-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c4273-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4273-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4273-110">Name</span><span class="sxs-lookup"><span data-stu-id="c4273-110">Name</span></span></p></th>
<th><p><span data-ttu-id="c4273-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="c4273-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c4273-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c4273-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c4273-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4273-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4273-114">Name</span><span class="sxs-lookup"><span data-stu-id="c4273-114">Name</span></span></p></td>
<td><p><span data-ttu-id="c4273-115">Optional</span><span class="sxs-lookup"><span data-stu-id="c4273-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4273-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4273-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4273-p102">Ein <strong>String</strong>-Wert, der das neue <strong>Property</strong>-Objekt eindeutig benennt. Weitere Informationen zu gültigen <strong>Property</strong>-Namen finden Sie in dem Thema zur <strong>Name</strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4273-p102">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4273-119">Typ</span><span class="sxs-lookup"><span data-stu-id="c4273-119">Type</span></span></p></td>
<td><p><span data-ttu-id="c4273-120">Optional</span><span class="sxs-lookup"><span data-stu-id="c4273-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4273-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4273-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4273-p103">Eine Konstante, die den Datentyp des neuen <strong>Property</strong>-Objekts definiert. Informationen zu gültigen Datentypen finden Sie in dem Thema zur <strong><a href="field-type-property-dao.md">Type</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4273-p103">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4273-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c4273-124">Value</span></span></p></td>
<td><p><span data-ttu-id="c4273-125">Optional</span><span class="sxs-lookup"><span data-stu-id="c4273-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4273-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4273-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4273-p104">Ein <strong>Variant</strong>-Wert, der den ursprünglichen Eigenschaftswert enthält. Weitere Informationen finden Sie in dem Thema zur <strong><a href="field-value-property-dao.md">Value</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4273-p104">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4273-129">DDL</span><span class="sxs-lookup"><span data-stu-id="c4273-129">DDL</span></span></p></td>
<td><p><span data-ttu-id="c4273-130">Optional</span><span class="sxs-lookup"><span data-stu-id="c4273-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4273-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4273-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4273-132"><strong>Variant</strong> (Untertyp<strong>Boolean</strong> ), der angibt, ob die <strong>Eigenschaft</strong> ein DDL-Objekt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c4273-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="c4273-133">Der Standardwert ist False.</span><span class="sxs-lookup"><span data-stu-id="c4273-133">The default is False.</span></span> <span data-ttu-id="c4273-134">Wenn DDL auf true festgelegt ist, können nicht Benutzer ändern oder diese <strong>Property-</strong> Objekt löschen, es sei denn, sie über DbSecWriteDef berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="c4273-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c4273-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4273-135">Return Value</span></span>

<span data-ttu-id="c4273-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4273-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="c4273-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4273-137">Remarks</span></span>

<span data-ttu-id="c4273-138">Ein benutzerdefiniertes **Property**-Objekt können Sie nur in der **[Properties](properties-collection-dao.md)** -Auflistung eines beständigen Objekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4273-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="c4273-p106">Wenn Sie **CreateProperty** verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zur **Name**-, **Type**- und **Value**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c4273-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="c4273-142">Wenn Name auf ein Objekt, das bereits ein Element der Auflistung ist bezieht, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4273-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="c4273-p107">Verwenden Sie die [**Delete**](fields-delete-method-dao.md) -Methode für die \*\*\*\*Properties\*\*\*\* -Auflistung, um ein benutzerdefiniertes Property-Objekt aus der Auflistung zu entfernen. Sie können keine integrierten Eigenschaften löschen.</span><span class="sxs-lookup"><span data-stu-id="c4273-p107">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="c4273-145">Wenn Sie das Argument DDL weglassen, wird standardmäßig auf False (nicht-DDL).</span><span class="sxs-lookup"><span data-stu-id="c4273-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="c4273-146">Da keine entsprechende DDL-Eigenschaft verfügbar gemacht wurde, müssen Sie ein **Property**-Objekt, das von DLL in Nicht-DLL geändert werden soll, löschen und erneut erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4273-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="c4273-147">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4273-147">Example</span></span>

<span data-ttu-id="c4273-p109">In diesem Beispiel wird versucht, den Wert einer benutzerdefinierten Eigenschaft festzulegen. Wenn die Eigenschaft nicht vorhanden ist, wird die CreateProperty-Methode zum Erstellen und Festlegen des Werts der neuen Eigenschaft verwendet. Zum Ausführen dieses Vorgangs ist die SetProperty-Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4273-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Set the Archive property to True. 
       SetProperty dbsNorthwind, "Archive", True 
        
       With dbsNorthwind 
          Debug.Print "Properties of " & .Name 
           
          ' Enumerate Properties collection of the Northwind  
          ' database. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
     
          ' Delete the new property since this is a  
          ' demonstration. 
          .Properties.Delete "Archive" 
     
          .Close 
       End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
       booTemp As Boolean) 
     
       Dim prpNew As Property 
       Dim errLoop As Error 
     
       ' Attempt to set the specified property. 
       On Error GoTo Err_Property 
       dbsTemp.Properties("strName") = booTemp 
       On Error GoTo 0 
     
       Exit Sub 
     
    Err_Property: 
     
       ' Error 3270 means that the property was not found. 
       If DBEngine.Errors(0).Number = 3270 Then 
          ' Create property, set its value, and append it to the  
          ' Properties collection. 
          Set prpNew = dbsTemp.CreateProperty(strName, _ 
             dbBoolean, booTemp) 
          dbsTemp.Properties.Append prpNew 
          Resume Next 
       Else 
          ' If different error has occurred, display message. 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
          End 
       End If 
     
    End Sub
```

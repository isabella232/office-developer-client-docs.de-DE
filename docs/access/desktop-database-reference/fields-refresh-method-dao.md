---
title: Fields.Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e118705052c23613500191437906be5507099ef
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921810"
---
# <a name="fieldsrefresh-method-dao"></a><span data-ttu-id="c69ed-102">Fields.Refresh-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c69ed-102">Fields.Refresh method (DAO)</span></span>


<span data-ttu-id="c69ed-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c69ed-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c69ed-104">Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="c69ed-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c69ed-105">Syntax</span></span>

<span data-ttu-id="c69ed-106">*Ausdruck* . Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c69ed-106">*expression* .Refresh</span></span>

<span data-ttu-id="c69ed-107">*Ausdruck* Eine Variable, die ein **Fields** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c69ed-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c69ed-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c69ed-108">Remarks</span></span>

<span data-ttu-id="c69ed-p101">Verwenden Sie die **OrdinalPosition**-Eigenschaft der einzelnen **Field**-Objekte, um die Position zu bestimmen, die das Microsoft Access-Datenbankmodul für **Field**-Objekte in der **Fields**-Auflistung eines **QueryDef**-, **Recordset**- oder **TableDef**-Objekts verwendet. Eine Änderung der **OrdinalPosition**-Eigenschaft eines **Field**-Objekts führt möglicherweise erst beim Anwenden der **Refresh**-Methode zu einer geänderten Reihenfolge der **Field**-Objekte.</span><span class="sxs-lookup"><span data-stu-id="c69ed-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="c69ed-p102">Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c69ed-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="c69ed-p103">Eine Sammlung ist mit Objekten gefüllt, wenn das erste Mal darauf verwiesen wird. Nachfolgende Änderungen durch andere Benutzer werden nicht automatisch angezeigt. Wenn es wahrscheinlich ist, dass ein anderer Benutzer eine Auflistung geändert hat, wenden Sie sofort die Refresh-Methode auf die Auflistung an, bevor Sie eine Aufgabe in der Anwendung ausführen, die voraussetzt, dass ein bestimmtes Objekt in der Auflistung vorhanden ist bzw. fehlt. So ist sichergestellt, dass die Auflistung möglichst aktuell ist. Andererseits kann die Refresh-Methode die Leistung unnötigerweise beeinträchtigen.
</span><span class="sxs-lookup"><span data-stu-id="c69ed-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

## <a name="example"></a><span data-ttu-id="c69ed-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c69ed-118">Example</span></span>

<span data-ttu-id="c69ed-p104">In diesem Beispiel wird mithilfe der Refresh-Methode die Fields-Auflistung der Categories-Tabelle anhand der Änderungen an den OrdinalPosition-Daten aktualisiert. Die Reihenfolge der Fields-Objekte in der Auflistung ändert sich erst, wenn die Refresh-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c69ed-p104">This example uses the **Refresh** method to update the **Fields** collection of the Categories table based on changes to the **OrdinalPosition** data. The order of the **Fields** in the collection changes only after the **Refresh** method is used.</span></span>

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```

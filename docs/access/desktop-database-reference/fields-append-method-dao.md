---
title: Fields.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 576928e6538ea704bf6f10d0826c0e6bbb359bf1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998238"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="2cea5-102">Fields.Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="2cea5-102">Fields.Append method (DAO)</span></span>

<span data-ttu-id="2cea5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cea5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2cea5-104">Fügt der **[Fields](field-object-dao.md)** -Auflistung ein neues **[Field](fields-collection-dao.md)** -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="2cea5-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cea5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cea5-105">Syntax</span></span>

<span data-ttu-id="2cea5-106">*Ausdruck* . Fügen Sie (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="2cea5-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="2cea5-107">*Ausdruck* Eine Variable, die ein **Fields** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2cea5-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cea5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cea5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cea5-109">Name</span><span class="sxs-lookup"><span data-stu-id="2cea5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2cea5-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="2cea5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2cea5-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2cea5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2cea5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cea5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cea5-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="2cea5-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="2cea5-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2cea5-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2cea5-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="2cea5-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="2cea5-116">Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2cea5-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2cea5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cea5-117">Remarks</span></span>

<span data-ttu-id="2cea5-118">Mithilfe der **Append**-Methode können Sie einer Datenbank eine neue Tabelle, einer Tabelle ein Feld und einem Index ein Feld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2cea5-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="2cea5-119">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="2cea5-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="2cea5-120">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="2cea5-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="2cea5-121">Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="2cea5-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="2cea5-122">Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="2cea5-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="2cea5-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2cea5-123">Example</span></span>

<span data-ttu-id="2cea5-p102">In diesem Beispiel wird entweder die **Append** -Methode oder die **Delete** -Methode zum Ändern der **Fields** -Auflistung eines **TableDef** -Objekts verwendet. Zum Ausführen dieser Prozedur ist die AppendDeleteField-Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2cea5-p102">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```

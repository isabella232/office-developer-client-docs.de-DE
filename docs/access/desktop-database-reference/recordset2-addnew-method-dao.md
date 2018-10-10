---
title: Recordset2.AddNew Method (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e8123fc67d8b41b892f92b19605a26384af68b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474185"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="26ae1-102">Recordset2.AddNew Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="26ae1-102">Recordset2.AddNew Method (DAO)</span></span>


<span data-ttu-id="26ae1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="26ae1-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="26ae1-104">Erstellt einen neuen Datensatz für ein aktualisierbares **Recordset2**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="26ae1-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ae1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26ae1-105">Syntax</span></span>

<span data-ttu-id="26ae1-106">*Ausdruck* . AddNew</span><span class="sxs-lookup"><span data-stu-id="26ae1-106">*expression* .AddNew</span></span>

<span data-ttu-id="26ae1-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="26ae1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26ae1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26ae1-108">Remarks</span></span>

<span data-ttu-id="26ae1-p101">Verwenden Sie die AddNew-Methode, um einen neuen Datensatz zu erstellen und zum durch Recordset benannten Recordset2-Objekt hinzuzufügen. Bei dieser Methode werden die Felder auf Standardwerte festgelegt. Sind keine Standardwerte angegeben, werden die Felder auf Null festgelegt (die für ein Recordset2 des Typs Tabelle angegebenen Standardwerte).</span><span class="sxs-lookup"><span data-stu-id="26ae1-p101">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="26ae1-p102">Mit der **[Update](recordset2-update-method-dao.md)** -Methode können Sie nach dem Ändern des neuen Datensatzes die Änderungen speichern und den Datensatz zum **Recordset2** hinzufügen. Es treten erst dann Änderungen in der Datenbank auf, wenn Sie die **Update**-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p102">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**. No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="26ae1-p103">[!HINWEIS] Wenn Sie eine <STRONG>AddNew</STRONG>-Methode aufrufen und dann durch einen beliebigen Vorgang zu einem anderen Datensatz wechseln, ohne <STRONG>Update</STRONG> zu verwenden, gehen Ihre Änderungen ohne Warnung verloren. Wenn Sie außerdem das <STRONG>Recordset2</STRONG> schließen oder die Prozedur beenden, die das <STRONG>Recordset2</STRONG> oder dessen <STRONG><A href="database-object-dao.md">Database</A></STRONG> -Objekt deklariert, wird der neue Datensatz ohne Warnung verworfen.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p103">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning. In addition, if you close the <STRONG>Recordset2</STRONG> or end the procedure that declares the <STRONG>Recordset2</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="26ae1-p104">[!HINWEIS] Wenn Sie <STRONG>AddNew</STRONG> in einem Microsoft Access-Arbeitsbereich verwenden und das Datenbankmodul eine neue Seite für den aktuellen Datensatz erstellen muss, ist die Seitensperre pessimistisch. Passt der neue Datensatz hingegen auf eine vorhandene Seite, ist die Seitensperre optimistisch.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p104">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="26ae1-p105">Wenn Sie noch nicht zum letzten Datensatz des **Recordset2**-Objekts gewechselt sind, werden Datensätze, die durch andere Prozesse zu Basistabellen hinzugefügt wurden, möglicherweise einbezogen, wenn sie hinter dem aktuellen Datensatz liegen. Wenn Sie einen Datensatz zu Ihrem eigenen **Recordset2** hinzufügen, ist er im **Recordset2** sichtbar und wird in die zugrunde liegende Tabelle einbezogen, in der er für neue **Recordset2**-Objekte sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p105">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="26ae1-119">Die Position des neuen Datensatzes hängt vom Typ des **Recordset2**-Objekts ab:</span><span class="sxs-lookup"><span data-stu-id="26ae1-119">The position of the new record depends on the type of **Recordset2**:</span></span>

  - <span data-ttu-id="26ae1-120">In einem Recordset2-Objekt vom Typ Dynaset werden Datensätze an das Ende des Recordset-Objekts eingefügt, unabhängig davon, welche Regeln in Bezug auf die Sortierung oder Reihenfolge beim Öffnen des Recordset-Objekts gültig waren.</span><span class="sxs-lookup"><span data-stu-id="26ae1-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="26ae1-p106">In einem Recordset2-Objekt vom Typ Tabelle, dessen Index-Eigenschaft festgelegt wurde, werden Datensätze in der Sortierreihenfolge an ihrer richtigen Position zurückgegeben. Falls Sie die Index-Eigenschaft nicht festgelegt haben, werden neue Datensätze am Ende des Recordset-Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p106">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="26ae1-p107">Der Datensatz, der vor dem Verwenden von **AddNew** aktuell war, bleibt der aktuelle Datensatz. Wenn Sie den neuen Datensatz zum aktuellen Datensatz machen möchten, können Sie die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft auf das durch die **[LastModified](recordset2-lastmodified-property-dao.md)** -Eigenschaft identifizierte Lesezeichen festlegen.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="26ae1-p108">[!HINWEIS] Um einen Datensatz hinzuzufügen, zu bearbeiten oder zu löschen, muss es einen eindeutigen Index im Datensatz in der zugrunde liegenden Datenquelle geben. Andernfalls tritt ein "Berechtigung verweigert"-Fehler im <STRONG>AddNew</STRONG> -, <STRONG>Delete</STRONG> - oder <STRONG>Edit</STRONG> -Methodenaufruf in einem Microsoft Access-Arbeitsbereich auf.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="26ae1-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="26ae1-127">Example</span></span>

<span data-ttu-id="26ae1-p109">Dieses Beispiel verwendet die **AddNew** -Methode, um einen neuen Datensatz mit dem angegebenen Namen zu erstellen. Die "AddName"-Funktion ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26ae1-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```

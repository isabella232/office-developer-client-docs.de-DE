---
title: Recordset.AddNew-Methode (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 79c8691fcea7cf04bac7d6cd05711730b510e215
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300644"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="c209f-102">Recordset.AddNew-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c209f-102">Recordset.AddNew Method (DAO)</span></span>

<span data-ttu-id="c209f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c209f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c209f-104">Erstellt einen neuen Datensatz für ein aktualisierbares **[Recordset](recordset-object-dao.md)**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c209f-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c209f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c209f-105">Syntax</span></span>

<span data-ttu-id="c209f-106">*expression* .AddNew</span><span class="sxs-lookup"><span data-stu-id="c209f-106">expression  . AddNew</span></span>

<span data-ttu-id="c209f-107">*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c209f-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c209f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c209f-108">Remarks</span></span>

<span data-ttu-id="c209f-p101">Verwenden Sie die **AddNew**-Methode, um einen neuen Datensatz im **Recordset**-Objekt, das nach dem Recordset benannt ist, zu erstellen und hinzuzufügen. Diese Methode legt die Felder auf Standardwerte fest. Wenn keine Standardwerte angegeben sind, werden die Felder auf "Null" festgelegt (die Standardwerte, die für einen Tabellentyp **Recordset** angegeben sind).</span><span class="sxs-lookup"><span data-stu-id="c209f-p101">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset. This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="c209f-p102">Verwenden Sie nach dem Ändern des neuen Datensatzes die **[Update](recordset-update-method-dao.md)** -Methode, um die Änderungen zu speichern und den Datensatz zum **Recordset** hinzuzufügen. In der Datenbank treten Änderungen erst dann auf, wenn Sie die **Update** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="c209f-p102">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**. No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="c209f-p103">Wenn Sie **AddNew** ausgeben und dann einen Vorgang ausführen, der ohne Verwenden von **Update** zu einem anderen Datensatz springt, gehen Ihre Änderungen ohne Warnung verloren, Wenn Sie das **Recordset** schließen oder das Verfahren beenden, das das **Recordset** oder sein **[Datenbankobjekt](database-object-dao.md)** deklariert, wird der neue Datensatz ohne Warnung verworfen.</span><span class="sxs-lookup"><span data-stu-id="c209f-p103">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning. In addition, if you close the **Recordset** or end the procedure that declares the **Recordset** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="c209f-p104">Wenn Sie **AddNew** in einem Microsoft Access-Arbeitsbereich verwenden und das Datenbankmodul eine neue Seite für den aktuellen Datensatz erstellen muss, ist Seitensperrung pessimistisch. Wenn der neue Datensatz auf eine vorhandene Seite passt, ist Seitensperrung optimistisch.</span><span class="sxs-lookup"><span data-stu-id="c209f-p104">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic. If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="c209f-p105">Wenn Sie noch nicht zum letzten Datensatz Ihres **Recordsets** gesprungen sind, sind Datensätze, die von anderen Prozessen Basistabellen hinzugefügt werden, möglicherweise enthalten, wenn sie nach dem aktuellen Datensatz positioniert sind. Wenn Sie Ihrem eigenen **Recordset** einen Datensatz hinzufügen, wird der Datensatz allerdings im **Recordset** angezeigt und in die zugrunde liegende Tabelle eingeschlossen, wo er für alle neuen **Recordset** -Objekte sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="c209f-p105">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record. If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="c209f-119">Die Position des neuen Datensatzes hängt vom **Recordset** -Typ ab:</span><span class="sxs-lookup"><span data-stu-id="c209f-119">The position of the new record depends on the type of **Recordset**:</span></span>

- <span data-ttu-id="c209f-120">In einem **Recordset** -Objekt vom dynaset-Typ werden Datensätze am Ende des **Recordsets** eingefügt, unabhängig von Sortier- oder Reihenfolgeregeln, die beim Öffnen des **Recordsets** wirksam waren.</span><span class="sxs-lookup"><span data-stu-id="c209f-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="c209f-p106">In einem Tabellentyp- **Recordset** -Objekt, für das die **[Index](recordset-index-property-dao.md)** -Eigenschaft festgelegt wurde, werden Datensätze am entsprechenden Platz in der Sortierreihenfolge zurückgegeben. Falls Sie die **Index** -Eigenschaft nicht festgelegt haben, werden neue Datensätze am Ende des **Recordsets** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c209f-p106">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order. If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="c209f-p107">Der Datensatz, der aktuell war, bevor Sie **AddNew** verwendet haben, bleibt aktuell. Wenn Sie den neuen Datensatz aktuell machen möchten, können Sie die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft auf das Bookmark festlegen, das von der **[LastModified](recordset-lastmodified-property-dao.md)** -Eigenschaftseinstellung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c209f-p107">The record that was current before you used **AddNew** remains current. If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="c209f-p108">Es muss ein eindeutiger Index für den Datensatz in der zugrunde liegenden Datenquelle vorhanden sein, damit der Datensatz hinzugefügt, bearbeitet oder gelöscht werden kann. Andernfalls tritt im Aufruf der Methoden **AddNew**, **Delete** oder **Edit** in einem Microsoft Access-Arbeitsbereich ein Fehler vom Typ "Berechtigung verweigert" auf.</span><span class="sxs-lookup"><span data-stu-id="c209f-p108">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="c209f-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c209f-127">Example</span></span>

<span data-ttu-id="c209f-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="c209f-p109">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
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

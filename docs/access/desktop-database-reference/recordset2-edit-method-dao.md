---
title: Recordset2. Edit-Methode (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2742b6558c555673937666ea7d27cae1a54fdf73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309436"
---
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="3343f-102">Recordset2. Edit-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="3343f-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="3343f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3343f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3343f-104">Kopiert den aktuellen Datensatz aus einem aktualisierbaren **[Recordset](recordset-object-dao.md)** -Objekt in den Kopierpuffer zur nachfolgenden Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="3343f-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3343f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3343f-105">Syntax</span></span>

<span data-ttu-id="3343f-106">*Ausdruck* . Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="3343f-106">*expression* .Edit</span></span>

<span data-ttu-id="3343f-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3343f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3343f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3343f-108">Remarks</span></span>

<span data-ttu-id="3343f-p101">Wenn Sie die **Edit**-Methode verwenden, werden Änderungen, die an den Feldern des aktuellen Datensatzes vorgenommen werden, in den Kopierpuffer kopiert. Speichern Sie die Änderungen mithilfe der **[Update](recordset2-update-method-dao.md)** -Methode, nachdem Sie die gewünschten Änderungen an dem Datensatz vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="3343f-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="3343f-111">Der aktuelle Datensatz bleibt nach der Verwendung von **Edit** aktuell.</span><span class="sxs-lookup"><span data-stu-id="3343f-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="3343f-112">[!HINWEIS] Wenn Sie einen Datensatz bearbeiten und dann durch einen beliebigen Vorgang zu einem anderen Datensatz wechseln, ohne zuerst **Update** zu verwenden, gehen Ihre Änderungen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="3343f-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="3343f-113">Außerdem wird der bearbeitete Datensatz ohne Warnung verworfen, wenn Sie Recordset beenden oder die Prozedur beenden, die das **Recordset** -oder das übergeordnete **[Database](database-object-dao.md)** -oder **[Connection](connection-object-dao.md)** -Objekt deklariert.</span><span class="sxs-lookup"><span data-stu-id="3343f-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="3343f-114">Die Verwendung von **Edit** erzeugt in folgenden Fällen einen Fehler:</span><span class="sxs-lookup"><span data-stu-id="3343f-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="3343f-115">Es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3343f-115">There is no current record.</span></span>

- <span data-ttu-id="3343f-116">Das **Connection**-, **Database**- oder **Recordset**-Objekt wurde schreibgeschützt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3343f-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="3343f-117">Der Datensatz enthält keine aktualisierbaren Felder.</span><span class="sxs-lookup"><span data-stu-id="3343f-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="3343f-118">Das **Database**- oder **Recordset**-Objekt wurde zur exklusiven Verwendung von einem anderen Benutzer geöffnet (Microsoft Access-Arbeitsbereich).</span><span class="sxs-lookup"><span data-stu-id="3343f-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="3343f-119">Ein anderer Benutzer hat die Seite mit Ihrem Datensatz gesperrt (Microsoft Access-Arbeitsbereich).</span><span class="sxs-lookup"><span data-stu-id="3343f-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="3343f-p103">Ist in einem Microsoft Access-Arbeitsbereich die [**LockEdits**](recordset2-lockedits-property-dao.md) -Eigenschafteneinstellung des **Recordset**-Objekts in einer Mehrbenutzerumgebung auf **True** festgelegt (pessimistisch gesperrt), bleibt der Datensatz ab dem Moment gesperrt, in dem **Edit** verwendet wird. Die Sperre wird erst dann aufgehoben, wenn die Aktualisierung abgeschlossen ist. Wenn die **LockEdits**-Eigenschafteneinstellung auf **False** festgelegt ist (optimistisch gesperrt), wird der Datensatz gesperrt und mit dem vorab bearbeiteten Datensatz verglichen, bevor er in der Datenbank aktualisiert wird. Wurde der Datensatz seit dem Verwenden der **Edit**-Methode geändert, schlägt die **Update**-Operation mit einem Laufzeitfehler fehl, falls Sie **OpenRecordset** anwenden, ohne **dbSeeChanges** anzugeben. Standardmäßig verwenden die mit einem Microsoft Access-Datenbankmodul verbundenen ODBC- und installierbare ISAM-Datenbanken immer optimistische Sperren.</span><span class="sxs-lookup"><span data-stu-id="3343f-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="3343f-p104">[!HINWEIS] Es muss ein eindeutiger Index für den Datensatz in der zugrunde liegenden Datenquelle vorhanden sein, damit ein Datensatz hinzugefügt, bearbeitet oder gelöscht werden kann. Andernfalls tritt im Aufruf der Methoden **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** oder **Edit** in einem Microsoft Access-Arbeitsbereich ein Fehler vom Typ "Berechtigung verweigert" auf.</span><span class="sxs-lookup"><span data-stu-id="3343f-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="3343f-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3343f-126">Example</span></span>

<span data-ttu-id="3343f-p105">In diesem Beispiel wird die **Edit**-Methode verwendet, um die aktuellen Daten durch den angegebenen Namen zu ersetzen. Die EditName-Prozedur ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3343f-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```

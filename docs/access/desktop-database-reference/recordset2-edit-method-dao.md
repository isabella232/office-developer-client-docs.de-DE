---
title: Recordset2.Edit-Methode (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707745"
---
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="d4df2-102">Recordset2.Edit-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d4df2-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="d4df2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4df2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4df2-104">Kopiert den aktuellen Datensatz aus einem aktualisierbaren **[Recordset](recordset-object-dao.md)** -Objekt zur nachfolgenden Bearbeitung in den Kopierpuffer.</span><span class="sxs-lookup"><span data-stu-id="d4df2-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4df2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4df2-105">Syntax</span></span>

<span data-ttu-id="d4df2-106">*Ausdruck* . Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="d4df2-106">*expression* .Edit</span></span>

<span data-ttu-id="d4df2-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d4df2-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4df2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4df2-108">Remarks</span></span>

<span data-ttu-id="d4df2-p101">Wenn Sie die **Edit** -Methode verwenden, werden an den Feldern des aktuellen Datensatzes vorgenommene Änderungen in den Kopierpuffer kopiert. Nachdem Sie die gewünschten Änderungen am Datensatz vorgenommen haben, verwenden Sie die **[Update](recordset2-update-method-dao.md)** -Methode, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d4df2-p101">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer. After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="d4df2-111">Der aktuelle Datensatz bleibt nach der Verwendung von **Edit** aktuell.</span><span class="sxs-lookup"><span data-stu-id="d4df2-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="d4df2-112">[!HINWEIS] Wenn Sie einen Datensatz bearbeiten und dann einen Vorgang durchführen, mit dem Sie zu einem anderen Datensatz wechseln, ohne jedoch zunächst **Update** zu verwenden, gehen Ihre Änderungen ohne Warnung verloren.</span><span class="sxs-lookup"><span data-stu-id="d4df2-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="d4df2-113">Darüber hinaus wird beim Schließen des Recordset-Objekts oder die Prozedur beenden, die das **Recordset-Objekt** oder das übergeordnete **[Datenbank-](database-object-dao.md)** oder **[Verbindungstyp](connection-object-dao.md)** Objekt deklariert, der bearbeitete Datensatz ohne Warnung verworfen.</span><span class="sxs-lookup"><span data-stu-id="d4df2-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="d4df2-114">Die Verwendung von **Edit** erzeugt in folgenden Fällen einen Fehler:</span><span class="sxs-lookup"><span data-stu-id="d4df2-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="d4df2-115">Es ist kein aktueller Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d4df2-115">There is no current record.</span></span>

- <span data-ttu-id="d4df2-116">Das **Connection** -, **Database** - oder **Recordset** -Objekt wurde schreibgeschützt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d4df2-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="d4df2-117">Der Datensatz enthält keine aktualisierbaren Felder.</span><span class="sxs-lookup"><span data-stu-id="d4df2-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="d4df2-118">Das **Database** - oder **Recordset** -Objekt wurde zur exklusiven Verwendung von einem anderen Benutzer geöffnet (Microsoft Access-Arbeitsbereich).</span><span class="sxs-lookup"><span data-stu-id="d4df2-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="d4df2-119">Ein anderer Benutzer hat die Seite mit Ihrem Datensatz gesperrt (Microsoft Access-Arbeitsbereich).</span><span class="sxs-lookup"><span data-stu-id="d4df2-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="d4df2-p103">Wenn in einem Microsoft Access-Arbeitsbereich die [**LockEdits**](recordset2-lockedits-property-dao.md) -Eigenschafteneinstellung des **Recordset** -Objekts in einer Mehrbenutzerumgebung auf **True** (pessimistisch gesperrt) festgelegt ist, bleibt der Datensatz ab dem Zeitpunkt der Verwendung von **Edit** bis zum Abschluss der Aktualisierung gesperrt. Wenn die **LockEdits** -Eigenschafteneinstellung auf **False** (optimistisch gesperrt) festgelegt ist, wird der Datensatz gesperrt und mit dem vorher bearbeiteten Datensatz verglichen, kurz bevor er in der Datenbank aktualisiert wird. Wenn der Datensatz seit der Verwendung der **Edit** -Methode geändert wurde, tritt beim **Update** -Vorgang ein Laufzeitfehler auf, falls Sie **OpenRecordset** ohne Angabe von **dbSeeChanges** verwenden. Standardmäßig verwenden mit dem Microsoft Access-Datenbankmodul verbundene ODBC- und installierbare ISAM-Datenbanken immer die optimistische Sperrung.</span><span class="sxs-lookup"><span data-stu-id="d4df2-p103">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete. If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database. If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**. By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="d4df2-p104">[!HINWEIS] Um einen Datensatz hinzuzufügen, zu bearbeiten oder zu löschen, muss es einen eindeutigen Index für den Datensatz in der zugrunde liegenden Datenquelle geben. Andernfalls tritt ein "Berechtigung verweigert"-Fehler im **[AddNew](recordset2-addnew-method-dao.md)** -, **[Delete](fields-delete-method-dao.md)** - oder **Edit** -Methodenaufruf in einem Microsoft Access-Arbeitsbereich auf.</span><span class="sxs-lookup"><span data-stu-id="d4df2-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="d4df2-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4df2-126">Example</span></span>

<span data-ttu-id="d4df2-p105">In diesem Beispiel wird die **Edit** -Methode verwendet, um die aktuellen Daten durch den angegebenen Namen zu ersetzen. Die EditName-Prozedur ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4df2-p105">This example uses the **Edit** method to replace the current data with the specified name. The EditName procedure is required for this procedure to run.</span></span>

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

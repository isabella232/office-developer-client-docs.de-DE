---
title: Field2 Object (DAO)
TOCTitle: Field2 Object
ms:assetid: 585aa163-402b-2c2b-d8d7-733a6d55d104
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194326(v=office.15)
ms:contentKeyID: 48544994
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ecc5bf969d0566982d2d3bf47c13919b13c610b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473926"
---
# <a name="field2-object-dao"></a><span data-ttu-id="cb05c-102">Field2 Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="cb05c-102">Field2 Object (DAO)</span></span>

<span data-ttu-id="cb05c-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb05c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cb05c-104">Ein **Field2**-Objekt stellt Daten mit einem gemeinsamen Datentyp in einer Spalte und einer typischen Gruppe von Eigenschaften dar.</span><span class="sxs-lookup"><span data-stu-id="cb05c-104">A **Field2** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb05c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb05c-105">Remarks</span></span>

<span data-ttu-id="cb05c-p101">Ein **Field2**-Objekt enthält dieselben Eigenschaften und Methoden wie das **[Field](field-object-dao.md)** -Objekt. Das **Field2**-Objekt enthält einige neue Eigenschaften und Methoden zur Unterstützung von mehrwertigen Feldern. Die folgenden neuen Eigenschaften und Methoden sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="cb05c-p101">A **Field2** object is contains all of the same properties and methods as the **[Field](field-object-dao.md)** object. The **Field2** object contains several new properties and methods that support multi-valued field types. The new properties and methods are:</span></span>

- <span data-ttu-id="cb05c-109">**[AppendOnly](field2-appendonly-property-dao.md)** -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb05c-109">**[AppendOnly](field2-appendonly-property-dao.md)** property</span></span>

- <span data-ttu-id="cb05c-110">**[ComplexType](field2-complextype-property-dao.md)** -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb05c-110">**[ComplexType](field2-complextype-property-dao.md)** property</span></span>

- <span data-ttu-id="cb05c-111">**[IsComplex](field2-iscomplex-property-dao.md)** -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb05c-111">**[IsComplex](field2-iscomplex-property-dao.md)** property</span></span>

- <span data-ttu-id="cb05c-112">**[LoadFromFile](field2-loadfromfile-method-dao.md)** -Methode</span><span class="sxs-lookup"><span data-stu-id="cb05c-112">**[LoadFromFile](field2-loadfromfile-method-dao.md)** method</span></span>

- <span data-ttu-id="cb05c-113">**[SaveToFile](field2-savetofile-method-dao.md)** -Methode</span><span class="sxs-lookup"><span data-stu-id="cb05c-113">**[SaveToFile](field2-savetofile-method-dao.md)** method</span></span>

<span data-ttu-id="cb05c-114">Wenn Sie auf ein **Field2**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="cb05c-114">To refer to a **Field2** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="cb05c-115">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="cb05c-115">**Fields**(0)</span></span>

<span data-ttu-id="cb05c-116">**Felder** ("Name")</span><span class="sxs-lookup"><span data-stu-id="cb05c-116">**Fields**("name")</span></span>

<span data-ttu-id="cb05c-117">**Felder**\!\[Namen\]</span><span class="sxs-lookup"><span data-stu-id="cb05c-117">**Fields**\!\[name\]</span></span>

<span data-ttu-id="cb05c-p102">Mit denselben Syntaxformen können Sie auch auf die **Value**-Eigenschaft eines von Ihnen erstellten **Field2**-Objekts verweisen, das Sie einer **Fields**-Auflistung anfügen. Der Kontext des Feldverweises bestimmt, ob sich der Verweis auf das **Field2**-Objekt oder die **Value**-Eigenschaft des **Field**-Objekts bezieht.</span><span class="sxs-lookup"><span data-stu-id="cb05c-p102">With the same syntax forms, you can also refer to the **Value** property of a **Field2** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field2** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="cb05c-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb05c-120">Example</span></span>

<span data-ttu-id="cb05c-121">Das folgende Beispiel zeigt, wie Sie durch ein Recordset-Objekt navigieren, das ein Mehrfachwertfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="cb05c-121">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="cb05c-122">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="cb05c-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub PrintStudentsAndClasses()
        Dim dbs As DAO.Database
        Dim rsStudents As DAO.Recordset2  'Recordset for students
        Dim rsClasses As DAO.Recordset2  'Recordset for classes
        Dim fld As DAO.Field2
    
        'open the database
        Set dbs = CurrentDb()
    
        'get the table of students
        Set rsStudents = dbs.OpenRecordset("tblStudents")
    
        'loop through the students
        Do While Not rsStudents.EOF
            
            'get the classes field
            Set fld = rsStudents("Classes")
    
            'get the classes Recordset
            'make sure the field is a multi-valued field before
            'getting a Recordset object
            If fld.IsComplex Then
                Set rsClasses = fld.Value
            End If
    
            'access all records in the Recordset
            If Not (rsClasses.BOF And rsClasses.EOF) Then
                rsClasses.MoveLast
                rsClasses.MoveFirst
            End If
    
            'print the student and number of classes
            Debug.Print rsStudents("FirstName") & " " & rsStudents("LastName"), _
                "Number of classes: " & rsClasses.RecordCount
    
            'print the classes for this student
            Do While Not rsClasses.EOF
                Debug.Print , rsClasses("Value")
                rsClasses.MoveNext
            Loop
    
            'close the Classes Recordset
            rsClasses.Close
    
            'get the next student
            rsStudents.MoveNext
    
        Loop
        
        'cleanup
        rsStudents.Close
    
        Set fld = Nothing
        Set rsStudents = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="cb05c-p103">Das folgende Beispiel zeigt, wie Sie durch die Dateien in einem Anlagenfeld navigieren. Der Dateityp und der Dateiname der einzelnen Anlagen werden im Direktfenster gedruckt.</span><span class="sxs-lookup"><span data-stu-id="cb05c-p103">The following example shows how to navigate the files in an attachment field. The file type and filename of each attachment is printed in the Immediate window.</span></span>

```vb
    Sub ListAttachments()
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Print the first and last name
            Debug.Print rst("FirstName") & " " & rst("LastName")
            
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Print all attachments in the field
            Do While Not rsA.EOF
                Debug.Print , rsA("FileType"), rsA("FileName")
                
                'Next attachment
                rsA.MoveNext
            Loop
            
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
            
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Sub
```

<br/>

<span data-ttu-id="cb05c-125">Das folgende Beispiel zeigt, wie Sie Dateien aus einem angegebenen Ordnerpfad zu einem Anlagenfeld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cb05c-125">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

```vb
    Public Function LoadAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld  As DAO.Field2
        Dim strFile As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Load all attachments in the specified directory
            strFile = Dir(strPath & "\*.*")
            
            rst.Edit
            Do While Len(strFile) > 0
                'Add a new attachment that matches the pattern.
                'Pass "" to match all files.
                If strFile Like strPattern Then
                    rsA.AddNew
                    rsA("FileData").LoadFromFile strPath & "\" & strFile
                    rsA.Update
                    
                    'Increment the number of files added
                    LoadAttachments = LoadAttachments + 1
                End If
                strFile = Dir
            Loop
            rsA.Close
            
            rst.Update
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

<br/>

<span data-ttu-id="cb05c-126">Das folgende Beispiel zeigt, wie Sie die in einem Anlagenfeld gespeicherten Dateien im angegebenen Ordnerpfad speichern.</span><span class="sxs-lookup"><span data-stu-id="cb05c-126">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

```vb
    Public Function SaveAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        Dim strFullPath As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Save all attachments in the field
            Do While Not rsA.EOF
                If rsA("FileName") Like strPattern Then
                    strFullPath = strPath & "\" & rsA("FileName")
                    
                    'Make sure the file does not exist and save
                    If Dir(strFullPath) = "" Then
                        rsA("FileData").SaveToFile strFullPath
                    End If
                    
                    'Increment the number of files saved
                    SaveAttachments = SaveAttachments + 1
                End If
                
                'Next attachment
                rsA.MoveNext
            Loop
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

<br/>

<span data-ttu-id="cb05c-127">Das folgende Beispiel zeigt, wie Sie eine in einem Anlagenfeld gespeicherte Datei löschen.</span><span class="sxs-lookup"><span data-stu-id="cb05c-127">The following example shows how to delete a file stored in an attachment field.</span></span>

```vb
    Function RemoveAttachment(strRemoveFile As String, Optional strFilter As String) As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database
        Set dbs = CurrentDb
        
        'Open the recordset. If the strFilter is supplied, add it to the WHERE
        'clause for the recordset. Otherwise, any files matching strFileName
        'will be deleted
        If Len(strFilter) > 0 Then
            Set rst = dbs.OpenRecordset("SELECT * FROM tblAttachments WHERE " & strFilter)
        Else
            Set rst = dbs.OpenRecordset("tblAttachments")
        End If
        
        'Get the Attachment field
        Set fld = rst("Attachments")
        
        'Navigate through the recordset
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Walk the attachments and look for the file name to remove
            Do While Not rsA.EOF
                If rsA("FileName") Like strRemoveFile Then
                    rsA.Delete
                    
                    'Increment the number of files removed
                    RemoveAttachment = RemoveAttachment + 1
                End If
                rsA.MoveNext
            Loop
                    
            'Cleanup the Attachments recordset
            rsA.Close
            Set rsA = Nothing
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        Set fld = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

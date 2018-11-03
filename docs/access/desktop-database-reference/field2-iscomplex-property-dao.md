---
title: Field2.IsComplex-Eigenschaft (DAO)
TOCTitle: IsComplex Property
ms:assetid: ffc90e6e-e3ee-4f9b-ca6b-615199300d45
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837318(v=office.15)
ms:contentKeyID: 48548970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 83fe55421bb5d45e53280c7ac323f571e1f4d88e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930035"
---
# <a name="field2iscomplex-property-dao"></a><span data-ttu-id="bb286-102">Field2.IsComplex-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="bb286-102">Field2.IsComplex property (DAO)</span></span>

<span data-ttu-id="bb286-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb286-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="bb286-p101">Gibt einen **Boolean**-Wert zurück, der angibt, ob das angegebene Feld ein mehrwertiger Datentyp ist. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bb286-p101">Returns **Boolean** that indicates whether the specified field is a multi-valued data type. Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="bb286-106">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="bb286-106">Version information</span></span>

<span data-ttu-id="bb286-107">Hinzugefügte Version: Access 2007</span><span class="sxs-lookup"><span data-stu-id="bb286-107">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="bb286-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb286-108">Syntax</span></span>

<span data-ttu-id="bb286-109">*Ausdruck* . IsComplex</span><span class="sxs-lookup"><span data-stu-id="bb286-109">*expression* .IsComplex</span></span>

<span data-ttu-id="bb286-110">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb286-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="example"></a><span data-ttu-id="bb286-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bb286-111">Example</span></span>

<span data-ttu-id="bb286-112">Das folgende Beispiel zeigt, wie Sie durch ein Recordset-Objekt navigieren, das ein Mehrfachwertfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="bb286-112">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="bb286-113">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bb286-113">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

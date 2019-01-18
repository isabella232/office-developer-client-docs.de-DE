---
title: Field2.LoadFromFile-Methode (DAO)
TOCTitle: LoadFromFile Method
ms:assetid: 8ffe4636-d4da-0579-f4b5-14f423647562
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197396(v=office.15)
ms:contentKeyID: 48546314
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101190
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bdb1ba92c4a0f4fbee7204b2f4fee8a96c87cc1b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710629"
---
# <a name="field2loadfromfile-method-dao"></a><span data-ttu-id="c0629-102">Field2.LoadFromFile-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0629-102">Field2.LoadFromFile method (DAO)</span></span>

<span data-ttu-id="c0629-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0629-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0629-104">Lädt die angegebene Datei vom Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c0629-104">Loads the specified file from disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="c0629-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="c0629-105">Version information</span></span>

<span data-ttu-id="c0629-106">Hinzugefügte Version: Access 2007</span><span class="sxs-lookup"><span data-stu-id="c0629-106">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="c0629-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0629-107">Syntax</span></span>

<span data-ttu-id="c0629-108">*Ausdruck* . LoadFromFile (***FileName***)</span><span class="sxs-lookup"><span data-stu-id="c0629-108">*expression* .LoadFromFile(***FileName***)</span></span>

<span data-ttu-id="c0629-109">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0629-109">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0629-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0629-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0629-111">Name</span><span class="sxs-lookup"><span data-stu-id="c0629-111">Name</span></span></p></th>
<th><p><span data-ttu-id="c0629-112">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="c0629-112">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c0629-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c0629-113">Data type</span></span></p></th>
<th><p><span data-ttu-id="c0629-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0629-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0629-115"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="c0629-115"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="c0629-116">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0629-116">Required</span></span></p></td>
<td><p><span data-ttu-id="c0629-117"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="c0629-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c0629-118">Der vollständig qualifizierte Pfad der Datei, die geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0629-118">The fully qualified path of the file to that you want to load.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="c0629-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0629-119">Example</span></span>

<span data-ttu-id="c0629-120">Im folgenden Codeausschnitt wird mithilfe der **LoadFromFile**-Methode das Bild eines Mitarbeiters vom Datenträger geladen.</span><span class="sxs-lookup"><span data-stu-id="c0629-120">The following code snippet uses the **LoadFromFile** method to load an employee's picture from disk.</span></span>

```vb 
   '  Instantiate the parent recordset.  
   Set rsEmployees = db.OpenRecordset("Employees") 
  
   … Code to move to desired employee 
  
   ' Activate edit mode. 
   rsEmployees.Edit 
  
   ' Instantiate the child recordset. 
   Set rsPictures = rsEmployees.Fields("Pictures").Value  
  
   ' Add a new attachment. 
   rsPictures.AddNew 
   rsPictures.Fields("FileData").LoadFromFile "EmpPhoto39392.jpg" 
   rsPictures.Update 
  
   ' Update the parent record 
   rsEmployees.Update 
```

<br/>

<span data-ttu-id="c0629-121">Das folgende Beispiel zeigt, wie Sie Dateien aus einem angegebenen Ordnerpfad zu einem Anlagenfeld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0629-121">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

<span data-ttu-id="c0629-122">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c0629-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

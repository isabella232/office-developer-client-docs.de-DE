---
title: Recordset.NoMatch-Eigenschaft (DAO)
TOCTitle: NoMatch Property
ms:assetid: 47d03575-f570-89b5-a20f-a3bd8b8b5c6d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193226(v=office.15)
ms:contentKeyID: 48544606
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052889
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 003cb9927b46843a3618e66943b230460677d7e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475442"
---
# <a name="recordsetnomatch-property-dao"></a><span data-ttu-id="576a0-102">Recordset.NoMatch-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="576a0-102">Recordset.NoMatch Property (DAO)</span></span>

<span data-ttu-id="576a0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="576a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="576a0-104">Gibt an, ob ein bestimmter Datensatz mithilfe der **[Seek](recordset-seek-method-dao.md)** -Methode oder einer der **[Find](recordset-findfirst-method-dao.md)** -Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="576a0-104">Indicates whether a particular record was found by using the **[Seek](recordset-seek-method-dao.md)** method or one of the **[Find](recordset-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="576a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="576a0-105">Syntax</span></span>

<span data-ttu-id="576a0-106">*Ausdruck* . NoMatch</span><span class="sxs-lookup"><span data-stu-id="576a0-106">*expression* .NoMatch</span></span>

<span data-ttu-id="576a0-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="576a0-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="576a0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="576a0-108">Remarks</span></span>

<span data-ttu-id="576a0-109">Wenn Sie ein **[Recordset](recordset-object-dao.md)** -Objekt öffnen oder erstellen, hat seine **NoMatch**-Eigenschaft den Wert **False**.</span><span class="sxs-lookup"><span data-stu-id="576a0-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="576a0-p101">Verwenden Sie für die Suche nach einem Datensatz die **Seek** -Methode für ein **Recordset** -Objekt vom Tabellentyp oder die **Find** -Methoden für ein **Recordset** -Objekt vom Dynaset- oder Momentaufnahmentyp. Überprüfen Sie die **NoMatch** -Eigenschaftseinstellung, um festzustellen, ob der Datensatz gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="576a0-p101">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object. Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="576a0-p102">Wenn die Methoden **Seek** und **Find** nicht erfolgreich sind und die **NoMatch**-Eigenschaft den Wert **True** hat, ist der aktuelle Datensatz nicht mehr gültig. Rufen Sie das Lesezeichen des aktuellen Datensatzes ab, bevor Sie die **Seek**-Methode oder eine **Find**-Methode verwenden, falls Sie zu diesem Datensatz zurückkehren müssen.</span><span class="sxs-lookup"><span data-stu-id="576a0-p102">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid. Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>


> [!NOTE]
> <span data-ttu-id="576a0-114">[!HINWEIS] Das Verwenden einer der **[Move](recordset-movefirst-method-dao.md)** -Methoden für ein **Recordset**-Objekt hat keinen Einfluss auf die Einstellung seiner **NoMatch**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="576a0-114">Using any of the **[Move](recordset-movefirst-method-dao.md)** methods on a **Recordset** object won't affect its **NoMatch** property setting.</span></span>


## <a name="example"></a><span data-ttu-id="576a0-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="576a0-115">Example</span></span>

<span data-ttu-id="576a0-p103">In diesem Beispiel wird die **NoMatch** -Eigenschaft verwendet, um zu bestimmen, ob **Seek** und **FindFirst** erfolgreich waren, und falls nicht, entsprechendes Feedback zu geben. Die Vorgehensweisen SeekMatch und FindMatch sind erforderlich, damit dieses Verfahren ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="576a0-p103">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="576a0-118">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der Seek-Methode einen Datensatz in einer verknüpften Tabelle finden.</span><span class="sxs-lookup"><span data-stu-id="576a0-118">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="576a0-119">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="576a0-119">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```

---
title: Recordset2.NoMatch-Eigenschaft (DAO)
TOCTitle: NoMatch Property
ms:assetid: 2d7a02ff-a2bf-5f0e-bd71-a6d42c25b13a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192114(v=office.15)
ms:contentKeyID: 48543972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 083e76ea4e2a0800153d50fa0c61d5acb7a29645
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922181"
---
# <a name="recordset2nomatch-property-dao"></a><span data-ttu-id="a267d-102">Recordset2.NoMatch-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="a267d-102">Recordset2.NoMatch property (DAO)</span></span>


<span data-ttu-id="a267d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a267d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a267d-104">Gibt an, ob ein bestimmter Datensatz mithilfe der **[Seek](recordset2-seek-method-dao.md)** -Methode oder einer der **[Find](recordset2-findfirst-method-dao.md)** -Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a267d-104">Indicates whether a particular record was found by using the **[Seek](recordset2-seek-method-dao.md)** method or one of the **[Find](recordset2-findfirst-method-dao.md)** methods (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a267d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a267d-105">Syntax</span></span>

<span data-ttu-id="a267d-106">*Ausdruck* . NoMatch</span><span class="sxs-lookup"><span data-stu-id="a267d-106">*expression* .NoMatch</span></span>

<span data-ttu-id="a267d-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a267d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a267d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a267d-108">Remarks</span></span>

<span data-ttu-id="a267d-109">Wenn Sie ein **[Recordset](recordset-object-dao.md)** -Objekt öffnen oder erstellen, hat seine **NoMatch**-Eigenschaft den Wert **False**.</span><span class="sxs-lookup"><span data-stu-id="a267d-109">When you open or create a **[Recordset](recordset-object-dao.md)** object, its **NoMatch** property is set to **False**.</span></span>

<span data-ttu-id="a267d-p101">Verwenden Sie für die Suche nach einem Datensatz die **Seek** -Methode für ein **Recordset** -Objekt vom Tabellentyp oder die **Find** -Methoden für ein **Recordset** -Objekt vom Dynaset- oder Momentaufnahmentyp. Überprüfen Sie die **NoMatch** -Eigenschaftseinstellung, um festzustellen, ob der Datensatz gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a267d-p101">To locate a record, use the **Seek** method on a table-type **Recordset** object or one of the **Find** methods on a dynaset- or snapshot-type **Recordset** object. Check the **NoMatch** property setting to see whether the record was found.</span></span>

<span data-ttu-id="a267d-p102">Wenn die Methoden **Seek** und **Find** nicht erfolgreich sind und die **NoMatch**-Eigenschaft den Wert **True** hat, ist der aktuelle Datensatz nicht mehr gültig. Rufen Sie das Lesezeichen des aktuellen Datensatzes ab, bevor Sie die **Seek**-Methode oder eine **Find**-Methode verwenden, falls Sie zu diesem Datensatz zurückkehren müssen.</span><span class="sxs-lookup"><span data-stu-id="a267d-p102">If the **Seek** or **Find** method is unsuccessful and the **NoMatch** property is **True**, the current record will no longer be valid. Be sure to obtain the current record's bookmark before using the **Seek** method or a **Find** method if you'll need to return to that record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a267d-114">[!HINWEIS] Das Verwenden einer der <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> -Methoden für ein <STRONG>Recordset</STRONG>-Objekt hat keinen Einfluss auf die Einstellung seiner <STRONG>NoMatch</STRONG>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a267d-114">Using any of the <STRONG><A href="recordset-movefirst-method-dao.md">Move</A></STRONG> methods on a <STRONG>Recordset</STRONG> object won't affect its <STRONG>NoMatch</STRONG> property setting.</span></span></P>



## <a name="example"></a><span data-ttu-id="a267d-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a267d-115">Example</span></span>

<span data-ttu-id="a267d-p103">In diesem Beispiel wird anhand der NoMatch-Eigenschaft ermittelt, ob Seek und FindFirst erfolgreich waren. Wenn nicht, wird entsprechendes Feedback zurückgegeben. Damit dieser Vorgang ausgeführt werden kann, sind die SeekMatch- und FindMatch-Prozeduren erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a267d-p103">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
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
     
    Sub SeekMatch(rstTemp As Recordset2, _ 
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

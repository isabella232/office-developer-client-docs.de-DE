---
title: Recordset2.CopyQueryDef Method (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: 36689ac0-f8a6-1f3e-4170-799141373777
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192474(v=office.15)
ms:contentKeyID: 48544170
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053073
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e70093a6678a61874462ec3517f6424e5da79f71
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605583"
---
# <a name="recordset2copyquerydef-method-dao"></a><span data-ttu-id="05478-102">Recordset2.CopyQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="05478-102">Recordset2.CopyQueryDef Method (DAO)</span></span>


<span data-ttu-id="05478-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05478-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="05478-104">Gibt ein **[QueryDef](querydef-object-dao.md)** -Objekt, das eine Kopie des **QueryDef-Objekt** ist verwendeten zum Erstellen des **[Recordset](recordset-object-dao.md)** -Objekts, dargestellt durch das Recordset-Objekt-Platzhalter (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="05478-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="05478-105">.</span><span class="sxs-lookup"><span data-stu-id="05478-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="05478-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="05478-106">Syntax</span></span>

<span data-ttu-id="05478-107">*Ausdruck* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="05478-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="05478-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="05478-108">*expression* A variable that represents a **Recordset2** object.</span></span>

<span data-ttu-id="05478-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="05478-109"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="05478-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05478-110">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="05478-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05478-111">Return value</span></span>
>>>>>>> <span data-ttu-id="05478-112">master</span><span class="sxs-lookup"><span data-stu-id="05478-112">master</span></span>

<span data-ttu-id="05478-113">QueryDef-Objekt</span><span class="sxs-lookup"><span data-stu-id="05478-113">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="05478-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05478-114">Remarks</span></span>

<span data-ttu-id="05478-115">Mithilfe der **CopyQueryDef**-Methode können Sie ein neues **QueryDef**-Objekt erstellen, welches ein Duplikat des **QueryDef**-Objekts darstellt, das zum Erstellen des **Recordset**-Objekts dient.</span><span class="sxs-lookup"><span data-stu-id="05478-115">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="05478-p102">Wurde zum Erstellen dieses **Recordset**-Objekts kein **QueryDef**-Objekt verwendet, tritt ein Fehler auf. Sie müssen zuerst ein **Recordset**-Objekt mithilfe der **OpenRecordset**-Methode öffnen, bevor Sie die **CopyQueryDef**-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="05478-p102">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs. You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="05478-118">Diese Methode ist hilfreich, wenn Sie ein **Recordset**-Objekt aus einem **QueryDef**-Objekt erstellen und das **Recordset**-Objekt an eine Funktion übergeben, die die SQL-Entsprechung der Abfrage erneut erstellen muss, beispielsweise um sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="05478-118">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="05478-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="05478-119">Example</span></span>

<span data-ttu-id="05478-p103">In diesem Beispiel wird die **CopyQueryDef**-Methode zum Erstellen der Kopie eines **QueryDef**-Objekts aus einem vorhandenen **Recordset**-Objekt verwendet. Die Kopie wird durch das Hinzufügen einer Klausel zur SQL-Eigenschaft geändert. Beim Erstellen eines permanenten **QueryDef**-Objekts können Sie der SQL-Eigenschaft Leerzeichen, Semikolon und Zeilenvorschub hinzufügen. Diese zusätzlichen Zeichen müssen entfernt werden, bevor neue Klauseln an die SQL-Anweisung angehängt werden können.</span><span class="sxs-lookup"><span data-stu-id="05478-p103">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```     

<br/>

<span data-ttu-id="05478-122">Dieses Beispiel zeigt eine mögliche Verwendung von CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="05478-122">This example shows a possible use of CopyQueryNew().</span></span>

```vb
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset2 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```


---
title: Recordset.Clone-Methode (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 37f78b428cc4f872743fe39403608074460b276a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474902"
---
# <a name="recordsetclone-method-dao"></a><span data-ttu-id="926b9-102">Recordset.Clone-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="926b9-102">Recordset.Clone Method (DAO)</span></span>


<span data-ttu-id="926b9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="926b9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="926b9-104">Erstellt ein dupliziertes **[Recordset](recordset-object-dao.md)** -Objekt, das auf das ursprüngliche **Recordset** -Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="926b9-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="926b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="926b9-105">Syntax</span></span>

<span data-ttu-id="926b9-106">*Ausdruck* . Wenn Sie den Klon</span><span class="sxs-lookup"><span data-stu-id="926b9-106">*expression* .Clone</span></span>

<span data-ttu-id="926b9-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="926b9-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="926b9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="926b9-108">Return Value</span></span>

<span data-ttu-id="926b9-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="926b9-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="926b9-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="926b9-110">Remarks</span></span>

<span data-ttu-id="926b9-p101">Verwenden Sie die **Clone** -Methode, um mehrere duplizierte **Recordset** -Objekte zu erstellen. Jedes **Recordset** kann einen eigenen aktuellen Datensatz haben. Wenn Sie **Clone** alleine verwenden, werden die Daten in den Objekten oder in den zugrunde liegenden Strukturen nicht geändert. Bei Verwendung der **Clone** -Methode können Sie Lesezeichen zwischen zwei oder mehr **Recordset** -Objekten freigeben, da ihre Lesezeichen austauschbar sind.</span><span class="sxs-lookup"><span data-stu-id="926b9-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each **Recordset** can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="926b9-p102">Sie können die **Clone** -Methode verwenden, wenn Sie einen Vorgang für ein **Recordset** ausführen möchten, für den mehrere aktuelle Datensätze erforderlich ist. Dies ist schneller und effizienter, als ein zweites **Recordset** zu öffnen. Ein mit der **Clone** -Methode erstelltes **Recordset** hat zunächst keinen aktuellen Datensatz. Um einen Datensatz aktuell zu machen, bevor Sie das **Recordset** klonen, müssen Sie die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft festlegen oder eine der **[Move](recordset-movefirst-method-dao.md)** -Methoden, eine der **[Find](recordset-findfirst-method-dao.md)** -Methoden oder die **[Seek](recordset-seek-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="926b9-p102">You can use the **Clone** method when you want to perform an operation on a **Recordset** that requires multiple current records. This is faster and more efficient than opening a second **Recordset**. When you create a **Recordset** with the **Clone** method, it initially lacks a current record. To make a record current before you use the **Recordset** clone, you must set the **[Bookmark](recordset-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset-findfirst-method-dao.md)** methods, or the **[Seek](recordset-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="926b9-p103">Die Anwendung der **[Close](connection-close-method-dao.md)** -Methode auf das ursprüngliche oder das duplizierte Objekt wirkt sich nicht auf das jeweils andere Objekt aus. Wenn Sie z. B. **Close** für das ursprüngliche **Recordset** ausführen, wird der Klon nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="926b9-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original **Recordset** doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="926b9-121">Wenn Sie den Klon einer Datensatzgruppe in einer ausstehenden Transaktion schließen, wird eine implizite <STRONG>Rollback</STRONG>-Operation verursacht.</span><span class="sxs-lookup"><span data-stu-id="926b9-121">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="926b9-p104">Wenn Sie ein <STRONG>Recordset</STRONG>-Tabellenobjekt in einem Microsoft Access-Arbeitsbereich klonen, wird die <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG>-Eigenschafteneinstellung nicht in die neue Kopie des Recordset geklont. Sie müssen die <STRONG>Index</STRONG>-Eigenschafteneinstellung manuell kopieren.</span><span class="sxs-lookup"><span data-stu-id="926b9-p104">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset. You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="926b9-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="926b9-124">Example</span></span>

<span data-ttu-id="926b9-125">In diesem Beispiel werden mit der **Clone** -Methode Kopien eines **Recordset** erstellt. Anschließend kann der Benutzer den Datensatzzeiger jeder Kopie unabhängig positionieren.</span><span class="sxs-lookup"><span data-stu-id="926b9-125">This example uses the **Clone** method to create copies of a **Recordset** and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```

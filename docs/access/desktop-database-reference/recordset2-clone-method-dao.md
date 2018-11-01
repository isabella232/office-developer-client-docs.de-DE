---
title: Recordset2.Clone Method (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95d02f56a7c1e916bd0b6181a7a22b3cebb9d9b1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875028"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="b66c8-102">Recordset2.Clone Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="b66c8-102">Recordset2.Clone Method (DAO)</span></span>


<span data-ttu-id="b66c8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b66c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b66c8-104">Erstellt ein doppeltes **[Recordset](recordset-object-dao.md)** -Objekt, das auf das ursprüngliche **Recordset2**-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="b66c8-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b66c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b66c8-105">Syntax</span></span>

<span data-ttu-id="b66c8-106">*Ausdruck* . Wenn Sie den Klon</span><span class="sxs-lookup"><span data-stu-id="b66c8-106">*expression* .Clone</span></span>

<span data-ttu-id="b66c8-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b66c8-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="b66c8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b66c8-108">Return value</span></span>

<span data-ttu-id="b66c8-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="b66c8-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="b66c8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b66c8-110">Remarks</span></span>

<span data-ttu-id="b66c8-p101">Verwenden Sie die **Clone**-Methode zum Erstellen mehrerer **Recordset**-Objektduplikate. Jede Datensatzgruppe kann über einen eigenen aktuellen Datensatz verfügen. Die Verwendung von **Clone** führt noch nicht dazu, dass Daten in den Objekten oder in ihren zugrunde liegenden Strukturen geändert werden. Mit der **Clone**-Methode können Sie Lesezeichen in mehreren **Recordset2**-Objekten gemeinsam verwenden, da ihre Lesezeichen austauschbar sind.</span><span class="sxs-lookup"><span data-stu-id="b66c8-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each recordset can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="b66c8-p102">Die **Clone**-Methode können Sie verwenden, um eine Operation für eine Datensatzgruppe auszuführen, die mehrere aktuelle Datensätze erfordert. Das geht schneller und ist effizienter, als eine zweite Datensatzgruppe zu öffnen. Wenn Sie eine Datensatzgruppe mit der **Clone**-Methode erstellen, fehlt zunächst ein aktueller Datensatz. Legen Sie zuerst die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft fest, oder verwenden Sie eine der **[Move](recordset-movefirst-method-dao.md)** -Methoden, eine der **[Find](recordset2-findfirst-method-dao.md)** -Methoden oder die **[Seek](recordset2-seek-method-dao.md)** -Methode, um einen Datensatz zum aktuellen Datensatz zu machen, bevor Sie den Klon der Datensatzgruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="b66c8-p102">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records. This is faster and more efficient than opening a second recordset. When you create a recordset with the **Clone** method, it initially lacks a current record. To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="b66c8-p103">Das Anwenden der **[Close](connection-close-method-dao.md)** -Methode auf das ursprüngliche oder das duplizierte Objekt wirkt sich nicht auf das jeweils andere Objekt aus. Angenommen, Sie verwenden **Close** für die ursprüngliche Datensatzgruppe, so wird der Klon nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="b66c8-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original recordset doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="b66c8-121">Wenn Sie den Klon einer Datensatzgruppe in einer ausstehenden Transaktion schließen, wird eine implizite <STRONG>Rollback</STRONG>-Operation verursacht.</span><span class="sxs-lookup"><span data-stu-id="b66c8-121">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="b66c8-p104">Wenn Sie ein <STRONG>Recordset</STRONG>-Tabellenobjekt in einem Microsoft Access-Arbeitsbereich klonen, wird die <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG>-Eigenschafteneinstellung nicht in die neue Kopie des Recordset geklont. Sie müssen die <STRONG>Index</STRONG>-Eigenschafteneinstellung manuell kopieren.</span><span class="sxs-lookup"><span data-stu-id="b66c8-p104">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset. You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="b66c8-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b66c8-124">Example</span></span>

<span data-ttu-id="b66c8-125">In diesem Beispiel wird die **Clone**-Methode zum Erstellen von Kopien einer Datensatzgruppe verwendet. Dann kann der Benutzer den Datensatzzeiger für jede Kopie unabhängig positionieren.</span><span class="sxs-lookup"><span data-stu-id="b66c8-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
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

---
title: Recordset2.Seek-Methode (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9510faab9035f2b2cbcccae0a8ddefa484a95cb1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700647"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="12c30-102">Recordset2.Seek-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="12c30-102">Recordset2.Seek method (DAO)</span></span>

<span data-ttu-id="12c30-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12c30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12c30-104">Sucht den Datensatz in einem indizierten **Recordset** -Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="12c30-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="12c30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12c30-105">Syntax</span></span>

<span data-ttu-id="12c30-106">*Ausdruck* . Seek (***Vergleich***, ***Key1***, ***Key2***, ***Key3***, ***Schlüssel4***, ***Schlüssel bezieht. 5***, ***Key6***, ***Key7***, ***Key8***, ***"Key9" entsprechen***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="12c30-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="12c30-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="12c30-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="12c30-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12c30-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12c30-109">Name</span><span class="sxs-lookup"><span data-stu-id="12c30-109">Name</span></span></p></th>
<th><p><span data-ttu-id="12c30-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="12c30-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="12c30-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="12c30-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="12c30-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12c30-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12c30-113"><em>Comparison</em></span><span class="sxs-lookup"><span data-stu-id="12c30-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="12c30-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="12c30-114">Required</span></span></p></td>
<td><p><span data-ttu-id="12c30-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="12c30-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="12c30-116">Einer der folgenden Zeichenfolgenausdrücke: &lt;, &lt;=, =, &gt;= oder &gt;.</span><span class="sxs-lookup"><span data-stu-id="12c30-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12c30-117"><em>Key1, Key2...Key13</em></span><span class="sxs-lookup"><span data-stu-id="12c30-117"><em>Key1, Key2...Key13</em></span></span></p></td>
<td><p><span data-ttu-id="12c30-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="12c30-118">Required</span></span></p></td>
<td><p><span data-ttu-id="12c30-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="12c30-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="12c30-120">Mindestens ein Wert, der den Feldern im aktuellen Index des <strong>Recordset</strong> -Objekts gemäß der Angabe seiner Einstellungen für die Eigenschaft <strong>Index</strong> entspricht.</span><span class="sxs-lookup"><span data-stu-id="12c30-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="12c30-121">Sie können bis zu 13 wichtige Argumente verwenden.</span><span class="sxs-lookup"><span data-stu-id="12c30-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="12c30-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12c30-122">Remarks</span></span>

<span data-ttu-id="12c30-p102">Bevor Sie **Seek** verwenden können, müssen Sie den aktuellen Index mit der **Index**-Eigenschaft festlegen. Wenn der Index ein nicht eindeutiges Schlüsselfeld identifiziert, sucht **Seek** nach dem ersten Datensatz, der die Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="12c30-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="12c30-125">Die **Seek** -Methode werden die angegebenen Schlüsselfelder durchsucht und sucht den ersten Datensatz, der Key1 und Demgegenüber angegebenen Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="12c30-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="12c30-126">Wenn er gefunden wurde, wird er zum aktuellen Datensatz gemacht, und die **NoMatch**-Eigenschaft wird auf **False** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12c30-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="12c30-127">Falls mit der **Seek**-Methode kein Suchergebnis erzielt wird, wird die **NoMatch**-Eigenschaft auf **True** festgelegt, und der aktuelle Datensatz ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="12c30-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="12c30-128">Wenn Vergleich ist gleich (=), größer als oder gleich (\>=), größer oder gleich (\>), **Seek** beginnt am Anfang des Index und sucht vorwärts.</span><span class="sxs-lookup"><span data-stu-id="12c30-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="12c30-129">Wenn Vergleich ist kleiner als (\<) oder kleiner oder gleich (\<=), **Seek** beginnt am Ende des Index und sucht rückwärts.</span><span class="sxs-lookup"><span data-stu-id="12c30-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="12c30-130">Wenn doppelte Einträge am Ende des Index vorhanden sind, **Seek** bei einem beliebigen Eintrag in der Duplikaten startet und sucht rückwärts.</span><span class="sxs-lookup"><span data-stu-id="12c30-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="12c30-131">Sie müssen für alle im Index definierten Felder Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="12c30-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="12c30-132">Wenn Sie **Seek** mit einem mehrspaltigen Index verwenden und Sie keinen Vergleichswert für jedes Feld im Index angeben, können Sie im Vergleich nicht den Operator "gleich" (=) verwenden.</span><span class="sxs-lookup"><span data-stu-id="12c30-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="12c30-133">Dies liegt daran einige Kriterienfelder (key2, key3 usw.) auf NULL-Wert festgelegt wird, die wahrscheinlich nicht übereinstimmt, wird.</span><span class="sxs-lookup"><span data-stu-id="12c30-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="12c30-134">Aus diesem Grund funktioniert der Operator "gleich" nur dann ordnungsgemäß, wenn Sie einen Datensatz verwenden, der außer bei dem Schlüssel, den Sie suchen, durchgängig **Null** ist.</span><span class="sxs-lookup"><span data-stu-id="12c30-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="12c30-135">Es wird empfohlen, die Sie verwenden, die größer als oder gleich (\>=) Operator stattdessen.</span><span class="sxs-lookup"><span data-stu-id="12c30-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="12c30-136">Das Argument key1 muss dieselbe Feld Datentyp aufweisen wie das entsprechende Feld im aktuellen Index.</span><span class="sxs-lookup"><span data-stu-id="12c30-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="12c30-137">Beispielsweise muss der aktuelle Index auf ein Zahlenfeld (wie Mitarbeiter-ID) verweist, numerisch key1 sein.</span><span class="sxs-lookup"><span data-stu-id="12c30-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="12c30-138">Entsprechend muss der aktuelle Index auf ein Textfeld (beispielsweise Nachname) verweist, key1 eine Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="12c30-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="12c30-139">Beim Verwenden von **Seek** muss kein aktueller Datensatz vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="12c30-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="12c30-140">Zum Auflisten der vorhandenen Indizes können Sie die **[Indexes](indexes-collection-dao.md)** -Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="12c30-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="12c30-p107">Mithilfe der [**Find**](recordset2-findfirst-method-dao.md) -Methoden können Sie in einem **Recordset** -Objekt vom Typ "Dynaset" oder "Snapshot" nach einem Datensatz suchen, der einer bestimmten Bedingung entspricht, die nicht in vorhandenen Indizes vorhanden ist. Sollen alle Datensätze gefunden werden, nicht nur diejenigen, die eine bestimmte Bedingung erfüllen, bewegen Sie sich mithilfe der **[Move](recordset-movefirst-method-dao.md)** -Methoden von Datensatz zu Datensatz.</span><span class="sxs-lookup"><span data-stu-id="12c30-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="12c30-p108">Sie können die **Seek** -Methode nicht auf eine verknüpfte Tabelle anwenden, da verknüpfte Tabellen als **Recordset** -Objekte vom Typ Tabelle nicht geöffnet werden können. Wenn Sie jedoch die **[OpenDatabase](dbengine-opendatabase-method-dao.md)** -Methode verwenden, um eine installierbare ISAM (nicht ODBC)-Datenbank direkt zu öffnen, können Sie **Seek** auf Tabellen in dieser Datenbank anwenden.</span><span class="sxs-lookup"><span data-stu-id="12c30-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="12c30-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="12c30-145">Example</span></span>

<span data-ttu-id="12c30-146">In diesem Beispiel wird die **Seek**-Methode veranschaulicht. Der Benutzer kann auf Basis einer ID-Nummer nach einem Produkt suchen.</span><span class="sxs-lookup"><span data-stu-id="12c30-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim intFirst As Integer 
     Dim intLast As Integer 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' You must open a table-type Recordset to use an index, 
     ' and hence the Seek method. 
     Set rstProducts = _ 
     dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
     With rstProducts 
     ' Set the index. 
     .Index = "PrimaryKey" 
     
     ' Get the lowest and highest product IDs. 
     .MoveLast 
     intLast = !ProductID 
     .MoveFirst 
     intFirst = !ProductID 
     
     Do While True 
     ' Display current record information and ask user 
     ' for ID number. 
     strMessage = "Product ID: " & !ProductID & vbCr & _ 
     "Name: " & !ProductName & vbCr & vbCr & _ 
     "Enter a product ID between " & intFirst & _ 
     " and " & intLast & "." 
     strSeek = InputBox(strMessage) 
     
     If strSeek = "" Then Exit Do 
     
     ' Store current bookmark in case the Seek fails. 
     varBookmark = .Bookmark 
     
     .Seek "=", Val(strSeek) 
     
     ' Return to the current record if the Seek fails. 
     If .NoMatch Then 
     MsgBox "ID not found!" 
     .Bookmark = varBookmark 
     End If 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="12c30-p109">In diesem Beispiel wird die **NoMatch** -Eigenschaft verwendet, um zu bestimmen, ob **Seek** und **FindFirst** erfolgreich waren, und falls nicht, entsprechendes Feedback zu geben. Die Prozeduren SeekMatch und FindMatch sind erforderlich, damit dieses Verfahren ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12c30-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

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

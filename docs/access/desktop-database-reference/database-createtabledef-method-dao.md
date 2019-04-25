---
title: Database.CreateTableDef-Methode (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c986f0a96c14dac8a9ee4f3c7fded5a049fa451e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294946"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="8c162-102">Database.CreateTableDef-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8c162-102">Database.CreateTableDef Method (DAO)</span></span>

<span data-ttu-id="8c162-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c162-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c162-104">Erstellt ein neues **[TableDef](tabledef-object-dao.md)**-Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="8c162-104">Creates a new [**TableDef**](tabledef-object-dao.md) object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8c162-105">.</span><span class="sxs-lookup"><span data-stu-id="8c162-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="8c162-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c162-106">Syntax</span></span>

<span data-ttu-id="8c162-107">*Ausdruck*.CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="8c162-107">offexpression.CreateTableDef(\*\*\*\*Name\*\*\*\*, ***Attributes***, ***SourceTableName, \*\*\*\*\*\*Connect***)</span></span>

<span data-ttu-id="8c162-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c162-108">*expression*  A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c162-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c162-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c162-110">Name</span><span class="sxs-lookup"><span data-stu-id="8c162-110">Name</span></span></p></th>
<th><p><span data-ttu-id="8c162-111">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="8c162-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8c162-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8c162-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="8c162-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c162-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c162-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8c162-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8c162-115">Optional</span><span class="sxs-lookup"><span data-stu-id="8c162-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c162-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c162-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c162-117">Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>), der neue <strong>TableDef</strong> eindeutig benennt.</span><span class="sxs-lookup"><span data-stu-id="8c162-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="8c162-118">Unter der <strong><a href="tabledef-name-property-dao.md">Name</a></strong> -Eigenschaft finden Sie Einzelheiten zu gültigen <strong>TableDef</strong> -Namen.</span><span class="sxs-lookup"><span data-stu-id="8c162-118">See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c162-119"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="8c162-119"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="8c162-120">Optional</span><span class="sxs-lookup"><span data-stu-id="8c162-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c162-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c162-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c162-p103">Eine Konstante oder Kombination aus Konstanten, mit der mindestens ein Merkmal des neuen <strong>TableDef</strong>-Objekts angegeben wird. Weitere Informationen finden Sie im Thema zur <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8c162-p103">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c162-124"><em>SourceTableName</em></span><span class="sxs-lookup"><span data-stu-id="8c162-124"><em>SourceTableName property</em></span></span></p></td>
<td><p><span data-ttu-id="8c162-125">Optional</span><span class="sxs-lookup"><span data-stu-id="8c162-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c162-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c162-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c162-127">Ein <strong>Variant</strong>-Parameter (Untertyp<strong>String</strong>) mit dem Namen einer Tabelle in einer externen Datenbank, die die ursprüngliche Quelle der Daten ist.</span><span class="sxs-lookup"><span data-stu-id="8c162-127">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data.</span></span> <span data-ttu-id="8c162-128">Die source-Zeichenfolge wird zur <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong>-Eigenschafteneinstellung des neuen <strong>TableDef</strong>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8c162-128">The source string becomes the <a href="tabledef-sourcetablename-property-dao.md"><strong>SourceTableName</strong></a> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c162-129"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="8c162-129"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="8c162-130">Optional</span><span class="sxs-lookup"><span data-stu-id="8c162-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="8c162-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8c162-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8c162-132">Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>) mit Informationen über die Quelle einer geöffneten oder verknüpften Datenbank oder einer Datenbank, die in einer Pass-Throug-Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c162-132">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table.</span></span> <span data-ttu-id="8c162-133">Weitere Informationen zu gültige Verbindungszeichenfolgen finden Sie in<strong> <a href="tabledef-connect-property-dao.md">Connect</a> </strong>-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c162-133">See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="8c162-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c162-134">Return value</span></span>

<span data-ttu-id="8c162-135">TableDef</span><span class="sxs-lookup"><span data-stu-id="8c162-135">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="8c162-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8c162-136">Remarks</span></span>

<span data-ttu-id="8c162-p106">Wenn Sie einen oder mehrere der optionalen Teile für die **CreateTableDef**-Methode weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschaften ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c162-p106">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its properties. See the individual property topics for more details.</span></span>

<span data-ttu-id="8c162-140">Wenn name sich auf ein Objekt bezieht, das bereits ein Mitglied einer Auflistung ist, oder wenn Sie im angefügten **TableDef**- oder **[Field](field-object-dao.md)**-Objekt eine ungültige Eigenschaft angeben, tritt bei Verwendung der **[Append](tabledefs-append-method-dao.md)**-Methode ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="8c162-140">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or [**Field**](field-object-dao.md) object you're appending, a run-time error occurs when you use the [**Append**](tabledefs-append-method-dao.md) method.</span></span> <span data-ttu-id="8c162-141">Sie können ein **TableDef** -Objekt außerdem erst dann an die **TableDefs** -Auflistung anfügen, nachdem Sie mindestens ein **Field** -Objekt für das **TableDef** -Objekt definiert haben.</span><span class="sxs-lookup"><span data-stu-id="8c162-141">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="8c162-142">Um ein **TableDef**-Objekt aus der **[TableDefs](tabledefs-collection-dao.md)**-Auflistung zu entfernen, verwenden Sie die **[Delete](tabledefs-delete-method-dao.md)**-Methode für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="8c162-142">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="8c162-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8c162-143">Example</span></span>

<span data-ttu-id="8c162-144">Dieses Beispiel erstellt ein neues **TableDef**-Objekt in der Northwind-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8c162-144">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="8c162-p108">In diesem Beispiel werden die **CreateTableDef**- und die **FillCache**-Methode sowie die **CacheSize**-, die **CacheStart**- und die **SourceTableName**-Eigenschaft verwendet, um die Datensätze in einer verknüpften Tabelle zwei Mal aufzuzählen. Anschließend werden die Einträge zweimal mit einem Cache für 50 Datensätze aufgezählt. Anschließend werden die Leistungsstatistiken für die Ausführung mit und ohne Zwischenspeicherung über die verknüpfte Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c162-p108">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```

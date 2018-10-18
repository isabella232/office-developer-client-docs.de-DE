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
ms.openlocfilehash: 99bccffb11dfb9813d52fed721a51b5417ef6be0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602818"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="b0238-102">Database.CreateTableDef-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0238-102">Database.CreateTableDef Method (DAO)</span></span>

<span data-ttu-id="b0238-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0238-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b0238-p101">Erstellt ein neues **[TableDef](tabledef-object-dao.md)** -Objekt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b0238-p101">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="b0238-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0238-106">Syntax</span></span>

<span data-ttu-id="b0238-107">*Ausdruck* . CreateTableDef (***Name***, ***Attribute***, ***SourceTableName***, ***Verbinden***)</span><span class="sxs-lookup"><span data-stu-id="b0238-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span></span>

<span data-ttu-id="b0238-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0238-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b0238-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0238-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0238-110">Name</span><span class="sxs-lookup"><span data-stu-id="b0238-110">Name</span></span></p></th>
<th><p><span data-ttu-id="b0238-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="b0238-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b0238-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b0238-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b0238-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0238-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0238-114">Name</span><span class="sxs-lookup"><span data-stu-id="b0238-114">Name</span></span></p></td>
<td><p><span data-ttu-id="b0238-115">Optional</span><span class="sxs-lookup"><span data-stu-id="b0238-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="b0238-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b0238-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b0238-p102">Ein <strong>Variant</strong>-Paramter (Untertyp <strong>String</strong>), der das neue <strong>TableDef</strong>-Objekt eindeutig benennt. Unter der <strong><a href="tabledef-name-property-dao.md">Name</a></strong>-Eigenschaft finden Sie Einzelheiten zu gültigen <strong>TableDef</strong>-Namen.</span><span class="sxs-lookup"><span data-stu-id="b0238-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0238-119">Attribute</span><span class="sxs-lookup"><span data-stu-id="b0238-119">Attributes</span></span></p></td>
<td><p><span data-ttu-id="b0238-120">Optional</span><span class="sxs-lookup"><span data-stu-id="b0238-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="b0238-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b0238-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b0238-p103">Eine Konstante oder Kombination aus Konstanten, mit der mindestens ein Merkmal des neuen <strong>TableDef</strong> -Objekts angegeben wird. Weitere Informationen finden Sie im Thema zur <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="b0238-p103">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0238-124">SourceTableName</span><span class="sxs-lookup"><span data-stu-id="b0238-124">SourceTableName</span></span></p></td>
<td><p><span data-ttu-id="b0238-125">Optional</span><span class="sxs-lookup"><span data-stu-id="b0238-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="b0238-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b0238-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b0238-p104">Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>), der den Namen einer Tabelle in einer externen Datenbank enthält, bei der es sich um die ursprüngliche Quelle der Daten handelt. Die source-Zeichenfolge wird zur <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong>-Eigenschafteneinstellung des neuen <strong>TableDef</strong>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b0238-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data. The source string becomes the <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0238-129">Verbinden</span><span class="sxs-lookup"><span data-stu-id="b0238-129">Connect</span></span></p></td>
<td><p><span data-ttu-id="b0238-130">Optional</span><span class="sxs-lookup"><span data-stu-id="b0238-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="b0238-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b0238-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b0238-p105">Ein <strong>Variant</strong>-Parameter (Untertyp <strong>String</strong>) mit Informationen über die Quelle einer geöffneten oder verknüpften Datenbank oder einer Datenbank, die in einer Pass-Throug-Abfrage verwendet wird. Weitere Informationen zu gültigen Verbindungszeichenfolgen finden Sie unter der <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b0238-p105">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table. See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0238-134"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b0238-134"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="b0238-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0238-135">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="b0238-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0238-136">Return value</span></span>
>>>>>>> <span data-ttu-id="b0238-137">master</span><span class="sxs-lookup"><span data-stu-id="b0238-137">master</span></span>

<span data-ttu-id="b0238-138">TableDef</span><span class="sxs-lookup"><span data-stu-id="b0238-138">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="b0238-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0238-139">Remarks</span></span>

<span data-ttu-id="b0238-p106">Wenn Sie einen oder mehrere der optionalen Teile für die **CreateTableDef** -Methode weglassen, können Sie die entsprechende Eigenschaft mithilfe einer entsprechenden Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie einige, aber nicht alle Eigenschaften ändern. Weitere Informationen finden Sie in den Themen zu den einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b0238-p106">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its properties. See the individual property topics for more details.</span></span>

<span data-ttu-id="b0238-143">Name bezieht sich auf ein Objekt, das bereits ein Element der Auflistung ist, oder Sie in der **TableDef** oder **[Field](field-object-dao.md)** -Objekt, die, das Sie anfügen, eine ungültige Eigenschaft angeben, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](tabledefs-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0238-143">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or **[Field](field-object-dao.md)** object you're appending, a run-time error occurs when you use the **[Append](tabledefs-append-method-dao.md)** method.</span></span> <span data-ttu-id="b0238-144">Sie können ein **TableDef** -Objekt außerdem erst dann an die **TableDefs** -Auflistung anfügen, nachdem Sie mindestens ein **Field** -Objekt für das **TableDef** -Objekt definiert haben.</span><span class="sxs-lookup"><span data-stu-id="b0238-144">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="b0238-145">Um ein **TableDef** -Objekt aus der **[TableDefs](tabledefs-collection-dao.md)** -Auflistung zu entfernen, verwenden Sie die **[Delete](tabledefs-delete-method-dao.md)** -Methode für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b0238-145">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="b0238-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0238-146">Example</span></span>

<span data-ttu-id="b0238-147">Dieses Beispiel erstellt ein neues **TableDef** -Objekt in der Northwind-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b0238-147">This example creates a new **TableDef** object in the Northwind database.</span></span>

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

<span data-ttu-id="b0238-p108">In diesem Beispiel werden die **CreateTableDef** - und die **FillCache** -Methode sowie die **CacheSize** -, die **CacheStart** - und die **SourceTableName** -Eigenschaft verwendet, um die Datensätze in einer verknüpften Tabelle zwei Mal aufzuzählen. Anschließend werden die Einträge zweimal mit einem Cache für 50 Datensätze aufgezählt. Anschließend werden die Leistungsstatistiken für die Ausführung mit und ohne Zwischenspeicherung über die verknüpfte Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0238-p108">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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

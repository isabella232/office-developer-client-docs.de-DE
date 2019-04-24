---
title: Recordset. FillCache-Methode (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300518"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="6d9c3-102">Recordset. FillCache-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d9c3-102">Recordset.FillCache method (DAO)</span></span>

<span data-ttu-id="6d9c3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d9c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d9c3-104">Füllt den lokalen Cache für ein **Recordset**-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen), teilweise oder vollständig auf.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d9c3-105">Syntax</span></span>

<span data-ttu-id="6d9c3-106">*Ausdruck* . FillCache (***Rows***, ***Start Bookmark***)</span><span class="sxs-lookup"><span data-stu-id="6d9c3-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="6d9c3-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d9c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d9c3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d9c3-109">Name</span><span class="sxs-lookup"><span data-stu-id="6d9c3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6d9c3-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="6d9c3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6d9c3-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6d9c3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6d9c3-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d9c3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d9c3-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="6d9c3-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="6d9c3-114">Optional</span><span class="sxs-lookup"><span data-stu-id="6d9c3-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="6d9c3-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6d9c3-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9c3-116">Ein <strong>Variant</strong>-Wert (Untertyp <strong>Integer</strong>), der angibt, wie viele Zeilen im Cache gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="6d9c3-117">Wenn Sie dieses Argument weglassen, wird der Wert durch die Einstellung der <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> -Eigenschaft bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-117">If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d9c3-118"><em>Start Bookmark</em></span><span class="sxs-lookup"><span data-stu-id="6d9c3-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="6d9c3-119">Optional</span><span class="sxs-lookup"><span data-stu-id="6d9c3-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="6d9c3-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6d9c3-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9c3-121">Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der ein Lesezeichen angibt.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="6d9c3-122">Der Cache wird ab dem Datensatz gefüllt, der durch dieses Lesezeichen angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="6d9c3-123">Wenn Sie dieses Argument weglassen, wird der Cache beginnend mit dem von der <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> -Eigenschaft angegebenen Datensatz gefüllt.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6d9c3-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d9c3-124">Remarks</span></span>

<span data-ttu-id="6d9c3-p103">Durch Zwischenspeichern wird die Leistung einer Anwendung verbessert, die Daten von einem Remoteserver abruft. Ein Cache ist Platz im lokalen Speicher, der für kürzlich vom Server abgerufene Daten reserviert ist, die voraussichtlich erneut angefordert werden, während die Anwendung ausgeführt wird. Fragt ein Benutzer Daten ab, überprüft das Microsoft Access-Datenbankmodul zuerst, ob die Daten noch im Cache vorhanden sind, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur die Daten gespeichert, die von einer ODBC-Datenquelle stammen.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="6d9c3-p104">Wenn Sie nicht warten möchten, bis der Cache mit Datensätzen gefüllt ist, die abgerufen werden, können Sie mithilfe der **FillCache**-Methode den Cache jederzeit explizit füllen. Das geht schneller, da mit **FillCache** mehrere Datensätze gleichzeitig abgerufen werden. Während Sie beispielsweise die Datensätze bildschirmweise anzeigen, ruft die Anwendung mithilfe von **FillCache** jeweils die Datensätze für den nächsten Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="6d9c3-p105">Jede mit einem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle, auf die Sie mit **Recordset**-Objekten zugreifen, kann einen lokalen Cache haben. Sie können einen Cache erstellen, indem Sie ein **Recordset**-Objekt aus einer Remotedatenquelle öffnen und dann die **CacheSize**- und **CacheStart**-Eigenschaften des **Recordset**-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="6d9c3-134">Wenn Zeilen und Start Bookmark einen Bereich von Datensätzen erstellen, die teilweise oder vollständig außerhalb des von den Eigenschaften **CacheSize** und **CacheStart** angegebenen Datensatzes liegen, wird der Teil des Recordset-Objekts außerhalb dieses Bereichs ignoriert und nicht geladen. in den Cache.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="6d9c3-135">Übersteigen die durch **FillCache** angeforderten Datensätze die in der Remotedatenquelle verbliebene Anzahl, ruft das Microsoft Access-Datenbankmodul nur die verbliebenen Datensätze ab, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="6d9c3-136">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="6d9c3-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="6d9c3-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d9c3-139">Example</span></span>

<span data-ttu-id="6d9c3-p107">In diesem Beispiel werden die **CreateTableDef**- und **FillCache**-Methoden und die **CacheSize**-, **CacheStart**- und **SourceTableName**-Eigenschaften verwendet, um die Datensätze in einer verknüpften Tabelle zweimal aufzuzählen. Daraufhin werden die Datensätze in einem Cache mit 50 Datensätzen zweimal aufgezählt. Anschließend enthält das Beispiel durch die verknüpfte Tabelle die Leistungsstatistik für die zwischengespeicherten und die nicht zwischengespeicherten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="6d9c3-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
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
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```

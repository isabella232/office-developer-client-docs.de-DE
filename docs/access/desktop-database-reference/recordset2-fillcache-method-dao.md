---
title: Recordset2.FillCache-Methode (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ef0f4ad298e316cbae295bcf4f6c4c5349b18655
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998532"
---
# <a name="recordset2fillcache-method-dao"></a><span data-ttu-id="f0113-102">Recordset2.FillCache-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="f0113-102">Recordset2.FillCache method (DAO)</span></span>

<span data-ttu-id="f0113-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0113-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0113-104">Füllt den lokalen Cache für ein **Recordset**-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält, teilweise oder vollständig auf (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen).</span><span class="sxs-lookup"><span data-stu-id="f0113-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0113-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0113-105">Syntax</span></span>

<span data-ttu-id="f0113-106">*Ausdruck* . FillCache (***Zeilen***, ***Anfangslesezeichen***)</span><span class="sxs-lookup"><span data-stu-id="f0113-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="f0113-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0113-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0113-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0113-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0113-109">Name</span><span class="sxs-lookup"><span data-stu-id="f0113-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f0113-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="f0113-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f0113-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f0113-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f0113-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0113-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0113-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="f0113-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="f0113-114">Optional</span><span class="sxs-lookup"><span data-stu-id="f0113-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f0113-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f0113-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f0113-p101">Ein <strong>Variant</strong>-Wert (Untertyp <strong>Integer</strong>), der angibt, wie viele Zeilen im Cache gespeichert werden sollen. Wenn Sie dieses Argument auslassen, wird der Wert durch die <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>-Eigenschafteneinstellung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f0113-p101">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache. If you omit this argument, the value is determined by the <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0113-118"><em>Anfangslesezeichen</em></span><span class="sxs-lookup"><span data-stu-id="f0113-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="f0113-119">Optional</span><span class="sxs-lookup"><span data-stu-id="f0113-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="f0113-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f0113-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f0113-p102">Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der ein Lesezeichen angibt. Der Cache wird ab dem Datensatz gefüllt, der durch dieses Lesezeichen angegeben wurde. Wenn Sie dieses Argument auslassen, wird der Cache ab dem Datensatz gefüllt, der durch die <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong>-Eigenschaft angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f0113-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark. The cache is filled starting from the record indicated by this bookmark. If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f0113-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0113-124">Remarks</span></span>

<span data-ttu-id="f0113-p103">Durch Zwischenspeichern wird die Leistung einer Anwendung verbessert, die Daten von einem Remoteserver abruft. Ein Cache ist Platz im lokalen Speicher, der für kürzlich vom Server abgerufene Daten reserviert ist, die voraussichtlich erneut angefordert werden, während die Anwendung ausgeführt wird. Fragt ein Benutzer Daten ab, überprüft das Microsoft Access-Datenbankmodul zuerst, ob die Daten noch im Cache vorhanden sind, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur die Daten gespeichert, die von einer ODBC-Datenquelle stammen.</span><span class="sxs-lookup"><span data-stu-id="f0113-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="f0113-p104">Wenn Sie nicht warten möchten, bis der Cache mit Datensätzen gefüllt ist, die abgerufen werden, können Sie mithilfe der **FillCache**-Methode den Cache jederzeit explizit füllen. Das geht schneller, da mit **FillCache** mehrere Datensätze gleichzeitig abgerufen werden. Während Sie beispielsweise die Datensätze bildschirmweise anzeigen, ruft die Anwendung mithilfe von **FillCache** jeweils die Datensätze für den nächsten Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="f0113-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="f0113-p105">Jede mit einem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle, auf die Sie mit **Recordset**-Objekten zugreifen, kann einen lokalen Cache haben. Sie können einen Cache erstellen, indem Sie ein **Recordset**-Objekt aus einer Remotedatenquelle öffnen und dann die **CacheSize**- und **CacheStart**-Eigenschaften des **Recordset**-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="f0113-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="f0113-134">Wenn Zeilen und Anfangslesezeichen erstellen einen Bereich von Datensätzen, die teilweise oder vollständig außerhalb des Bereichs von Datensätzen, die von den Eigenschaften **CacheSize** und **CacheStart** angegeben, der Teil des Recordset-Objekts außerhalb dieses Bereichs wird ignoriert und nicht geladen werden in den Cache.</span><span class="sxs-lookup"><span data-stu-id="f0113-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="f0113-135">Übersteigen die durch **FillCache** angeforderten Datensätze die in der Remotedatenquelle verbliebene Anzahl, ruft das Microsoft Access-Datenbankmodul nur die verbliebenen Datensätze ab, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f0113-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="f0113-136">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="f0113-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="f0113-p106">FillCache ruft nur Datensätze ab, die noch nicht zwischengespeichert wurden. Wenn Sie eine Aktualisierung aller zwischengespeicherten Daten erzwingen möchten, legen Sie die CacheSize-Eigenschaft des Recordset-Objekts auf 0 fest, setzen Sie die Größe des ursprünglich angeforderten Caches zurück, und verwenden Sie dann FillCache.</span><span class="sxs-lookup"><span data-stu-id="f0113-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="f0113-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f0113-139">Example</span></span>

<span data-ttu-id="f0113-p107">In diesem Beispiel werden die **CreateTableDef**- und **FillCache**-Methoden und die **CacheSize**-, **CacheStart**- und **SourceTableName**-Eigenschaften verwendet, um die Datensätze in einer verknüpften Tabelle zweimal aufzuzählen. Daraufhin werden die Datensätze in einem Cache mit 50 Datensätzen zweimal aufgezählt. Anschließend enthält das Beispiel durch die verknüpfte Tabelle die Leistungsstatistik für die zwischengespeicherten und die nicht zwischengespeicherten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="f0113-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
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

---
title: ExecuteOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 51c5ab78c4ea49ade7fd2b6972aa3753b0c6df09
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862310"
---
# <a name="executeoptionenum"></a><span data-ttu-id="572d1-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="572d1-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="572d1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="572d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="572d1-104">Gibt an, wie ein Anbieter einen Befehl ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="572d1-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="572d1-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="572d1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="572d1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="572d1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="572d1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="572d1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="572d1-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="572d1-109">0 x 10</span><span class="sxs-lookup"><span data-stu-id="572d1-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="572d1-110">Gibt an, dass der Befehl asynchron ausgeführt werden soll.
</span><span class="sxs-lookup"><span data-stu-id="572d1-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="572d1-111">Dieser Wert kann nicht mit dem <a href="commandtypeenum.md">ExecuteOptionEnum</a>-Wert <strong>adAsyncExecute</strong> kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="572d1-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="572d1-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="572d1-113">0 x 20</span><span class="sxs-lookup"><span data-stu-id="572d1-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="572d1-114">Gibt an, dass die verbleibenden Zeilen nach der ersten, in der <a href="cachesize-property-ado.md">CacheSize</a>-Eigenschaft angegebenen Menge asynchron abgerufen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="572d1-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="572d1-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="572d1-116">0 x 40</span><span class="sxs-lookup"><span data-stu-id="572d1-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="572d1-p102">Gibt an, dass der Hauptthread beim Abrufen nie blockiert. Wenn die angeforderte Zeile nicht abgerufen worden ist, wird die aktuelle Zeile automatisch an das Ende der Datei verschoben.
</span><span class="sxs-lookup"><span data-stu-id="572d1-p102">Indicates that the main thread never blocks while retrieving. If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="572d1-119">Wenn Sie ein <a href="recordset-object-ado.md">Recordset-Objekt</a> aus einem <a href="stream-object-ado.md">Stream</a> , der ein dauerhaft gespeichertes <strong>Recordset</strong>enthält öffnen, wird <strong>AdAsyncFetchNonBlocking</strong> keinen Einfluss; der Vorgang wird synchron und blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="572d1-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="572d1-120"><strong>AdAsynchFetchNonBlocking</strong> hat keine Auswirkung, wenn die <a href="commandtypeenum.md">AdCmdTableDirect</a> -Option zum Öffnen des <strong>Recordset-Objekt</strong>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="572d1-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="572d1-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="572d1-122">0 x 80</span><span class="sxs-lookup"><span data-stu-id="572d1-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="572d1-123">Gibt an, dass der Befehlstext ist, einen Befehl oder eine gespeicherte Prozedur, der gibt keine Zeilen (beispielsweise einen Befehl, der nur Daten einfügt) zurück.</span><span class="sxs-lookup"><span data-stu-id="572d1-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="572d1-124">Wenn alle Zeilen abgerufen werden, werden sie verworfen und nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="572d1-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="572d1-125"><strong>AdExecuteNoRecords</strong> kann nur als optionaler Parameter an die <strong>Command-</strong> oder <strong>Connection</strong> <strong>Execute</strong> -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="572d1-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="572d1-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="572d1-127">0 x 400</span><span class="sxs-lookup"><span data-stu-id="572d1-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="572d1-128">Gibt an, dass die Ergebnisse einer Befehlsausführung als Datenstrom zurückgegeben werden sollten.
</span><span class="sxs-lookup"><span data-stu-id="572d1-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="572d1-129"><strong>AdExecuteStream</strong> können nur als optionaler Parameter an den <strong>Befehl</strong> <strong>Execute</strong> -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="572d1-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="572d1-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="572d1-131">Gibt an, dass <strong>CommandText</strong> ein Befehl oder eine gespeicherte Prozedur ist, der bzw. die eine einzelne Zeile zurückgibt, die als <strong>Record</strong>-Objekt zurückgegeben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="572d1-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="572d1-132"><strong>adOptionUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="572d1-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="572d1-133">-1</span><span class="sxs-lookup"><span data-stu-id="572d1-133">-1</span></span></p></td>
<td><p><span data-ttu-id="572d1-134">Gibt an, dass der Befehl nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="572d1-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="572d1-135">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="572d1-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="572d1-136">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="572d1-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="572d1-137">Konstante</span><span class="sxs-lookup"><span data-stu-id="572d1-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="572d1-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="572d1-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="572d1-139">AdoEnums.ExecuteOption.ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="572d1-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="572d1-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="572d1-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="572d1-141">AdoEnums.ExecuteOption.NORECORDS</span><span class="sxs-lookup"><span data-stu-id="572d1-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="572d1-142">AdoEnums.ExecuteOption.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="572d1-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>


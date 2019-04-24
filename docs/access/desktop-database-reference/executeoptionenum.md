---
title: ExecuteOptionEnum (Access Desktop Database Reference)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293245"
---
# <a name="executeoptionenum"></a><span data-ttu-id="56692-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="56692-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="56692-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56692-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56692-104">Gibt an, wie ein Anbieter einen Befehl ausführen sollte.</span><span class="sxs-lookup"><span data-stu-id="56692-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56692-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="56692-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="56692-106">Wert</span><span class="sxs-lookup"><span data-stu-id="56692-106">Value</span></span></p></th>
<th><p><span data-ttu-id="56692-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56692-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56692-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="56692-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="56692-109">0x10</span><span class="sxs-lookup"><span data-stu-id="56692-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="56692-110">Gibt an, dass der Befehl asynchron ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56692-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="56692-111">Dieser Wert kann nicht mit dem <a href="commandtypeenum.md">ExecuteOptionEnum</a>-Wert <strong>adAsyncExecute</strong> kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="56692-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56692-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="56692-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="56692-113">0x20</span><span class="sxs-lookup"><span data-stu-id="56692-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="56692-114">Gibt an, dass die verbleibenden Zeilen nach der ersten, in der <a href="cachesize-property-ado.md">CacheSize</a>-Eigenschaft angegebenen Menge asynchron abgerufen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="56692-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56692-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="56692-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="56692-116">0x40</span><span class="sxs-lookup"><span data-stu-id="56692-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="56692-117">Gibt an, dass der Hauptthread beim Abrufen nie blockiert.</span><span class="sxs-lookup"><span data-stu-id="56692-117">Indicates that the main thread never blocks while retrieving.</span></span> <span data-ttu-id="56692-118">Wenn die angeforderte Zeile nicht abgerufen worden ist, wird die aktuelle Zeile automatisch an das Ende der Datei verschoben.</span><span class="sxs-lookup"><span data-stu-id="56692-118">If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="56692-119">Wenn Sie ein <a href="recordset-object-ado.md">Recordset</a> -Objekt aus einem <a href="stream-object-ado.md">Stream</a> -Objekt mit einem persistent gespeicherten <strong>Recordset</strong>-Objekt öffnen, hat <strong>adAsyncFetchNonBlocking</strong> keine Auswirkung; der Vorgang wird synchron und blockiert.</span><span class="sxs-lookup"><span data-stu-id="56692-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="56692-120"><strong>adAsynchFetchNonBlocking</strong> hat keine Auswirkungen, wenn die <a href="commandtypeenum.md">adCmdTableDirect</a> -Option zum Öffnen des <strong>Recordset-Objekts</strong>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56692-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56692-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="56692-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="56692-122">0x80</span><span class="sxs-lookup"><span data-stu-id="56692-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="56692-123">Zeigt an, dass der Befehlstext ein Befehl oder eine gespeicherte Prozedur ist, der keine Zeilen zurückgibt (beispielsweise ein Befehl, der nur Daten einfügt).</span><span class="sxs-lookup"><span data-stu-id="56692-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="56692-124">Wenn alle Zeilen abgerufen werden, werden sie verworfen und nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56692-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="56692-125"><strong>adExecuteNoRecords</strong> kann nur als optionaler Parameter an die <strong>Command</strong> -oder <strong>Connection</strong> <strong>Execute</strong> -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="56692-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56692-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="56692-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="56692-127">0x400</span><span class="sxs-lookup"><span data-stu-id="56692-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="56692-128">Gibt an, dass die Ergebnisse einer Befehlsausführung als Datenstrom zurückgegeben werden sollten.</span><span class="sxs-lookup"><span data-stu-id="56692-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="56692-129"><strong>adExecuteStream</strong> kann nur als optionaler Parameter an die <strong>Command</strong> <strong>Execute</strong> -Methode übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="56692-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56692-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="56692-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="56692-131">Gibt an, dass <strong>CommandText</strong> ein Befehl oder eine gespeicherte Prozedur ist, der bzw. die eine einzelne Zeile zurückgibt, die als <strong>Record</strong>-Objekt zurückgegeben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="56692-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56692-132"><strong>adOptionUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="56692-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="56692-133">-1</span><span class="sxs-lookup"><span data-stu-id="56692-133">-1</span></span></p></td>
<td><p><span data-ttu-id="56692-134">Gibt an, dass der Befehl nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="56692-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="56692-135">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="56692-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="56692-136">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="56692-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56692-137">Konstante</span><span class="sxs-lookup"><span data-stu-id="56692-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56692-138">AdoEnums. ExecuteOption. ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="56692-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56692-139">AdoEnums. ExecuteOption. ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="56692-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56692-140">AdoEnums. ExecuteOption. ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="56692-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56692-141">AdoEnums. ExecuteOption. noRECORDs</span><span class="sxs-lookup"><span data-stu-id="56692-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56692-142">AdoEnums. ExecuteOption. unSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="56692-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>


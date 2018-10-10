---
title: CommandTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b694d2d691766063f418aba6535fd9c7a8e3ca95
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472696"
---
# <a name="commandtypeenum"></a><span data-ttu-id="9c172-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="9c172-102">CommandTypeEnum</span></span>


<span data-ttu-id="9c172-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c172-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9c172-104">Gibt an, wie ein Befehlsargument interpretiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9c172-104">Specifies how a command argument should be interpreted.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c172-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="9c172-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9c172-106">Wert</span><span class="sxs-lookup"><span data-stu-id="9c172-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9c172-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c172-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c172-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-109">-1</span><span class="sxs-lookup"><span data-stu-id="9c172-109">-1</span></span></p></td>
<td><p><span data-ttu-id="9c172-110">Gibt kein Befehlstypargument an.</span><span class="sxs-lookup"><span data-stu-id="9c172-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c172-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-112">1</span><span class="sxs-lookup"><span data-stu-id="9c172-112">1</span></span></p></td>
<td><p><span data-ttu-id="9c172-113">Wertet <a href="commandtext-property-ado.md">CommandText</a> als Textdefinition eines Befehls oder eines gespeicherter Prozeduraufrufs aus.</span><span class="sxs-lookup"><span data-stu-id="9c172-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c172-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-115">2</span><span class="sxs-lookup"><span data-stu-id="9c172-115">2</span></span></p></td>
<td><p><span data-ttu-id="9c172-116">Wertet <strong>CommandText</strong> als Namen einer Tabelle aus, deren Spalten alle von einer intern generierten SQL-Abfrage zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9c172-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c172-117"><strong>adCmdStoredProc fest</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-118">4</span><span class="sxs-lookup"><span data-stu-id="9c172-118">4</span></span></p></td>
<td><p><span data-ttu-id="9c172-119">Wertet <strong>CommandText</strong> als Namen einer gespeicherten Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="9c172-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c172-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-121">8</span><span class="sxs-lookup"><span data-stu-id="9c172-121">8</span></span></p></td>
<td><p><span data-ttu-id="9c172-p101">Standardwert. Gibt an, dass der Befehlstyp in der <strong>CommandText</strong>-Eigenschaft unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9c172-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c172-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-125">256</span><span class="sxs-lookup"><span data-stu-id="9c172-125">256</span></span></p></td>
<td><p><span data-ttu-id="9c172-p102">Wertet <strong>CommandText</strong> als Dateinamen eines dauerhaft gespeicherten <a href="recordset-object-ado.md">Recordsets</a> aus. Wird lediglich mit <strong>Recordset. </strong><a href="open-method-ado-recordset.md">Open</a> oder <a href="requery-method-ado.md">Requery</a> verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c172-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c172-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="9c172-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="9c172-129">512</span><span class="sxs-lookup"><span data-stu-id="9c172-129">512</span></span></p></td>
<td><p><span data-ttu-id="9c172-130">Wertet <strong>CommandText</strong> als Namen einer Tabelle, deren Spalten alle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9c172-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="9c172-131">Nur verwendet mit <strong>"Recordset.Open"</strong> oder <strong>Requery</strong> .</span><span class="sxs-lookup"><span data-stu-id="9c172-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="9c172-132">Um die <a href="seek-method-ado.md">Seek</a> -Methode verwenden, muss das <strong>Recordset</strong> mit <strong>AdCmdTableDirect</strong>geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9c172-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="9c172-133">Dieser Wert kann nicht mit dem <a href="executeoptionenum.md">ExecuteOptionEnum</a>-Wert <strong>adAsyncExecute</strong> kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9c172-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c172-134">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="9c172-134">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="9c172-135">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9c172-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c172-136">Konstante</span><span class="sxs-lookup"><span data-stu-id="9c172-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c172-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="9c172-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c172-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="9c172-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c172-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="9c172-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c172-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="9c172-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c172-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="9c172-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c172-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="9c172-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c172-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="9c172-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>


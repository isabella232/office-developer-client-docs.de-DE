---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e456cfcc344c818504cb2ae1c2af9a4294b004ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876414"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="84ce1-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="84ce1-102">SearchDirectionEnum</span></span>


<span data-ttu-id="84ce1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84ce1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84ce1-104">Gibt die Richtung einer Datensatzsuche innerhalb eines [Recordsets](recordset-object-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="84ce1-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84ce1-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="84ce1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="84ce1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="84ce1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="84ce1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84ce1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84ce1-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="84ce1-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="84ce1-109">-1</span><span class="sxs-lookup"><span data-stu-id="84ce1-109">-1</span></span></p></td>
<td><p><span data-ttu-id="84ce1-110">Sucht rückwärts und hält am Anfang des <strong>Recordset-Objekts</strong>.</span><span class="sxs-lookup"><span data-stu-id="84ce1-110">Searches backward, stopping at the beginning of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="84ce1-111">Wenn eine Übereinstimmung gefunden wird, wird der Datensatzzeiger bei <a href="bof-eof-properties-ado.md">BOF</a>positioniert.</span><span class="sxs-lookup"><span data-stu-id="84ce1-111">If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ce1-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="84ce1-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="84ce1-113">1</span><span class="sxs-lookup"><span data-stu-id="84ce1-113">1</span></span></p></td>
<td><p><span data-ttu-id="84ce1-114">Sucht vorwärts und hält am Ende des <strong>Recordset-Objekts</strong>an.</span><span class="sxs-lookup"><span data-stu-id="84ce1-114">Searches forward, stopping at the end of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="84ce1-115">Wenn eine Übereinstimmung gefunden wird, wird der Datensatzzeiger bei <a href="bof-eof-properties-ado.md">EOF</a>positioniert.</span><span class="sxs-lookup"><span data-stu-id="84ce1-115">If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="84ce1-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="84ce1-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="84ce1-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="84ce1-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84ce1-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="84ce1-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84ce1-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="84ce1-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84ce1-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="84ce1-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>


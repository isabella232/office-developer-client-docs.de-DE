---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f9fdf9dd5908b65ae3b6f6ce5a44eba07e4d9bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308806"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="abf29-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="abf29-102">SearchDirectionEnum</span></span>


<span data-ttu-id="abf29-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="abf29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="abf29-104">Gibt die Richtung einer Datensatzsuche innerhalb eines [Recordsets](recordset-object-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="abf29-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="abf29-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="abf29-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="abf29-106">Wert</span><span class="sxs-lookup"><span data-stu-id="abf29-106">Value</span></span></p></th>
<th><p><span data-ttu-id="abf29-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abf29-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abf29-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="abf29-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="abf29-109">-1</span><span class="sxs-lookup"><span data-stu-id="abf29-109">-1</span></span></p></td>
<td><p><span data-ttu-id="abf29-110">Sucht rückwärts und hält am Anfang des Recordset- <strong>Objekts</strong>.</span><span class="sxs-lookup"><span data-stu-id="abf29-110">Searches backward, stopping at the beginning of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="abf29-111">Wenn keine Übereinstimmung gefunden wird, wird der Datensatzzeiger an <a href="bof-eof-properties-ado.md">BOF</a>positioniert.</span><span class="sxs-lookup"><span data-stu-id="abf29-111">If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abf29-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="abf29-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="abf29-113">1</span><span class="sxs-lookup"><span data-stu-id="abf29-113">1</span></span></p></td>
<td><p><span data-ttu-id="abf29-114">Sucht nach vorn und beendet am Ende des <strong>Recordset-Objekts</strong>.</span><span class="sxs-lookup"><span data-stu-id="abf29-114">Searches forward, stopping at the end of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="abf29-115">Wenn keine Übereinstimmung gefunden wird, wird der Datensatzzeiger am <a href="bof-eof-properties-ado.md">EOF</a>positioniert.</span><span class="sxs-lookup"><span data-stu-id="abf29-115">If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="abf29-116">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="abf29-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="abf29-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="abf29-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="abf29-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="abf29-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abf29-119">AdoEnums. SearchDirection. rückwärts</span><span class="sxs-lookup"><span data-stu-id="abf29-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abf29-120">AdoEnums. SearchDirection. FORWARD</span><span class="sxs-lookup"><span data-stu-id="abf29-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>


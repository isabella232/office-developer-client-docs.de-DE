---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3998f41c1400a2870633f19228cbf73189e9527a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474785"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="97c1b-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="97c1b-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="97c1b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="97c1b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="97c1b-p101">Gibt Optionen an, um ein [Stream](stream-object-ado.md)-Objekt zu öffnen. Die Werte können mit einer OR-Operation kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="97c1b-p101">Specifies options for opening a [Stream](stream-object-ado.md) object. The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97c1b-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="97c1b-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="97c1b-107">Wert</span><span class="sxs-lookup"><span data-stu-id="97c1b-107">Value</span></span></p></th>
<th><p><span data-ttu-id="97c1b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97c1b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97c1b-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="97c1b-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="97c1b-110">1</span><span class="sxs-lookup"><span data-stu-id="97c1b-110">1</span></span></p></td>
<td><p><span data-ttu-id="97c1b-111">Öffnet das <strong>Stream</strong>-Objekt im asynchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="97c1b-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c1b-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="97c1b-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="97c1b-113">4</span><span class="sxs-lookup"><span data-stu-id="97c1b-113">4</span></span></p></td>
<td><p><span data-ttu-id="97c1b-p102">Identifiziert den Inhalt des <em>Source</em>-Parameters als bereits geöffnetes <a href="record-object-ado.md">Record</a>-Objekt. Das Standardverhalten besteht darin, die <em>Quelle</em> als eine URL zu behandeln, die direkt auf einen Knoten in einer Baumstruktur verweist. Der diesem Knoten zugeordnete Standarddatenstrom wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="97c1b-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c1b-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="97c1b-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="97c1b-118">-1</span><span class="sxs-lookup"><span data-stu-id="97c1b-118">-1</span></span></p></td>
<td><p><span data-ttu-id="97c1b-p103">Standardwert. Gibt das Öffnen des <strong>Stream</strong>-Objekts mit Standardoptionen an.</span><span class="sxs-lookup"><span data-stu-id="97c1b-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97c1b-121">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="97c1b-121">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="97c1b-122">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="97c1b-122">These constants do not have ADO/WFC equivalents.</span></span>


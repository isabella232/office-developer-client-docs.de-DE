---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721220"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="3d04f-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="3d04f-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="3d04f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d04f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d04f-p101">Gibt Optionen an, um ein [Stream](stream-object-ado.md)-Objekt zu öffnen. Die Werte können mit einer OR-Operation kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="3d04f-p101">Specifies options for opening a [Stream](stream-object-ado.md) object. The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d04f-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="3d04f-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="3d04f-107">Wert</span><span class="sxs-lookup"><span data-stu-id="3d04f-107">Value</span></span></p></th>
<th><p><span data-ttu-id="3d04f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d04f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d04f-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="3d04f-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="3d04f-110">1</span><span class="sxs-lookup"><span data-stu-id="3d04f-110">1</span></span></p></td>
<td><p><span data-ttu-id="3d04f-111">Öffnet das <strong>Stream</strong>-Objekt im asynchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="3d04f-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d04f-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="3d04f-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="3d04f-113">4</span><span class="sxs-lookup"><span data-stu-id="3d04f-113">4</span></span></p></td>
<td><p><span data-ttu-id="3d04f-p102">Identifiziert den Inhalt des <em>Source</em>-Parameters als bereits geöffnetes <a href="record-object-ado.md">Record</a>-Objekt. Das Standardverhalten besteht darin, die <em>Quelle</em> als eine URL zu behandeln, die direkt auf einen Knoten in einer Baumstruktur verweist. Der diesem Knoten zugeordnete Standarddatenstrom wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3d04f-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d04f-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="3d04f-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="3d04f-118">-1</span><span class="sxs-lookup"><span data-stu-id="3d04f-118">-1</span></span></p></td>
<td><p><span data-ttu-id="3d04f-p103">Standardwert. Gibt das Öffnen des <strong>Stream</strong>-Objekts mit Standardoptionen an.</span><span class="sxs-lookup"><span data-stu-id="3d04f-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3d04f-121">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="3d04f-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="3d04f-122">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="3d04f-122">These constants do not have ADO/WFC equivalents.</span></span>


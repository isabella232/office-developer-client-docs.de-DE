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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314749"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="2c56a-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="2c56a-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="2c56a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c56a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c56a-104">Gibt Optionen an, um ein [Stream](stream-object-ado.md)-Objekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c56a-104">Specifies options for opening a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="2c56a-105">Die Werte können mit einer OR-Operation kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2c56a-105">The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c56a-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="2c56a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="2c56a-107">Wert</span><span class="sxs-lookup"><span data-stu-id="2c56a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="2c56a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c56a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c56a-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="2c56a-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="2c56a-110">1</span><span class="sxs-lookup"><span data-stu-id="2c56a-110">1</span></span></p></td>
<td><p><span data-ttu-id="2c56a-111">Öffnet das <strong>Stream</strong>-Objekt im asynchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="2c56a-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c56a-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="2c56a-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="2c56a-113">4</span><span class="sxs-lookup"><span data-stu-id="2c56a-113">4</span></span></p></td>
<td><p><span data-ttu-id="2c56a-p102">Identifiziert den Inhalt des <em>Source</em>-Parameters als bereits geöffnetes <a href="record-object-ado.md">Record</a>-Objekt. Das Standardverhalten besteht darin, die <em>Quelle</em> als eine URL zu behandeln, die direkt auf einen Knoten in einer Baumstruktur verweist. Der diesem Knoten zugeordnete Standarddatenstrom wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2c56a-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c56a-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="2c56a-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="2c56a-118">-1</span><span class="sxs-lookup"><span data-stu-id="2c56a-118">-1</span></span></p></td>
<td><p><span data-ttu-id="2c56a-p103">Standardwert. Gibt das Öffnen des <strong>Stream</strong>-Objekts mit Standardoptionen an.</span><span class="sxs-lookup"><span data-stu-id="2c56a-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2c56a-121">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="2c56a-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="2c56a-122">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="2c56a-122">These constants do not have ADO/WFC equivalents.</span></span>

